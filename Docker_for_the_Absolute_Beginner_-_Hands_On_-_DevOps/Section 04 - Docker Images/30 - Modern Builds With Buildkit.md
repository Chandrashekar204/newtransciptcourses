# Modern Builds With Buildkit

*Section: Docker Images*

1 In the previous lecture, we walked through four problems 2 with the traditional Docker builder. 3 Packages re-downloaded from scratch on every build, 4 secrets leaking into image metadata, 5 no matter which workaround we tried, 6 architecture lock-in to whatever machine 7 we happen to be building on, 8 and independent stages running sequentially 9 when they could be running in parallel. 10 Now, all four of these problems have the same root cause.

11 The legacy build engine was designed years ago 12 for a simpler world, 13 and it never picked up the features that modern teams need. 14 So a few years ago, 15 Docker rewrote the build engine from scratch, 16 and they called it BuildKit. 17 And as of Docker 23.0, released in January 2023, 18 BuildKit became the default builder. 19 You don't have to enable it. 20 You don't have to add a flag. It's just on.

21 In fact, the build you ran in our earlier demo 22 was already powered by BuildKit. 23 That plus building 12.3 seconds output, 24 you saw at the top of the build, that's BuildKit talking. 25 So what does BuildKit do for us? 26 Well, a few things. 27 First, the caching is smarter. 28 BuildKit hashes the actual content of files 29 going into a layer 30 rather than relying on file system timestamps.

31 So cache hits are more reliable. 32 And second, it adds four new capabilities 33 that fix the four problems we just identified one for one. 34 Let me walk you through each one. 35 But first, a quick note on the CLI. 36 The command line front end for BuildKit is called BuildX. 37 When you installed Docker back in the setup lesson, 38 you probably saw Docker BuildX plugin in the package list. 39 That was BuildX going in.

40 For everyday work, you don't really need to think about it. 41 Plain Docker build already routes through BuildKit 42 and BuildX under the hood. 43 But when you want the advanced features 44 I'm about to show you, 45 you'll switch to the explicit form Docker BuildX build. 46 Okay, so let's look at the four fixes. 47 The first one is cache mounts. 48 This is the fix for redownloading packages on every build.

49 Here's how it works. 50 Inside a run instruction, 51 you add a mount option with typeset to cache 52 and you tell BuildKit which directory to keep around between builds. 53 Let me show you what that looks like. 54 A quick note on the line at the top, 55 that hash syntax Docker Dockerfile colon one isn't a comment, 56 it's a directive. 57 It tells BuildKit to use the modern Dockerfile front end, 58 which is what unlocks the mount syntax.

59 Without it, BuildKit falls back to basic syntax 60 and the mount option won't work. 61 So whenever you're using these BuildKit features, 62 always start your Dockerfile with that line. 63 Now, with this cache mount in place, 64 the first build downloads the pip packages as normal. 65 But the next time you build, 66 those downloads come from your local cache 67 instead of the network. 68 Builds that used to take a minute can now take 10 seconds, 69 basically free speed.

70 The second fix is secret mounts. 71 Remember the secret section from the previous lecture, 72 the build arg flag env, copy then rm, multistage workarounds. 73 Every single approach leaked the secret in some way. 74 BuildKit fixes this cleanly. 75 Instead of passing the secret in as a build argument 76 or copying it as a file, 77 you mount it into a single run step. 78 Here's the pattern. 79 And when you build, you pass the secret in 80 from outside the Dockerfile like this.

81 So what's actually happening here, 82 BuildKit reads your secret file from your local file system, 83 mounts it into the build container 84 at slash run slash secret slash Mikey 85 for the duration of that one run step, 86 and then unmounts it the moment the step finishes. 87 The secret is available to that one command 88 and nothing else. 89 It never gets copied into any layer. 90 It never shows up in the build history.

91 It never appears in Docker inspect. 92 Run Docker history on the final image 93 and you won't see a trace of it. 94 Much, much safer than every approach 95 we walked through last time. 96 And arguably the single most important reason 97 to be using BuildKit, 98 especially if your build touches private resources. 99 The third fix is multi-platform builds. 100 This is the fix for architecture lock-in.

101 With BuildKit, one command builds 102 for as many architectures as you list. 103 Here's what that looks like. 104 So what does this do? 105 BuildKit builds the image twice, 106 once for AMD64, once for ARM64, 107 and pushes both to the registry under a single name 108 as a multi-arc manifest. 109 Then when someone runs a Docker pull on an Apple Silicon Mac, 110 Docker automatically pulls the ARM64 variant.

111 On an Intel laptop, it pulls AMD64. 112 Same image name, right architecture every time. 113 This is actually why most images on Docker Hub 114 just work on Apple Silicon Macs 115 without any extra effort 116 the maintainers published multi-arc manifests. 117 Pretty neat when you think about it. 118 And the fourth fix is parallel stage execution. 119 Remember the example I mentioned last time 120 where you have two from stages, 121 one for a front-end bundle, 122 another for a back-end binary 123 that don't depend on each other.

124 The traditional builder ran them one after the other. 125 BuildKit doesn't. 126 It looks at the whole Docker file upfront, 127 figures out what depends on what, 128 and runs the independent pieces side-by-side. 129 And here's the nice thing. 130 You don't have to write anything new 131 in the Docker file to get this. 132 It's just how BuildKit operates. 133 You write the same multi-stage Docker file 134 you would have written before, 135 and BuildKit figures out the parallelism on its own.

136 Free speed up for nothing. 137 Okay, one last note. 138 Before we move on, 139 everything you learned in the Docker images lecture still applies. 140 The Docker history command still shows layers. 141 Layers still cache the same way. 142 The Docker file syntax from, run, copy, entry point, 143 that's all unchanged. 144 BuildKit is a faster, smarter engine 145 sitting under the same Docker file you already know.

146 So nothing to relearn, 147 just new capabilities you can opt into when you need them.
