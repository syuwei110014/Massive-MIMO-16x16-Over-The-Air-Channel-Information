# Outline
This web page provides the measured channel matrices of the MIMO-OFDM system with 16 transmit antennas and 20 receiver antennas.
#### 1. Frame Architecure
    1.1	Time & Frequency Domain Specification
    1.2	Noise Regularization
    1.3	Data Conversion Process
#### 2. Scenarios Description
    2.1	Centralized Base Station + Non-Folding Terminal
    2.2	Distributed Base Station + Non-Folding Terminal
    2.3	Centralized Base Station + Folding Terminal
    2.2	Distributed Base Station + Folding Terminal
#### 3. Operating Instructions
    3.1	Download the OTA measurement
    3.2	Channel Estimation
            3.2.1  Download Channel Estimation Package
            3.2.2  Get .dat Channel files by C language
            3.2.3  Get .mat Channel files from .dat Channel files by MATLAB
    3.3	Channel Access Format of .dat & .mat
            3.3.1  .dat Channel files Format
            3.3.2  .mat Channel files Format
****



# 1.  Frame Architecure
## 1.1  Time & Frequency Domain Specification
The OFDM system consists of 40 slots per frame, which have 560 symbols in total. Here, we take only eight slots per frame, 112 symbols, and each symbol contains 1620 sub-carriers.

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121650291-028f0a80-cacc-11eb-9674-201488cf8a3a.png" alt="Cover" width="67%"/><img src="https://user-images.githubusercontent.com/42632656/121650338-0e7acc80-cacc-11eb-807c-f6c277d56697.png" alt="Cover" width="33%"/>
</p>

<p align="center">
Fig. 1. Time Domain Transmission Specification
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121651386-243cc180-cacd-11eb-9d0d-23dd9e469b27.png" alt="Cover" width="67%"/>
</p>

<p align="center">
Fig. 2. Frequency Domain Specification
</p>

## 1.2  Noise Regularization
The received signal has already been regularized according to the noise level and is shown in Fig. 3. 
<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121651633-6a922080-cacd-11eb-8826-55c9bd9b7b84.png" alt="Cover" width="50%"/>

<p align="center">
Fig. 3. Regularized Received Signal
</p>

## 1.3  Data Conversion Process
For the detailed conversion process, please refer to Section 3. Fig. 4 shows the flow chart of the file transformation process. In the beginning, you’ll get *.dat format IQ data file after decompressing the downloaded data, this part show in Section 3.1. Then, we used C program to perform channel estimation and save the results as .dat format. Finally, we operate Matlab to convert them as .mat format, making it easier to use. The method to use the program is shown in Section 3.2. More detailed saving format description show in Section 3.3.

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121652227-03c13700-cace-11eb-910e-45c344671925.png" alt="Cover" width="75%"/>
</p>

<p align="center">
Fig. 4. Flow chart of file transformation process
</p>

****



# 2.  Scenarios Description
In this section, we shows the measurement scenarios.
## 2.1  Centralized Base Station + Non-Folding Terminal

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121652974-cad59200-cace-11eb-8be4-b95762503025.png" alt="Cover" width="75%"/>
    
<img src="https://user-images.githubusercontent.com/42632656/121652991-cf01af80-cace-11eb-90cf-eef942595797.png" alt="Cover" width="75%"/>
</p>

<p align="center">
Fig. 5. Measured environment with the centralized base station
</p>

## 2.2  Distributed Base Station + Non-Folding Terminal

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121653004-d32dcd00-cace-11eb-81f2-336b0449ab69.png" alt="Cover" width="75%"/>
    
<img src="https://user-images.githubusercontent.com/42632656/121653107-eb9de780-cace-11eb-9299-e073fe69a994.png" alt="Cover" width="75%"/>
</p>

<p align="center">
Fig. 6. Measured environment with the distributed base station
</p>

## 2.3  Centralized Base Station + Folding Terminal
<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121653132-efca0500-cace-11eb-9604-ea2c0ea02016.png" alt="Cover" width="75%"/>
    
