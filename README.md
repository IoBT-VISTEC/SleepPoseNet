# SleepPoseNet: Multi-View Learning for Sleep Postural Transition Recognition Using UWB
This work is published in IEEE Journal of Biomedical and Health Informatics (JBHI'2020)

## Abstract

**Recognizing the movements during sleep is crucial for the monitoring of patients with sleep disorders. However, the utilization of Ultra-Wideband (UWB) radar for the classification of human sleep postures has not been explored widely. This study investigates the performance of the off-the-shelf single antenna UWB in a novel application of sleep postural transition (SPT) recognition. The proposed Multi-View Learning, entitled SleepPoseNet or SPN, with time series data augmentation, aims to classify four standard SPTs. SPN exhibits an ability to capture both time and frequency features, including the movement and direction of sleeping positions. The data recorded from 38 volunteers displayed that SPN, with a mean accuracy of 73.7±0.8% significantly outperformed the mean accuracy of 59.9±0.7% obtained from a deep convolution neural network (DCNN) in recent state-of-the-art work on human activity recognition using UWB. Apart from the  UWB system, SPN with data augmentation can ultimately be adopted to learn and classify time series data in various applications.**

## Data description
All data can be downloaded [here](https://drive.google.com/file/d/1bXQZDdWqCEVAjtJkmyE32_e7JN6d05Ey/view?usp=sharing).
## Dataset I
**There are totally 930 input samples.**

* **Input signal: X[930,160,180]**
* **Label: y[930]**

Each input sample is a 16s UWB radar signal output, which is contained in a 2D array of  size 160x180; the first axis is slow-time and the second axis is range bin (fast-time).

There are six possibility labels for each input sample.

* **0** - Supine to Left
* **1** - Supine to Right
* **2** - Supine to Prone
* **3** - Left to Supine
* **4** - Right to Supine
* **5** - Prone to Supine

**In the paper, left and right are considered as sides, so there are a total of 4 classes**

**Files description** \
X = wall-placed radar data \
y = label as a digit \
subjects = subject or participant label


## Dataset II

Session 1 = static scene  
Session 2 = with the presence of a fan (a moving object)  

Each sample contains only one postural transition (the change of a posture)
Dimension = #samples, slow time, range bins or fast time = #samples, 160, 180
Each range bin approximately represents 5 cm, so 180 range bins = 900 cm
Each slow time index represents 0.1 s, so 160 slow time indices = 16 s

Label data (y_digit)
* **0** = Supine side
* **1** = Side prone
* **2** = Prone side
* **3** = Side supine
* **4** = Supine prone
* **5** = Prone supine
* **6** = Background

**In the paper, we used only classes 0, 3, 4, 5, and 6, so there are a total of 5 classes**

**Files description** \
X_wall = wall-placed radar data \
X_ceiling = ceiling-placed radar data \
y_digit = label as a digit \
y_str = label as a string \
subjects = subject or participant label


<p align='center'>
<img src="/fig/bedroom.png" height=300px>
</p>
<p align='center'> <b>Fig. 1</b> The experiment room, UWB radar, and camera position.</p>

## Device

In this paper, we use **XeThru X4M03** with 10Hz frame rate.

<p align='center'><img src="/fig/xethru.jpg" height=300px></p>
<p align='center'> <b>Fig. 2</b> XeThru X4M03</p>

Any enquiry can be sent to maytusp@gmail.com

## Citation
When using any part of this dataset, please cite [our paper](https://doi.org/10.1109/JBHI.2020.3025900)

```
@article{piriyajitakonkij2020sleepposenet,
  title={SleepPoseNet: Multi-view learning for sleep postural transition recognition using UWB},
  author={Piriyajitakonkij, Maytus and Warin, Patchanon and Lakhan, Payongkit and Leelaarporn, Pitshaporn and Kumchaiseemak, Nakorn and Suwajanakorn, Supasorn and Pianpanit, Theerasarn and Niparnan, Nattee and Mukhopadhyay, Subhas Chandra and Wilaiprasitporn, Theerawit},
  journal={IEEE Journal of Biomedical and Health Informatics},
  year={2020},
  publisher={IEEE}
}
```
