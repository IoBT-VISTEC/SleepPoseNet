# SleepPoseNet: Multi-View Multi-Task Learning for Sleep Postural Transition Recognition Using UWB

## Abstract

**Recognizing the movements during sleep is crucial for the monitoring of patients with sleep disorders. However, the utilization of the deep learning approaches ultra-wideband (UWB)-based indoor applications for the classification of human sleeping postures has not been explored widely. This study investigates the performance of the off-the-shelf single antenna UWB in a novel application of sleep postural transition (SPT) recognition. The proposed Multi-View Multi-Task Learning, entitled SleepPoseNet or SPN, with time series data augmentation aims to classify four standard SPTs. SPN exhibits an ability to capture both time and frequency features, including the movement and direction of sleeping positions. Three cost functions for multi-views, multi-tasks, and classification are proposed to optimize SPN. The data recorded from 26 volunteers displayed that SPN with mean accuracy of 79.7 +/- 0.5% significantly outperformed the mean accuracy of 73.5 +/- 0.7% obtained from deep convolution neural network (DCNN) in a recent state-of-the-art work on human activity recognition using UWB. Apart from UWB system, SPN with the data augmentation can ultimately be adopted to learn and classify time series data in various applications.**

## Data description

**There are totally 930 input samples.**

**Data**

* **Input signal: X[930,160,180]**
* **Label: y[930]**

Each input sample is a 16 s UWB radar signal output which is contained in 2D array size 160x180, the first axis is slow-time and the second axis is range bin (fast-time). The movement of sleep postural transitions mostly begin at 5-7th second or indices 50-70 in first axis. 

There are six possibility labels for each input sample.

* **0** - Supine to Left
* **1** - Supine to Right
* **2** - Supine to Prone
* **3** - Left to Supine
* **4** - Right to Supine
* **5** - Prone to Supine

*There are some subjects performed more than one experiment set, we provide a **'subject.txt'** file tells subject's number of each sample index.* 

## Experiment Protocol

The UWB radar system was attached to the wall with 0.8 m height above the bed. The pitch angle was approximately 45 degrees downward towards the bed. Six STPs were selected. There were 26 volunteers, including 19 males and 7 females participated in this study. The height ranged from 1.55 to 1.80 m, the weight ranged from 40 to 90 kg, and the age ranged from 18 to 35 years old. The experiment commenced with the subjects lying down with a supine position in the middle of the bed under the line-of-sight of the radar. The subjects were instructed to perform 6 motions, in a sample, following an arranged sequence: supine to left lateral, left lateral to supine, supine to right lateral, right lateral to supine, supine to prone, and prone to supine, at their own pace. The subjects were given 10-15 s to rest while inhaling for 4-5 times before performing the next motion. This allowed the radar system to obtain the respiration features before and after each change of posture.

<p align='center'>
<img src="/fig/bedroom.png" height=300px>
</p>
<p align='center'> <b>Fig. 1</b> The experiment room, UWB radar and camera position.</p>

## Device

In this paper, we use **XeThru X4M03** with 10Hz frame rate.

<p align='center'><img src="/fig/xethru.jpg" height=300px></p>
<p align='center'> <b>Fig. 2</b> XeThru X4M03</p>

## Dataset

**Note!** This manuscript is under review. The dataset and code are available when the manuscript is accepted.

## Citation

When using (any part) of this dataset, please cite
