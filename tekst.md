- [ ] **Think about the order of stuff** (when visual number sense?)
  - mention when pressed
  - after subitizing I guess 
  - maybe mention previous methods and how we differ
    - bridge from artificial neural populations to vaes?

# Introduction

- **Why** is your research interesting/why does it interest you?
  - How do people learn number?
    - or rather, what are the cognitive mechanisms behind fundamental number sense, as some animals have those too
    - it's something that automatically develops, but yet is very abstract
  - How does (lived) experience/vision/perception relate to something so abstract
    - abstract in the sense that numbers are ideal and universal in scope
- We train an unsupervised generative model to learn visual numerosity representions 
  - (So some sort of instance counting)
- Particulair interest in natural images

# Subitizing

- Keep it simple, only mention visual number sense related stuff later
- subitizing is a skill that allows us to identify a small number of items at a glance
  - refer to the figure to say that the set size of the elephants can't be readily percieved, at least not as sudden
  - so subitizing only works for small numerosities in the subitizing range
  - we specifically research visual sets
  - an mechanism used for exact representation of small numerosity
<!-- at this point the whole goal of the research needs to be sort of clear! -->
- SOSdataset clearly show a number of salient objects in the subitizng range


# Visual number sense

**Keep it simple!** Mention that is very fast bc of holistic pattern recognition and achieved by parallel processing
And that it is different from counting bc it's automatic/requires no concious attention mechanisms
- Numerosity is an intergral part of the visual world (perceptual category just as color)
- Therefore,  an unsupervised (develops automatically) algorithm that also learns a particulair representation to test wether numerosity information is really integral to the visual world. (Variational Autoencoders)

- What is visual number sense
  - The idea that numerosity is an intergral part of our visual world, similair to how color is a definite perceptual phenomena connected to a certain experience
    - so the experience of percieving say 3 versus items is fundamentally different, similair to how percieving a red and a blue object is a different kind of experience
  - and sort of the reason that we have this experience of numerosity is because it is important for behaviour
  - (refering to the figure) the difference in perceptual character can be seen in the sort of jump in this graph

- So rapid that no indivual attention to elements is needed
  - likely the result of holistic pattern recognition or peak-reading in the visiospatial system 
  - preattentive
- Nonmediated, as in a mostly neural/pereceptual process
  - no counting/individual attentn
  - no arthimatic
- Develops automatically in animals, children and also, at least under some circumstances, in artificial learning models 
  - artificial stuff is simple tho
  - likely because any representational system of the world needs to represent numerosity to make decisions
    - (be it predictory models or different kinds)


# Variational Autoencoders

- Feeding images and reconstructing them, so building up a latent representation that encodes the most important/emblematic features of the data
- (and this process is completely unsupervised)

How an autoencoder works is that it tries to find two functions, shown as the encoder and decoder networks. These functions are often types of neural networks, and in the case of images often convolutional networks specifically. The task of the encoder network is to map the input data to a much smaller "latent" or inferred, more simple representation of the data. This is a real valued vector. This small vector is then decoded back to an actual image by the decoder network. A simple autoencoder like this then learns by trying to reconstruct the original as well as possible, for example computing the gradient of the network by a pixel by pixel loss. 


# Optimizing reconstructions #

## fpl ##

- **Gist** a loss function that works well for subitizing bc it retains object contours better
- vaes are blurry, which is bad for subitizing because objects merge into the background
- refer to the figure and point to distorted/depeasing objects
- result in sharper contours reconstruction
- achieved by the first few layers of pretrained deep cnn
  - so loses detail, but that is less important for subitizing

## syn ##

- More data was needed, as non pretrained vaes need a lot of data
- class imbalance

## Size-invarient numerisity detectors ##

- One dimension of the latent space often responded to changes in numerosity, while it's reponse to increase cumaltive object area (point to syntethic figure on how it's measure) in center stayed relativelt centered.  Some other dimensionens showed a more discontious response to changes in numerisoty, while showcasing increasing varience in "absolute" response with growing cumaltive area

# Subitizing performance

(While refering to the vae figure)

- an image is fed into the encoder part and transformed into a latent vector, as shown here
- after this transformation, we retrieve the count label (so in this case 3), and then try to predict the 
  correct label feeding the latent vector into a simple softmax classifier
- (subitizing might not be numerical computation , i.e. it's recycled elsehwere for numerical tasks/goals, so just like salient object peak-reading another "connectiost" module reads out the result)












