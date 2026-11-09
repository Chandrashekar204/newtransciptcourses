# 2.6 — Big O: Drop Non-Dominants

> Section 2: Big O

So now we're going to look at another way that we can simplify big O. That's called drop non dominance. So to illustrate this I'm going to start with our nested for loops that we saw in the last video. But I'm going to add an additional for loop after these. So we have our nested for loops above and a separate standalone for loop down here. So let's flip over and take a look at this in IntelliJ. So there is our method there. And we'll call this down here with the number ten.

And I'll run this. Okay. So I'm going to scroll to the top here. And you can see it starts with zero zero and then goes down to here where it goes to nine nine. And then we have zero through nine. So now let's flip back. So this nested for loop ran o of n squared times. That was the zero 0 to 9 nine. And this for loop ran o of n times. So the total number of operations was n squared plus n. So that would be o of n squared plus n. But as n gets larger the n squared grows much faster than the n.

Even if we only took this to 100, the n squared portion would be 10,000 operations and that standalone n would be 100 operations. So the n squared is the dominant firm and the n is the non-dominant firm. And as n becomes larger and larger, you can see that that standalone n starts becoming irrelevant. So we just drop the n. So this rule of simplification. Is dropped. Non dominance.

----------------------------------------
