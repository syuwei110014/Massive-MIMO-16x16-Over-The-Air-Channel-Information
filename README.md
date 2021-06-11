# User Manual
This web page provides the measured channel matrices of the MIMO-OFDM system with 16 transmit antennas and 20 receiver antennas.
### 1) Frame Architecure
    1.1	Time & Frequency Domain Specification
    1.2	Noise Regularization
    1.3	Data Conversion Process
### 2) Scenarios Description
    2.1	Centralized Base Station + Non-Folding Terminal
    2.2	Distributed Base Station + Non-Folding Terminal
    2.3	Centralized Base Station + Folding Terminal
    2.2	Distributed Base Station + Folding Terminal
### 3) Operating Instructions
    3.1	Download the OTA measurement
    3.2	Channel Estimation
            3.2.1  Download Channel Estimation Package
            3.2.2  Get .dat Channel files by C language
            3.2.3  Get .mat Channel files from .dat Channel files by MATLAB
    3.3	Channel Access Format of .dat & .mat
            3.3.1  .dat Channel files Format
            3.3.2  .mat Channel files Format
****



# 1) Frame Architecure
## 1.1	Time & Frequency Domain Specification
  The OFDM system consists of 40 slots per frame, which have 560 symbols in total. Here, we take only eight slots per frame, 112 symbols, and each symbol contains 1620 sub-carriers.

<img src="https://user-images.githubusercontent.com/42632656/121650291-028f0a80-cacc-11eb-9674-201488cf8a3a.png" alt="Cover" width="67%"/><img src="https://user-images.githubusercontent.com/42632656/121650338-0e7acc80-cacc-11eb-807c-f6c277d56697.png" alt="Cover" width="33%"/>

Fig. 1. Time Domain Transmission Specification

<img src="https://user-images.githubusercontent.com/42632656/121651386-243cc180-cacd-11eb-9d0d-23dd9e469b27.png" alt="Cover" width="67%"/>

Fig. 2. Frequency Domain Specification

## 1.2	Noise Regularization
  The received signal has already been regularized according to the noise level and is shown in Fig. 3. 

<img src="https://user-images.githubusercontent.com/42632656/121651633-6a922080-cacd-11eb-8826-55c9bd9b7b84.png" alt="Cover" width="50%"/>

Fig. 3. Regularized Received Signal
## 1.3	Data Conversion Process
  For the detailed conversion process, please refer to Section 3. Fig. 4 shows the flow chart of the file transformation process. In the beginning, you’ll get *.dat format IQ data file after decompressing the downloaded data, this part show in Section 3.1. Then, we used C program to perform channel estimation and save the results as .dat format. Finally, we operate Matlab to convert them as .mat format, making it easier to use. The method to use the program is shown in Section 3.2. More detailed saving format description show in Section 3.3.

<img src="https://user-images.githubusercontent.com/42632656/121652227-03c13700-cace-11eb-910e-45c344671925.png" alt="Cover" width="75%"/>

Fig. 4. Flow chart of file transformation process
****



# 2) Scenarios Description
In this section, we shows the measurement scenarios.
## 2.1	Centralized Base Station + Non-Folding Terminal

<img src="https://user-images.githubusercontent.com/42632656/121652974-cad59200-cace-11eb-8be4-b95762503025.png" alt="Cover" width="75%"/>
<img src="https://user-images.githubusercontent.com/42632656/121652991-cf01af80-cace-11eb-90cf-eef942595797.png" alt="Cover" width="75%"/>

Fig. 5. Measured environment with the centralized base station

## 2.2	Distributed Base Station + Non-Folding Terminal

<img src="https://user-images.githubusercontent.com/42632656/121653004-d32dcd00-cace-11eb-81f2-336b0449ab69.png" alt="Cover" width="75%"/>
<img src="https://user-images.githubusercontent.com/42632656/121653107-eb9de780-cace-11eb-9299-e073fe69a994.png" alt="Cover" width="75%"/>

Fig. 5. Measured environment with the centralized base station

## 2.3	Centralized Base Station + Folding Terminal

<img src="https://user-images.githubusercontent.com/42632656/121653132-efca0500-cace-11eb-9604-ea2c0ea02016.png" alt="Cover" width="75%"/>
<img src="https://user-images.githubusercontent.com/42632656/121653151-f2c4f580-cace-11eb-97c4-f3a31d27e98f.png" alt="Cover" width="75%"/>

Fig. 5. Measured environment with the centralized base station

## 2.2	Distributed Base Station + Folding Terminal

<img src="https://user-images.githubusercontent.com/42632656/121653167-f5bfe600-cace-11eb-8c07-9228af8a1ca1.png" alt="Cover" width="75%"/>
<img src="https://user-images.githubusercontent.com/42632656/121653169-f789a980-cace-11eb-9e68-9ded94d86004.png" alt="Cover" width="75%"/>

Fig. 5. Measured environment with the centralized base station













