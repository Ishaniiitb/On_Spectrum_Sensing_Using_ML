# On Spectrum Sensing, a Machine Learning Method for Cognitive Radio Systems

## Problem Statement

The development and breakthroughs made in the field of communication and related systems has lead to a drastic increase in the consumption of the radio spectrum (the frequency spectrum over which most of the wireless communication occurs). Radio spectrum being a finite resource, has lead to its deficit. 

In order to sovle this problem, efficient management and allocation of radio spectrum amongst various users is of utmost priority. This is where machine learning steps in the picture. We propose an ML oriented model, which analyses the particular frequency channel, and depending on its behaviour and state, does 1 of the 2 following options : 

1) Makes the frequency channel avaiable to other users who are in need of the radio spectrum.
2) Reserves that frequency channel for a primary user and doesn't allow any other users to take over the current channel, which is in use.

## Proposed Design

The proposed system has been divided into multiple sub-phases for easier understanding and sequential execution : 

### 1) Generation of synthetic dataset :

In this particular step we artifically generate a synthetic dataset using functions (most of them comming from the random package in python). First we assume 1 of 2 hypothesis : 

1) H(a) : In this hypothesis we assume that the primary user is absent or is not transmitting any signal actively. This means that the particular channel as of now is only carrying a noise signal, and the total energy statistic of the channel will be the energy of the noise signal.
2) H(p) : In this hypothesis we assume that the primary user is present and is actively transmitting a signal. This means that the energy statistic of the channel will the sum of both, the energy statistic of the signal being transmitted by the user and the energy statistic of the noise signal.

This property of the frequency channel, i.e, the energy statistic, is vital for predicting the presence of a primary user. So we generate two datasets, a training dataset (of size 10,000 samples) and a testing dataset (of size 8,000 samples). We first pass these datasets through a K-means clustering algorithm, in order to convert this unlabelled dataset into a labeled dataset for our suprvised ML models which will come later on.
