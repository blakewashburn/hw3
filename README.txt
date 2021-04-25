README
Blake Washburn

The collection of files provided in this Github enviornment were written for 
Homework 3 in Dr. Feng Luo's Deep Learning Course at Clemson University during
the Spring 2021 semester - CPSC8430

The files in this repo and their purpose are listed below:
prompt.pdf - Contains the directions provided for the assignment
dcgan.ipynb - Implementation of Deep Convolutional GAN network
wgan.ipynb - Implementation of Wasserstein GAN network
acgan.ipynb - Implementation of Auxilary Classifier GAN network
report.pdf - written report analysis performance of implemented networks

To run the above files, the following libraries are required:
python 3.8
pytorch 1.7
matplotlib 3.2.2
numpy 1.19

The dataset required to run the code is the cifar10 dataset. To download this 
dataset, simply change the download option from "False" to "True" in the cell
specified by the "Grab CIFAR10 Dataset" comment. The line of code to change is:
"dataset = datasets.CIFAR10(root="./data", download=False, transform=..."
This will create a new folder in the current directory named "data", which 
will be used by all of the implementation files in this repo.

To run the files mentioned above, first, create three folders named dcganOutput,
wganOutput, and acganOutput. These will be used to store images produced by the
dcgan.ipynb, wgan.ipynb, and acgan.ipynb files. Next, create a jupyter notebook
in an enviornment with the specified packages installed and run the cells from 
top to bottom.

All files are set with a training epoch number of 135. Using Palmetto with a 
Deep Learning enviornment setup specified in the Palmetto documentation, 
the files took 4 hours complete execution when run at the same time. 

None of the three implementation files utilize the FID scoring method to 
determine the accuracy of their generated images. It was my intent to add this. 
However, I spent too much time working on implementation, and neglected this
until the last couple of hours before the project was due. I then ran into 
issues regarding its download and use. As a result, images are produces, but
are not tested for their FID score.