<img src="https://user-images.githubusercontent.com/42632656/121653151-f2c4f580-cace-11eb-97c4-f3a31d27e98f.png" alt="Cover" width="75%"/>
</p>
<p align="center">
Fig. 7. Measured environment with the centralized base station
</p>

## 2.4  Distributed Base Station + Folding Terminal
<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121653167-f5bfe600-cace-11eb-8c07-9228af8a1ca1.png" alt="Cover" width="75%"/>
    
<img src="https://user-images.githubusercontent.com/42632656/121653169-f789a980-cace-11eb-9e68-9ded94d86004.png" alt="Cover" width="75%"/>
</p>

<p align="center">
Fig. 8. Measured environment with the distributed base station
</p>

****



# 3.  Operating Instructions
Section 3 will guide you on downloading the raw data file, transforming it to the channel matrices, and converting them into *.mat type (used by MATLAB). The user manual outline is as follows.
## 3.1  Download the OTA measurements
To download the original time-domain IQ compressed data, please link to the following link. Since the data is massive for each scenario, we partition the data into five parts (namely, part1, part2, …, part5 ).
<https://drive.google.com/drive/folders/19RdM7rw7qJ7H8oF_SvNw9flN1NMv1CTi?usp=sharing>

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121653837-af1ebb80-cacf-11eb-87c9-00f1f1f799e4.png" alt="Cover" width="50%"/>
</p>

<p align="center">
Fig. 9. Compressed Row IQ Data
</p>

Download the data of your desire scenario, and then decompress it to get the following IQ data files. Each scenario contains about 1000 records of the received signal, which is from iqdata1 to iqdata1000. Each record contains 20 Rx channels. All the data are stored in the time domain IQ data format. Iqdata1 represents the first record, ch20 represents the 20th Rx antenna of the first record.

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121654649-86e38c80-cad0-11eb-95e7-5c217b410f1c.png" alt="Cover" width="50%"/>
</p>

<p align="center">
Fig. 10. Decompressed Row IQ Data
</p>

## 3.2  Channel Estimation
### 3.2.1  Download Channel Estimation Package
Download the channel estimation file package, which is about 98 MB. Decompress it to get the following files.

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121654687-9236b800-cad0-11eb-9202-d0a629a8d6df.png" alt="Cover" width="20%"/>
</p>
<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121654698-94007b80-cad0-11eb-9333-6b04a2a29d43.png" alt="Cover" width="50%"/>
</p>

<p align="center">
Fig. 11. Channel Estimation Program Folder
</p>

(1)	Data contains the required parameters for the channel estimation.

(2)	HPDSCH folder puts the execution results, which is channel IQ data.

(3)	YPDSCH folder puts the data from 3.1. The data is shown in Fig. 12.

(4)	*.dll files are the needed utils for channel estimation. Since the Intel company provides the Math Kernel Library database, the computer CPU demands to be the Intel product.

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121654739-9ebb1080-cad0-11eb-8728-d9127886c047.png" alt="Cover" width="50%"/>
</p>

<p align="center">
Fig. 12. Put Depressed Row IQ Data in YPDSCH Folder
</p>

### 3.2.2  C Language Operating Instructions
After executing Channel_est.exe, enter two kinds of values.

(1)	Start from iqdata: represents to access channel from which records.

(2)	Num. of iqdata: represents the number of channels to be accessed.

Ensuring the YPDSCH folder contains the corresponding *.dat files to transform the data

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121654798-af6b8680-cad0-11eb-923e-617abb562a30.png" alt="Cover" width="20%"/>
</p>

<p align="center">   
<img src="https://user-images.githubusercontent.com/42632656/121654844-b98d8500-cad0-11eb-8f50-08b59a04ecb2.png" alt="Cover" width="75%"/>
</p>
<p align="center">
Fig. 13. Execute C Language Program Channel_est.exe
</p>
After finishing the execution, you can switch to the HPDSCH folder to capture the channel information. For the storage format, please take 3.4 for reference. The storage format can be further transformed into cell format from the Channel_est.m
<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121654923-cb6f2800-cad0-11eb-9808-a446653d42df.png" alt="Cover" width="50%"/>
</p>

