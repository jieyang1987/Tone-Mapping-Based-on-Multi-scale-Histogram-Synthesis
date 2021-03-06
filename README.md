# Tone Mapping Based on Multi-scale Histogram Synthesis

### Introduction

**MSHIST** is a wide dynamic range tone mapping algorithm developed by [**I2Sense Lab**](<https://www.ucalgary.ca/i2sense/>) of [**University of Calgary**](<https://www.ucalgary.ca/>). our algorithm uses functions built upon different scales to tone map pixels to different values. Functions of large scales are used to maintain image brightness consistency and functions of small scales are used to preserve local detail and contrast. An efficient method using local variance has been proposed to fuse the values of different scales and to remove artifacts. The algorithm utilizes integral images and integral histograms to reduce computation complexity and processing time. Experimental results show that the proposed algorithm can generate high brightness, good contrast and appealing images that surpass the performance of many state-of-the-art tone mapping algorithms.

### HDR image rendering examples and comparison 

The following image-table shows tone mapped images with different tone mapping operators. The operators are: 

- **Durand TMO**: Durand, Frédo, and Julie Dorsey. "Fast bilateral filtering for the display of high-dynamic-range images." *ACM transactions on graphics (TOG)*. Vol. 21. No. 3. ACM, 2002.
- **Gu TMO**:   Gu, Bo, et al. "Local edge-preserving multiscale decomposition for high dynamic range image tone mapping." *IEEE Transactions on image Processing* 22.1 (2012): 70-79.
- **Paris TMO**: Paris, Sylvain, Samuel W. Hasinoff, and Jan Kautz. "Local Laplacian filters: edge-aware image processing with a Laplacian pyramid." *Communications of the ACM* 58.3 (2015): 81-91.
- **Mantiuk TMO**: Mantiuk, Rafał, Scott Daly, and Louis Kerofsky. "Display adaptive tone mapping." *ACM Transactions on Graphics (TOG)*. Vol. 27. No. 3. ACM, 2008.
- **iCAM06 TMO**: Kuang, Jiangtao, Garrett M. Johnson, and Mark D. Fairchild. "iCAM06: A refined image appearance model for HDR image rendering." *Journal of Visual Communication and Image Representation* 18.5 (2007): 406-414.
- **Proposed**: Multi-scale histogram synthesis algorithm.

The corresponding HDR file can be downloaded [here](./HDR_files)

|                  Durand TMO                  |                 Gu TMO                 |                 Paris TMO                  |                 Mantiuk TMO                 |                 iCAM06 TMO                 |                 Proposed                 |
| :------------------------------------------: | :------------------------------------: | :----------------------------------------: | :-----------------------------------------: | :----------------------------------------: | :--------------------------------------: |
| ![Durand](./images/AtriumMorning/durand.jpg) |  ![Gu](./images/AtriumMorning/gu.jpg)  | ![Paris](./images/AtriumMorning/paris.jpg) |   ![](./images/AtriumMorning/mantiuk.jpg)   |   ![](./images/AtriumMorning/icam06.jpg)   | ![Ours](./images/AtriumMorning/Ours.png) |
|     ![](./images/AtriumNight/durand.jpg)     |    ![](./images/AtriumNight/gu.jpg)    |    ![](./images/AtriumNight/paris.jpg)     |    ![](./images/AtriumNight/mantiuk.jpg)    |    ![](./images/AtriumNight/icam06.jpg)    |    ![](./images/AtriumNight/ours.png)    |
|       ![](./images/belgium/durand.jpg)       |      ![](./images/belgium/Gu.jpg)      |      ![](./images/belgium/paris.jpg)       |      ![](./images/belgium/mantiuk.jpg)      |      ![](./images/belgium/icam06.jpg)      |      ![](./images/belgium/ours.png)      |
|      ![](./images/cathedral/durand.jpg)      |     ![](./images/cathedral/gu.jpg)     |     ![](./images/cathedral/paris.jpg)      |     ![](./images/cathedral/mantiuk.jpg)     |     ![](./images/cathedral/icam06.jpg)     |     ![](./images/cathedral/ours.png)     |
|      ![](./images/crowfoot/durand.jpg)       |     ![](./images/crowfoot/gu.jpg)      |      ![](./images/crowfoot/paris.jpg)      |     ![](./images/crowfoot/mantiuk.jpg)      |     ![](./images/crowfoot/icam06.jpg)      |     ![](./images/crowfoot/ours.png)      |
|    ![](./images/designCenter/durand.jpg)     |   ![](./images/designCenter/gu.jpg)    |    ![](./images/designCenter/paris.jpg)    |   ![](./images/designCenter/mantiuk.jpg)    |   ![](./images/designCenter/icam06.jpg)    |   ![](./images/designCenter/ours.png)    |
|       ![](./images/garage/durand.jpg)        |      ![](./images/garage/gu.jpg)       |       ![](./images/garage/paris.jpg)       |      ![](./images/garage/mantiuk.jpg)       |      ![](./images/garage/icam06.jpg)       |      ![](./images/garage/ours.png)       |
|       ![](./images/groveD/durand.jpg)        |      ![](./images/groveD/gu.jpg)       |       ![](./images/groveD/paris.jpg)       |      ![](./images/groveD/mantiuk.jpg)       |      ![](./images/groveD/icam06.jpg)       |      ![](./images/groveD/ours.png)       |
|      ![](./images/memorial/durand.jpg)       |     ![](./images/memorial/gu.jpg)      |      ![](./images/memorial/paris.jpg)      |     ![](./images/memorial/mantiuk.jpg)      |     ![](./images/memorial/icam06.jpg)      |     ![](./images/memorial/ours.png)      |
|       ![](images/Moraine1/durand.jpg)        |      ![](images/Moraine1/gu.jpg)       |       ![](images/Moraine1/paris.jpg)       |      ![](images/Moraine1/mantiuk.jpg)       |      ![](images/Moraine1/icam06.jpg)       |      ![](images/Moraine1/ours.png)       |
|       ![](images/Moraine2/durand.jpg)        |      ![](images/Moraine2/gu.jpg)       |       ![](images/Moraine2/paris.jpg)       |      ![](images/Moraine2/mantiuk.jpg)       |      ![](images/Moraine2/icam06.jpg)       |      ![](images/Moraine2/ours.png)       |
|        ![](./images/moto/durand.jpg)         |       ![](./images/moto/gu.jpg)        |        ![](./images/moto/paris.jpg)        |       ![](./images/moto/mantiuk.jpg)        |       ![](./images/moto/icam06.jpg)        |       ![](./images/moto/ours.png)        |
|  ![](./images/nancy_cathedral_2/durand.jpg)  | ![](./images/nancy_cathedral_2/gu.jpg) | ![](./images/nancy_cathedral_2/paris.jpg)  | ![](./images/nancy_cathedral_2/mantiuk.jpg) | ![](./images/nancy_cathedral_2/icam06.jpg) | ![](./images/nancy_cathedral_2/ours.png) |
|        ![](./images/orion/durand.jpg)        |       ![](./images/orion/gu.jpg)       |       ![](./images/orion/paris.jpg)        |       ![](./images/orion/mantiuk.jpg)       |       ![](./images/orion/icam06.jpg)       |       ![](./images/orion/ours.png)       |
|       ![](./images/rend01/durand.jpg)        |      ![](./images/rend01/gu.jpg)       |       ![](./images/rend01/paris.jpg)       |      ![](./images/rend01/mantiuk.jpg)       |      ![](./images/rend01/icam06.jpg)       |      ![](./images/rend01/ours.png)       |
|      ![](./images/Rockies3b/durand.jpg)      |     ![](./images/Rockies3b/gu.jpg)     |     ![](./images/Rockies3b/paris.jpg)      |     ![](./images/Rockies3b/mantiuk.jpg)     |     ![](./images/Rockies3b/icam06.jpg)     |     ![](./images/Rockies3b/ours.png)     |
|      ![](./images/tinterna/durand.jpg)       |     ![](./images/tinterna/gu.jpg)      |      ![](./images/tinterna/paris.jpg)      |     ![](./images/tinterna/mantiuk.jpg)      |     ![](./images/tinterna/icam06.jpg)      |     ![](./images/tinterna/ours.png)      |
|         ![](./images/tmN/durand.jpg)         |        ![](./images/tmN/gu.jpg)        |        ![](./images/tmN/paris.jpg)         |        ![](./images/tmN/mantiuk.jpg)        |        ![](./images/tmN/icam06.jpg)        |        ![](./images/tmN/ours.png)        |
|     ![](./images/Vernicular/durand.jpg)      |    ![](./images/Vernicular/gu.jpg)     |     ![](./images/Vernicular/paris.jpg)     |    ![](./images/Vernicular/mantiuk.jpg)     |    ![](./images/Vernicular/icam06.jpg)     |    ![](./images/Vernicular/ours.png)     |
|     ![](./images/vinesunset/durand.jpg)      |    ![](./images/vinesunset/gu.jpg)     |     ![](./images/vinesunset/paris.jpg)     |    ![](./images/vinesunset/mantiuk.jpg)     |    ![](./images/vinesunset/icam06.jpg)     |    ![](./images/vinesunset/ours.png)     |



### Download:

To obtain the code, you can:

Contact  [**Prof. Yadid-Pecht**](<https://www.ucalgary.ca/i2sense/yadid_pecht_biography>) at **orly.yadid-pecht at ucalgary dot ca**. Please note that you will have to fill and sign a Terms of Use agreement in order to proceed to download.



### Contact:

Please contact [**Prof. Yadid-Pecht**](<https://www.ucalgary.ca/i2sense/yadid_pecht_biography>) or [**Dr. Jie Yang**](<https://jieyang1987.github.io/>) for any issue regarding the algorithm

Email: orly dot yadid-pecht at ucalgary dot ca; yangjie at westlake dot edu dot cn



### Dependency:

1. Matlab R2018a

2. Matlab HDR tool box (https://github.com/banterle/HDR_Toolbox)

3. Matlab Vlfeat tool box (http://www.vlfeat.org/index.html)

4. Openexr (<http://www.openexr.com/>, optional)



### Citation and Reference

This work is first published in the following conference in 2017 IEEE International Workshop on Computational Advances in Multi-Sensor Adaptive Processing (CAMSAP)

[Multi-Scale histogram tone mapping algorithm for display of wide dynamic range images](<https://ieeexplore.ieee.org/abstract/document/8313070/>)

If you find this work useful for your research please cite:

```
@inproceedings{yang2017multi,
  title={Multi-Scale histogram tone mapping algorithm for display of wide dynamic range images},
  author={Yang, Jie and Hore, Alain and Shahnovich, Ulian and Yadid-Pecht, Orly},
  booktitle={2017 IEEE 7th International Workshop on Computational Advances in Multi-Sensor Adaptive Processing (CAMSAP)},
  pages={1--5},
  year={2017},
  organization={IEEE}
}
```