# Things that Are Others

*I've decided to do a little project where I'll try to answer questions on some of the sub reddits I follow.  I have no desire to participate in discussions on internet boards, but I think it's a useful excercise to think about answers.*

Group identification seems to be a big deal these days.  Which group you belong to seems to indicate more and more about who you vote for and what you think about various policy proposals, but while that's incredibly important, it's not what I've come here to talk about today.  What I'm interested in is how you classify things that you don't know anything about.

Here's a question:

[Classification: Having the NN know when it doesn't know](https://www.reddit.com/r/MachineLearning/comments/chq8pk/d_classification_having_the_nn_know_when_it/)

Ok, well it's not a question, it's some sort of weird clause that isn't fully a sentence, but you know, the internet...

The asker is building an app (*aren't we all*) that would help visually impaired people identify animals given a picture on their phone.  Sure.  I guess that could help people like those plant apps that help you find things.  Seems like you'd have a problem with the animal holding still in a place where you could see it with your phone, but maybe they've done the market research.  Or maybe it's just a school problem.  The asker is using some sort of NN to learn and then classify targets, but they want to know what happens when you give your phone a picture of "junk".  How do you know there's not an animal, or that this is an animal that you didn't train on.  

This is a big problem, because like all the other commenters point out, there's not a good way to do this given your standard CNNs.  It has classes.  Your input goes into one of those classes.  There may be some output confidence, but what do those numbers mean?  

One choice is to train on all of the other stuff that exists in the world and form a class of **not-animal**.  Maybe.  But that's an awful big space.  Every fork, every spoon, and every truck.  Everything?  In all conditions?  How do stuffed animals play here?  There's some other suggestions about using Bayesian NN's, and I don't know enough about them at this point to say anything, but my guess is that it's going to be a tough lift to get something that cutting edge for this one person working on an iphone.

Really, though I think that it's important to talk about limitations of NNs and think about what we can get out of them.  What the user could really use is getting a likelihood out of their system, not just some final probability of type.  It's a bit of a hack, but if you had a real likelihood for each type, you could then set some threshold and say below which, I don't know what I have.  You might even be able to do something funny and say whether the likelihood of all animals was high enough to classify it as an unknown animal.  But this isn't what you usually get out of an NN.  You don't get a real probability density function over your classes.  While the NNs are much better than the SVNs of old, you sort of have the same behaviour.  You get something better out of a GAN since it learns the PDF, but you don't have a good mathematical representation of it.  I could say more about my real work, but I won't.

My advice to the asker is that given the limitations of the NN, they may actually want to take a step back into the dark ages of computer vision.  It might be worthwhile to do the animal/not-animal classification using some sort of feature, i.e. edges or sifts or a saliency calculation that tells you if there's something worth looking in your frame.  Then if that pops, go ahead and use your NN to do a classification.

In any event, you're going to need a big disclaimer on your app that says it is not responsible for mis-identifying the bear that is about to eat you.

chomp.    