<p align="center">
Fig. 14. Produce Channel Information Data in HPDSCH Folder
</p>

### 3.2.3  Matlab Operating Instructions
After executing Channel_est.exe, enter two kinds of values.

(1)	Start from iqdata : represents to access channel from which records.

(2)	Num. of iqdata : represents the number of channels to be accessed.

(3)	Num. of symbol : represents the number of symbols to be saved.

Ensuring the HPDSCH folder contains the corresponding *.dat files to transform the data
<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121655052-e5a90600-cad0-11eb-9b87-bcb5674b517f.png" alt="Cover" width="20%"/>
</p>

<p align="center"> 
<img src="https://user-images.githubusercontent.com/42632656/121655061-e8a3f680-cad0-11eb-96e4-6f168d4ec64e.png" alt="Cover" width="75%"/>
</p>
<p align="center">
Fig. 15. Execute Matlab Program Channel_est.m
</p>
It will display each record's execution time when running the program and then save the results to the HPDSCH_mat folder. Each record is saved in the cell format. The number of channels for each cell is 1620 multiply the number of symbols. The following takes 10 records as an example.
<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121655162-fa859980-cad0-11eb-8845-4db0236552a6.png" alt="Cover" width="20%"/>
</p>

<p align="center">  
<img src="https://user-images.githubusercontent.com/42632656/121655185-feb1b700-cad0-11eb-89f6-dc2c7a9923a0.png" alt="Cover" width="50%"/>
</p>
<p align="center">
Fig. 16. Produce Channel Information Data in HPDSCH_mat Folder
</p>

## 3.3  Channel Access Format
### 3.3.1  *.dat Channel Access Format
The channel information is accessible from the first piece of the first record of the terminal, arranged according to h_1,1, h_1,2, … h_1,16. The second piece immediately following the first piece, arranged as h_2,1, h_2,2, … h_2,16. The procedure is repeated to the 20th piece, arranged as h_20,1, h_20,2, … h_20,16. Each piece of channel information of each record contains 1620×112 sub-carriers, which are accessed in a vertical direction, arranged as sub-carrier-1, …, to sub-carrier-181439. Each sub-carrier contains two floating numbers, represent the real and imaginary number of the sub-carrier, respectively. In conclusion, each HPDSCH_iqdata1_ch storages 2×181440×16 = 5806080 floating numbers.

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121655216-04a79800-cad1-11eb-88c4-a7bce00b124c.png" alt="Cover" width="75%"/>
</p>

<p align="center">
Fig. 17. Channel Access Configuration Diagram
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121655226-0709f200-cad1-11eb-849c-dde579a32e1a.png" alt="Cover" width="50%"/>
</p>

<p align="center">
Fig. 18. MIMO System Diagram
</p>

### 3.3.2  .mat Channel Access Format
The vertical direction represents the 20 Rx antennas, while the horizontal direction represents the 16 Tx antennas. Each contains 1620×Num_of_symbol sub-carriers.
<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121655255-0b360f80-cad1-11eb-9cc2-c4aea3639a6d.png" alt="Cover" width="20%"/>
</p>

<p align="center"> 
<img src="https://user-images.githubusercontent.com/42632656/121655274-0e310000-cad1-11eb-9cf5-d1c9baf39c44.png" alt="Cover" width="75%"/>
</p>

<p align="center">
Fig. 19. Channel Access Configuration Diagram
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/42632656/121655282-0ffac380-cad1-11eb-8850-d723d20ee747.png" alt="Cover" width="50%"/>
</p>

<p align="center">
Fig. 20. MIMO System Diagram
</p>

# License
(c) 2021 Chen-Wei Syu, Chao-Kai Wen

(c) e-mail: syuwei110014@gmail.com, chaokai.wen@mail.nsysu.edu.tw

@InProceedings{xxxxx, 
author={Chen-Wei Syu},
title={Adaptive Dynamic Hypernet for Parameter Optimization of Multi-Input Multi-Output Detector},
booktitle ={Unpublished doctoral dissertation},
year={2021},
month={Jul},
Address={National Sun Yat-sen University CTLAB, Taiwan},
}
