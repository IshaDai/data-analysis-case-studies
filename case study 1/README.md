<h1 align='center'> Introduction to Data Management, Analysis and Security</h1>

<h2 align='center'> Case Study 1 - Transcoding Data Analysis</h2>

### 1 Introduction

Video content is being produced, transported and consumed in more ways and by devices than ever. To facilitate this process, 
seamless interaction between video producing, transporting and consuming devices is required. The difference in avaliable 
resources, network bandwidth and video representation types between devices requires a mechanism for video content adaptation 
and translation. One such mechanism is video transcoding.

#### So What is Video Transcoding?

Video transcoding (sometimes refered to as encoding) is the process of converting a video from one digital format to another. 
A format is defined by characteristics such as:

* Bit rate
* Frame rate
* Spatial resolution
* Coding syntax
* Content

One of the earliest applications of transcoding was to adapt the bit rate of a precompressed video stream to a channel 
bandwidth. For example, a TV program may be originally compressed at a high bit rate for studio applications, but later 
needs to be transmitted over a public channel at a much lower bit rate.

#### So what are we doing with this?

Transcoding is a computationally demanding process and several methods has been proposed in order to increase its efficiency. 
Runtime scheduling of transcoding jobs in multicore and cloud environments is hard as resource requirements may not be known 
before hand. Currently, for video transcoding jobs, one has to rely on worst-case values which lead to an over provisioning 
of resources. This is due to the fact that the resource requirement of a transcoding job is highly dependent on the video 
data to be converted and its conversion parameters. In order to allow such distributed and multicore systems to overcome 
the problem of over provisioning, a method for predicting the resource requirement of each job is required. If the scheduler 
can predict accurately how long each job would take to execute on a given platform, it can make an optimal decision, returning 
results faster, possibly minimizing energy, waiting time and maximizing throughput.

### 2 Data Description

The presented dataset (`transcoding_data.csv`) contains 23 columns which include input and output video characteristics, 
along with their transcoding time and memory resource requirements, while transcoding videos to different but valid formats. 
The dataset was collected based on experiments on an Intel i7-3720QM CPU through randomly picking output parameters of a video 
transcoding application. The attributes present in the dataset and their information are presented in the table below.

In this case study, we are going to analyze `transcoding_data.csv` file, and build a transcoding time prediction model and show the 
significance of the provided datasets. More specific analysis process can be found in the `transcode.ipynb` file.
