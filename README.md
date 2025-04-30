# On_Spectrum_Sensing_Using_ML

### Problem Statement

The development and breakthroughs made in the field of communication and related systems has lead to a drastic increase in the consumption of the radio spectrum (the frequency spectrum over which most of the wireless communication occurs). Radio spectrum being a finite resource, has lead to its deficit. 

In order to sovle this problem, efficient management and allocation of radio spectrum amongst various users is of utmost priority. This is where machine learning steps in the picture. We propose an ML oriented model, which analyses the particular frequency channel, and depending on its behaviour and state, does 1 of the 2 following options : 

1) Makes the frequency channel avaiable to other users who are in need of the radio spectrum.
2) Reserves that frequency channel for a primary user and doesn't allow any other users to take over the current channel, which is in use.

### Proposed Design

The proposed system has been divided into multiple sub-phases for easier understanding and sequential execution : 

#### 1) Generation of synthetic dataset :

        In this particular step we artifically generate a synthetic dataset using functions (most of them comming from the random package in python).
