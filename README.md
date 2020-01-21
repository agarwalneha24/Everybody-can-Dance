# Everybody-can-Dance
Given two videos–one of a target person whose appearance we wish to synthesize, and the other of a source subject whose motion we wish to impose onto our target person – we transfer moton from source subject to target subject.
It is the implementation of Generative adversarial Networks which is the combination of two Deep-Learning models.

Generator And Discriminator

Generator
The generator part of a GAN learns to create fake data by incorporating feedback from the discriminator. It learns to make the discriminator classify its output as real which means they learn how to model or create new thing based on the probability distribution p(x=y).

Discriminator
The discriminator in a GAN is simply a classiﬁer. It tries to distinguish real data from the data created by the generator. It could use any network architecture appropriate to the type of data it’s classifying, which means they learn how to model the conditional 
probability distribution function (p.d.f) p(y—x).

GAN Training
Because a GAN contains two separately trained networks, its training algorithm must
address two complications:
1. GANs must juggle two diﬀerent kinds of training (generator and discriminator).
2. GAN convergence is hard to identify.

Alternating Training
The generator and the discriminator have diﬀerent training processes. So how do we
train the GAN as a whole?
1. GAN training proceeds in alternating periods:
2. The discriminator trains for one or more epochs.
3. The generator trains for one or more epochs.

Repeat steps 1 and 2 to continue to train the generator and discriminator networks. We keep the generator constant during the discriminator training phase. As discriminator training tries to ﬁgure out how to distinguish real data from fake, it has to learn
how to recognize the generator’s ﬂaws. That’s a diﬀerent problem for a thoroughly trained generator than it is for an untrained generator that produces random output. Similarly, we keep the discriminator constant during the generator training phase.
Otherwise the generator would be trying to hit a moving target and might never converge.
It’s this back and forth that allows GANs to tackle otherwise intractable generative problems. We get a toehold in the diﬃcult generative problem by starting with a much simpler classiﬁcation problem. Conversely, if you can’t train a classiﬁer to tell
the diﬀerence between real and generated data even for the initial random generator output, you can’t get the GAN training started.

Convergence
As the generator improves with training, the discriminator performance gets worse because the discriminator can’t easily tell the diﬀerence between real and fake. If the generator succeeds perfectly, then the discriminator has a 50This progression poses a problem for convergence of the GAN as a whole: the discriminator feedback gets less meaningful over time. If the GAN continues training past the point when the discriminator is giving completely random feedback, then the generator starts to train on junk feedback, and its own quality may collapse.

METHODOLOGY: 
We aim to transfer motion from a given source video to the target video through working with the three given stages:  
1. Pose Detection-We’ll here use Open Pose library which uses deep learning to extract features for detecting pose(CNN Neural Network) 
2. Global Pose Normalization  
3. Mapping from normalized pose stick figures to the target subject-Implementation of Generative Adversial Networks.

This project can leave a huge impact on media industry by producing high quality content easily requiring minimum time investment and in least expensive manner. Our Contributions is to produce  learning-based networks for human motion transfer between videos, and the quality of our results which demonstrate complex motion transfer in realistic and detailed videos. Our project aims to produce quality content in a very lesser cost and lesser time thus implementing high skill required task which can only be done by professionals.It can decrease the cost of  support dancers in low budget movies. Dance is for everyone it should democratize equally even for  people with disabilities.
