# 4.16 — LL: Reverse

> Section 4: Linked Lists

So in this video we are going to reverse a linked list. So our method is going to start like this. It doesn't have any return type. We are just going to reverse the linked list. So when you do this, you are reversing a particular linked list in place. It is not creating a duplicate linked list that is in the reverse order. So at a high level, the process of doing this is we take head and tail and we reverse them. Then we're just going to start taking the arrows and flipping them over the other way until the entire linked list is reversed.

So I'm going to put this all back and I will move this down here. And the first thing we'll do is reverse head and tail. And in order to do that, we'll need a variable temp that points to this head node. Then we can say head equals tail and tail equals temp. So let's look at the three lines of code. To do this. First we have to create this temp variable. Set it equal to head. And then we say head is equal to tail. And tail is equal to temp. Let's look at these in with the rest of our code like this.

And now let's bring our linked list back. So in order to do this we will need a couple more variables. We will need one that points to the node after temp. And I will call that one after, and one that points at the node before temp. And I will call that before. And these are going to move through the linked list as we are flipping these arrows over to go the other way. So I'll put this back. And let's create these two variables. So after equals temp dot next and before equals null.

So let's look at these in with the rest of our code. That's what we have so far. And now comes the hard part for the reverse method. So let's bring back our linked list here. And in order to move those through the linked list, we're going to use a for loop that goes the length of the linked list. And inside the for loop, we're going to have four lines of code that have to be in the right order. If they're not in the right order, this will break.

So the first line says after is equal to temp. Next. So in the first iteration it's already equal to temp. Next. And it's very important to do this first in the for loop, because in this next line here we say temp dot next equals before. So that is temp dot next equals before. And that flips the arrow back the other way. So the thing that makes this method difficult is that gap between the 11 and the three. So you have to have that after variable pointing to the node that is across that gap.

So then we'll say before equals temp that's going to move that up to this node. And now we can have temp jump across that gap with this line temp equals after. Like that. So let's walk through this to the end of the length list. We'll say after equals temp dot next. And we have to do that before this next line that creates that gap. And then we'll move before up. And temp over. And we'll do it again and we'll flip that arrow back. We'll move before up and temp over.

And now this will be the last time that we run this for loop. So after equals temp. Next. Well temp. Next is now null. So after is going to get set to null. Then we say temp dot next equals before. Before temp. And temp equals after. And now we're done with the for loop. And now we have a reversed linked list. So now let's look at this for loop and with the rest of our code. And that is our reverse method. So we'll look at this code in a moment in IntelliJ.

And when we do. We will create this linked list one through four, and then we'll run the reverse method and then it will be four through one. So let's flip over to IntelliJ and take a look at this. So there is our reverse method there. And I'll come up to our main tab here with our main method. And this creates our linked list with values one through four. And this line here will print out that linked list. I'll run this. And you can see that we have a linked list with values one through four.

So I'll come up here. And I will paste in this line of code and that will reverse our linked list. And then we'll run the print list method again. So I'll run this. And now our linked list is four through one. And that is our method for reverse.


########################################
