The goal is to train a model on MNIST dataset to:

Achieve an accuracy of 99.4 consistently in a no. of epochs.
Within 15 epochs
Less than 10k parameters

Code1 - Setup

Target:

Set up the skeleton:

dropout=0.1, batchNorm after every Conv2D etc.

Results:

Parameters - 10,170

Best training accuracy- 99.05

Best test accuracy - 99.26

Analysis:

Model is under-fitting

The gap between test and train is high

Capacity can be pushed further

Code2

Target:

Added GAP layer at the end and a Conv2D layer after GAP.

MaxPooling shifted after RF=5,5

Also modified kernel sizes and input/output channels.

Results:

Parameters - 9,914

Best training accuracy- 99.14

Best test accuracy - 99.44

Analysis:

Model is under-fitting.

Target is reached but not consistent.

Code3 - Setup

Target:

Not modifying the skeleton of the model.

Increased dropout from 0.1 to 0.15

Results:

Parameters - 9,914

Best training accuracy- 98.81

Best test accuracy - 99.36

Analysis:

Model is under-fitting.

The accuracy of both test and train is reduced greatly if we increase dropout.

Code4 - Setup

Target:

Decreased dropout from 0.1 to 0.05

Added RandomRotation in the model

Results:

Parameters - 9,914

Best training accuracy- 99.06

Best test accuracy - 99.48

Analysis:

The accuracy is reached (11th epoch) but still need to fine tune. Let's see after adding step LR.

Code5

Target:

Added step LR to the model

Removed RandomRotation in the model (not needed)

Results:

Parameters - 9,914

Best training accuracy- 99.38

Best test accuracy - 99.45

Analysis:

The accuracy is reached.
