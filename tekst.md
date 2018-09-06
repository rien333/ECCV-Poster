# Introduction

- Why is your research interesting/why does it interest you?
- How do people learn number
- How does (lived) experience/vision/perception relate to something so abstract?

# Subitizing



- Keep it simple, only mention visual number sense related stuff related\
- subitizing is a skill that allows us to identify a small number of items at a glance
  - we specifically research visual sets
  - refer to the figure to say that the set size of the elephants can't be readily percieved, at least not as sudden
<!-- at this point the whole goal of the research needs to be sort of clear! -->
- SOSdataset clearly show a number of salient objects in the subitizng range

# Variational Autoencoders

How an autoencoder works is that it tries to find two functions, shown as the encoder and decoder networks. These functions are often types of neural networks, and in the case of images often convolutional networks specifically. The task of the encoder network is to map the input data to a much smaller "latent" or inferred, more simple representation of the data. This is a real valued vector of for example size 100. This small vector is then decoded back to an actual image by the decoder network. A simple autoencoder like this then learns by trying to reconstruct the original as well as possible, for example computing the gradient of the network by a pixel by pixel loss. 


# Visual number sense

- What is visual number sense
  - The idea that numerosity is an intergral part of our visual world, similair to how color is a definite perceptual phenomena connected to a certain experience
    - so the experience of percieving say 3 versus items is fundamentally different, similair to how percieving a red and a blue object is a different kind of experience
  - and sort of the reason that we have this experience of numerosity is because it is important for behaviour

- So rapid that no indivual attention to elements is needed
  - likely the result of holistic pattern recognition or peak-reading in the visiospatial system 
  - preattentive
- Nonmediated, as in a mostly neural/pereceptual process
  - no counting
  - 
- Develops automatically in animals, children and also, at least under some circumstances, in artificial learning models 
  - artificial stuff is simple tho
  - likely because any representational system of the world needs to represent numerosity to make decisions
    - (be it predictory models or different kinds)


# Subitizing performance

(While refering to the vae figure)

- an image is fed into the encoder part and transformed into a latent vector, as shown here
- after this transformation, we retrieve the count label (so in this case 3), and then try to predict the 
  correct label feeding the latent vector into a simple softmax classifier
  
