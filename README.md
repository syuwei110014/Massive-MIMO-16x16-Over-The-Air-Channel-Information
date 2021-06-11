# User Manual
This web page provides the measured channel matrices of the MIMO-OFDM system with 16 transmit antennas and 20 receiver antennas.
### 1. Frame Architecure
    1.1	Time & Frequency Domain Specification
    1.2	Noise Regularization
    1.3	Data Conversion Process
### 2. Scenarios Description
    2.1	Centralized Base Station + Non-Folding Terminal
    2.2	Distributed Base Station + Non-Folding Terminal
    2.3	Centralized Base Station + Folding Terminal
    2.2	Distributed Base Station + Folding Terminal
### 3. Operating Instructions
    3.1	Download the OTA measurement
    3.2	Channel Estimation
            3.2.1  Download Channel Estimation Package
            3.2.2  Get .dat Channel files by C language
            3.2.3  Get .mat Channel files from .dat Channel files by MATLAB
    3.3	Channel Access Format of .dat & .mat
            3.3.1  .dat Channel files Format
            3.3.2  .mat Channel files Format
****
# 1. Frame Architecure
## 1.1	Time & Frequency Domain Specification
  The OFDM system consists of 40 slots per frame, which have 560 symbols in total. Here, we take only eight slots per frame, 112 symbols, and each symbol contains 1620 sub-carriers.

<img src="https://user-images.githubusercontent.com/42632656/121650291-028f0a80-cacc-11eb-9674-201488cf8a3a.png" alt="Cover" width="67%"/><img src="https://user-images.githubusercontent.com/42632656/121650338-0e7acc80-cacc-11eb-807c-f6c277d56697.png" alt="Cover" width="33%"/>

Fig. 1. Time Domain Transmission Specification

## 1.2	Noise Regularization

## 1.3	Data Conversion Process
