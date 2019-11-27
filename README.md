# Auto Tuning Spectral Clustering
Python3 code for the IEEE SPL paper "Auto-Tuning Spectral Clustering for SpeakerDiarization Using Normalized Maximum Eigengap"

## DER Leaderboards

#### **DIHARD 2019 Dev Set**
192 Sessions  

No collar for evalutation  
Overlap regions are also evaluated  
  
Track 1: Oracle VAD (Full DH2019 Dev set) 
Full dev set  
  
| System and Error | Total Error: Before Reseg | Total Error: After Reseg  | Speaker Error: Before Reseg | Speaker Error: After Reseg|
| ---------------------------------------------------------------|:------:|:------:|:--------:|:----:|
| __DiHard 2019 Baseline (JHU), (t1, test-set_opt, thres -0.03)__           | 24.24% | -      | 13.5%   | -     |
| USC t2D02_ahc_plda (_test-set opt._, thres +0.07)                         | 30.02% | 36.97% | 19.1%   | 16.1% |

Track 2: System VAD (Full DH2019 Dev set)  

| System and Error | Total Error: Before Reseg | Total Error: After Reseg  | Speaker Error: Before Reseg | Speaker Error: After Reseg|
| ---------------------------------------------------------------|:------:|:------:|:--------:|:----:|
| __t2:DiHard 2019 Baseline (JHU) (t2, system SAD)__                     | -      | -     | -     | -     |
| USC t2D02_ahc_plda (_test-set opt._, thres -0.2)                       | 46.95% | 47.1% | 15.7% | 14.9% |
| USC t2D03_spt_cos (_test-set opt._, RP thres 0.08 for cos. sim. value) | -      | -     | -     | -     |   


#### **NIST SRE 2000 CALLHOME Disk-8(LDC2001S97)**

Collar 0.25, No overlap for evaluation  
Track 1: Oracle VAD (Full DH2019 Dev set) 

| System and Error | Total Error: Before Reseg | Total Error: After Reseg  | Speaker Error: Before Reseg | Speaker Error: After Reseg|
| --------------------------------------------------------------- |:------:|:------:|:--------:|:-----:|
| JHU, 2017, Garcia-Romero [1] (t1, Oracle SAD)               |        | -      | 12.8 %   | 9.9%  |
| Google, 2018, Quan Wang, d-vector + Spectral Clustering [3] | 18.8%  | -      | 12.0%    | -     |
| Google, 2019, Fully Supervised [4]                          | -      | -      | 7.6%     | -     |
| __Auto-Tuning NMESC [5]__                                   | 14.14% |   -    | 7.24%    | -     |  


### **AMI meeting corpora**

Collar 0.25, No overlap for evaluation  
Track 1: Oracle VAD (Full DH2019 Dev set) 

| System and Error | Total Error: Before Reseg | Total Error: After Reseg  | Speaker Error: Before Reseg | Speaker Error: After Reseg|
| ---------------------------------------------------------------|:------:|:------:|:--------:|:----:|
| USC t2B02 (test-set-optimized threshold: -0.09)         | -      | -      | -        | -    |
| USC t2C01 (test-set-optimized threshold:  0.44)         | -      | -      | -        | -    |  



#### **callhome American English (LDC97S42 + LDC97T14) Evaluation**

Collar 0.25, No overlap for evaluation  
Track 1: Oracle VAD (Full DH2019 Dev set) 

- __CH-109__ (2-speaker subset, test condition: known number of speakers)  

| System and Error | Total Error: Before Reseg | Total Error: After Reseg  | Speaker Error: Before Reseg | Speaker Error: After Reseg|
| ---------------------------------------------------------------|:------:|:------:|:------:|:-----:|
| __Google, 2018, Quan Wang, d-vector + Spectral Clustering [3]__| 12.54% | -      | 5.97%  | -     |
| __IBM, 2017, Zbyněk Zajíc [5]__                                | -      | -      | 7.84%  | -     |
| t2D02_spt_plda (KNOWN # of spks, LLR th 0.0 for raw PLDA)       | 5.61%  | 5.41%  | 1.3%   | 0.7%  |  


- __CH-Eval__ (Eval set from corpora, speakers >= 2, test condition:unknown number of condition)  

| System and Error | Total Error: Before Reseg | Total Error: After Reseg  | Speaker Error: Before Reseg | Speaker Error: After Reseg|
| ---------------------------------------------------------------|:------:|:------:|:--------:|:----:|
| __Google, 2018, Quan Wang, d-vector + Spectral Clustering [3]__| 12.48% | -      | 6.03%    | -    |
| USC t2B02 (except thr is 0)                                    | 15.39% | -      | 3.9%     | -    |

#### **NIST RT-03 CTS (LDC2007S10) Evaluation**

Collar 0.25, No overlap for evaluation  
Track 1: Oracle VAD (Full DH2019 Dev set) 

| System and Error | Total Error: Before Reseg | Total Error: After Reseg  | Speaker Error: Before Reseg | Speaker Error: After Reseg|
| ---------------------------------------------------------------|:------:|:------:|:--------:|:----:|
| __Google, 2018, Quan Wang, d-vector + Spectral Clustering [3]__| 12.30% | -      | 3.76%    | -    |
| t2B02 (test-set-optimized threshold: -0.09)                | -      | -      | -        | -    |
| t2C01 (test-set-optimized threshold:  0.44)                | -      | -      | -        | -    |  

