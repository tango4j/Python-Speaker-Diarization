# Auto Tuning Spectral Clustering
Python3 code for the IEEE SPL paper "Auto-Tuning Spectral Clustering for SpeakerDiarization Using Normalized Maximum Eigengap"

## DER Leaderboards


#### **1.NIST SRE 2000 CALLHOME Disk-8(LDC2001S97)**

Collar 0.25, No overlap for evaluation  
## Track 1: Oracle VAD  

| System and Error | DER,Speaker Error: Before Reseg | DER,Speaker Error: After Reseg |
| -------------------------------------------------------------|:------:|:------:|
| Callhome Diarization Xvector Model [6]                       | 8.39%  | -      |
| __Auto-Tuning NMESC [A1]__                                   | 7.29%  | -      |  
| __Auto-Tuning NMESC Implemented spectral_opt.py__            | 7.24%  | -      |   

## Track 2: System VAD  

| System and Error | Total Error: Before Reseg | Total Error: After Reseg  | Speaker Error: Before Reseg | Speaker Error: After Reseg|
| ------------------------------------------------------------|:------:|:------:|:--------:|:-----:|
| JHU, 2017, Garcia-Romero [1] (t1, Oracle SAD)               |        | -      | 12.8 %   | 9.9%  |
| Google, 2018, Quan Wang, d-vector + Spectral Clustering [3] | 18.8%  | -      | 12.0%    | -     |
| Google, 2019, Fully Supervised [4]                          | -      | -      | 7.6%     | -     |
| __Auto-Tuning NMESC [A1]__                                  | 11.73% |   -    | 5.41%    | -     |   

#### **2. DIHARD 2019 Dev Set**
192 Sessions  

No collar for evalutation  
Overlap regions are also evaluated  
  
## Track 1: Oracle VAD (Full DH2019 Dev set) 
Full dev set  
  
| System and Error | Total Error: Before Reseg | Total Error: After Reseg  | Speaker Error: Before Reseg | Speaker Error: After Reseg|
| ---------------------------------------------------------------|:------:|:------:|:--------:|:----:|
| __DiHard 2019 Baseline (JHU), (t1, test-set_opt, thres -0.03)__           | 24.24% | -      | 13.5%   | -     |
| USC t2D02_ahc_plda (_test-set opt._, thres +0.07)                         | 30.02% | 36.97% | 19.1%   | 16.1% |

## Track 2: System VAD (Full DH2019 Dev set)  

| System and Error | Total Error: Before Reseg | Total Error: After Reseg  | Speaker Error: Before Reseg | Speaker Error: After Reseg|
| ---------------------------------------------------------------|:------:|:------:|:--------:|:----:|
| __t2:DiHard 2019 Baseline (JHU) (t2, system SAD)__                     | -      | -     | -     | -     |
| USC t2D02_ahc_plda (_test-set opt._, thres -0.2)                       | 46.95% | 47.1% | 15.7% | 14.9% |
| USC t2D03_spt_cos (_test-set opt._, RP thres 0.08 for cos. sim. value) | -      | -     | -     | -     |   



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
| t2D02_spt_plda (KNOWN # of spks, LLR th 0.0 for raw PLDA)      | 5.61%  | 5.41%  | 1.3%   | 0.7%  |  


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


[A1] [Auto-Tuning Spectral Clustering for SpeakerDiarization Using Normalized Maximum Eigengap](https://drive.google.com/file/d/1CdEJPrpW6pRCObrppcZnw0_hRwWIHxi8/view?usp=sharing)

[1] [SPEAKER DIARIZATION USING DEEP NEURAL NETWORK EMBEDDINGS](https://www.danielpovey.com/files/2017_icassp_diarization_embeddings.pdf) - 9.9% DER on NIST SRE 2000 CH 

[2] [Priors for Speaker Counting and Diarization with AHC](https://engineering.jhu.edu/hltcoe/wp-content/uploads/sites/92/2016/10/Sell_McCree_Garcia-Romero_2016A.pdf) - Speaker prior method that is applied in [1]

[3] [SPEAKER DIARIZATION WITH LSTM](https://arxiv.org/pdf/1710.10468.pdf) - Google's 2018 Result with 12.0% DER on NIST SRE 2000 CH

[4] [FULLY SUPERVISED SPEAKER DIARIZATION](https://arxiv.org/pdf/1810.04719.pdf) - Google's latest result with 7.6% DER on NIST SRE 2000 CH (SoTA)

[5] [Speaker Diarization Using Convolutional Neural Network for Statistics Accumulation Refinement](https://www.isca-speech.org/archive/Interspeech_2017/pdfs/0051.PDF) - IBM's diarization paper that is tested on Callhome American English (LDC97S42) with CH-109 subset(2-speaker subset).

[6] [Kaldi-Callhome Diarization Xvector Model](https://david-ryan-snyder.github.io/2018/05/04/model_callhome_diarization_v2.html) 
