# WiDs-Endterm

### Tough thing---
CIFAR-100 has very few images per class around 500/class if we try to train out                     model on these raw images our model will overfit, and will fail in the new images
thats why first of all i normalized all the images my transforming pixel values into a standard range for that i used mean and std deviation fo th eCIFAR dataset this also helped the neural nets to stay stable.

along with this i randomly cropped, zoom in and zoom out the images to make more fake dataset for training the model this helps in training the model (model learns how a dog looks from a distance or whatever)
We are told to use custom architecture i made the class ProjectCNN, this model uses a Pyramid shape it starts from 64 filters and doubles the number of filter as it proceeds further. so that this allows the network to learn simple features first and then complex features

then i implemented some basic neural network logics ect

for the loss function of the model i used CrossEntropyLoss ( as it was a multi-class classification)
for the optimizer i used Adam ( as it's adapts the learning rate for each parameter individually it is more reliable for the training)
### i also used OneCycleLR as the Scheduler changes the learning rate seemed look
And at last there is the basic training loop and evalutaion loop and graph plotting...
