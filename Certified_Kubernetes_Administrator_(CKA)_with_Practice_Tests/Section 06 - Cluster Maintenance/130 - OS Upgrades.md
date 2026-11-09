# OS Upgrades

*Section: Cluster Maintenance*

1 In this lecture, 2 we will discuss about scenarios 3 where you might have to take down nodes as part 4 of your cluster, say for maintenance purposes, 5 like upgrading a base software 6 or applying patches like security patches, et cetera, 7 on your cluster. 8 In this lecture, we will see the options available 9 to handle such cases. 10 So you have a cluster with a few nodes 11 and pods serving applications.

12 What happens when one of these nodes go down? 13 Of course, the pods on them are not accessible. 14 Now, depending upon how you deploy those pods, 15 your users may be impacted. 16 For example, since you have multiple replicas 17 of the blue pod, the users accessing the blue application 18 are not impacted as they're being served 19 through the other blue pod that's online. 20 However, users accessing the green pod are impacted as 21 that was the only pod running the green application.

22 Now, what does Kubernetes do in this case? 23 If the node came back online immediately, 24 then the cube control process starts 25 and the pods come back online. 26 However, if the node was down for more than five minutes, 27 then the pods are terminated from that node. 28 Well, Kubernetes considers them as dead. 29 If the pods were part of a replica set, 30 then they're recreated on other nodes.

31 The time it waits for a pod to come back online is known 32 as the pod eviction timeout 33 and is set on the controller manager 34 with a default value of five minutes. 35 In modern Kubernetes, pod eviction is handled 36 through node taints and pod tolerations. 37 When a node becomes not ready 38 or unreachable, Kubernetes applies no execute taints 39 and pods are evicted after a grace period 40 unless they tolerate those taints.

41 So whenever a node goes offline, the master node waits 42 for up to five minutes before considering the node dead. 43 When the node comes back online 44 after the pod eviction timeout, 45 it comes up blank without any pod scheduled on it. 46 Since the blue pod was part of a replica set, 47 it had a new pod created on another node. 48 However, since the green pod was not part 49 of a replica set, it's just gone.

50 Thus, if you have maintenance tasks 51 to be performed on a node, if you know 52 that the workloads running on the node have other replicas, 53 and if it's okay that they go down for a short period 54 of time, and if you're sure the node will come back online 55 within five minutes, you can make a quick upgrade 56 and reboot. 57 However, you do not for sure know if a node is going 58 to be back online in five minutes.

59 Well, you cannot for sure say it is going to be back at all. 60 So there is a safer way to do it. 61 You can purposefully drain the node of all the workloads so 62 that the workloads are moved to other nodes in the cluster. 63 Well, technically, they're not moved. 64 When you drain a node, the pods are gracefully terminated 65 from the node that they're on and recreated on another. 66 The node is also cordoned or marked as unschedulable, 67 meaning no pods can be scheduled on this node 68 until you specifically remove the restriction.

69 Now that the pods are safe on the other nodes, 70 you can reboot the first node. 71 When it comes back online, it is still unschedulable. 72 You then need to uncoordinated so 73 that the pods can be scheduled on it again. 74 Now remember, the pods that were moved 75 to the other nodes don't automatically fall back. 76 If any of those pods were deleted 77 or if new pods were created in the cluster, 78 then they would be created on this node.

79 Apart from drain and uncordon, 80 there is also another command called cordon. 81 Cordon simply marks a node unschedulable. 82 Unlike drain, it does not terminate 83 or move the pods on an existing node. 84 It simply makes sure 85 that new pods are not scheduled on that node. 86 Well, the set for this lecture. 87 Head over to the practice test 88 and practice training, coordinating 89 and then coordinating a note.

90 I will see you in the next lecture.
