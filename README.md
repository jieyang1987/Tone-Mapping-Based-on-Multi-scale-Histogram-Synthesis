# Tone-Mapping-Based-on-Multi-scale-Histogram-Synthesis

The following image-table show tone mapped images with different tone mapping operators. The operators are: 

- Durand TMO: Durand, Frédo, and Julie Dorsey. "Fast bilateral filtering for the display of high-dynamic-range images." *ACM transactions on graphics (TOG)*. Vol. 21. No. 3. ACM, 2002.
- Gu TMO:   Gu, Bo, et al. "Local edge-preserving multiscale decomposition for high dynamic range image tone mapping." *IEEE Transactions on image Processing* 22.1 (2012): 70-79.
- Paris TMO: Paris, Sylvain, Samuel W. Hasinoff, and Jan Kautz. "Local Laplacian filters: edge-aware image processing with a Laplacian pyramid." *Communications of the ACM* 58.3 (2015): 81-91.
- Mantiuk TMO: Mantiuk, Rafał, Scott Daly, and Louis Kerofsky. "Display adaptive tone mapping." *ACM Transactions on Graphics (TOG)*. Vol. 27. No. 3. ACM, 2008.
- iCAM06 TMO: Kuang, Jiangtao, Garrett M. Johnson, and Mark D. Fairchild. "iCAM06: A refined image appearance model for HDR image rendering." *Journal of Visual Communication and Image Representation* 18.5 (2007): 406-414.
- Proposed multi-scale histogram synthesis algorithm



|                         Durand TMO                         |                       Gu TMO                       |                        Paris TMO                         |                       Mantiuk TMO                       |                 iCAM06 TMO                 |                 Proposed                 |
| :--------------------------------------------------------: | :------------------------------------------------: | :------------------------------------------------------: | :-----------------------------------------------------: | :----------------------------------------: | :--------------------------------------: |
| ![Durand](./images/AtriumMorning/AtriumMorning_durand.jpg) | ![Gu](./images/AtriumMorning/AtriumMorning_Gu.jpg) | ![Paris](./images/AtriumMorning/AtriumMorning_paris.jpg) | ![](./images/AtriumMorning/AtriumMorning_mantiuk08.jpg) |   ![](./images/AtriumMorning/icam06.jpg)   | ![Ours](./images/AtriumMorning/Ours.png) |
|            ![](./images/AtriumNight/durand.jpg)            |          ![](./images/AtriumNight/gu.jpg)          |           ![](./images/AtriumNight/paris.jpg)            |          ![](./images/AtriumNight/mantiuk.jpg)          |    ![](./images/AtriumNight/icam06.jpg)    |    ![](./images/AtriumNight/ours.png)    |
|              ![](./images/belgium/durand.jpg)              |            ![](./images/belgium/Gu.jpg)            |             ![](./images/belgium/paris.jpg)              |            ![](./images/belgium/mantiuk.jpg)            |      ![](./images/belgium/icam06.jpg)      |      ![](./images/belgium/ours.png)      |
|             ![](./images/cathedral/durand.jpg)             |           ![](./images/cathedral/gu.jpg)           |            ![](./images/cathedral/paris.jpg)             |           ![](./images/cathedral/mantiuk.jpg)           |     ![](./images/cathedral/icam06.jpg)     |     ![](./images/cathedral/ours.png)     |
|             ![](./images/crowfoot/durand.jpg)              |           ![](./images/crowfoot/gu.jpg)            |             ![](./images/crowfoot/paris.jpg)             |           ![](./images/crowfoot/mantiuk.jpg)            |     ![](./images/crowfoot/icam06.jpg)      |     ![](./images/crowfoot/ours.png)      |
|           ![](./images/designCenter/durand.jpg)            |         ![](./images/designCenter/gu.jpg)          |           ![](./images/designCenter/paris.jpg)           |         ![](./images/designCenter/mantiuk.jpg)          |   ![](./images/designCenter/icam06.jpg)    |   ![](./images/designCenter/ours.png)    |
|              ![](./images/garage/durand.jpg)               |            ![](./images/garage/gu.jpg)             |              ![](./images/garage/paris.jpg)              |            ![](./images/garage/mantiuk.jpg)             |      ![](./images/garage/icam06.jpg)       |      ![](./images/garage/ours.png)       |
|               ![](images\groveD\durand.jpg)                |             ![](images\groveD\gu.jpg)              |               ![](images\groveD\paris.jpg)               |             ![](images\groveD\mantiuk.jpg)              |       ![](images\groveD\icam06.jpg)        |       ![](images\groveD\ours.png)        |
|             ![](./images/memorial/durand.jpg)              |           ![](./images/memorial/gu.jpg)            |             ![](./images/memorial/paris.jpg)             |           ![](./images/memorial/mantiuk.jpg)            |     ![](./images/memorial/icam06.jpg)      |     ![](./images/memorial/ours.png)      |
|              ![](images/Moraine1/durand.jpg)               |            ![](images/Moraine1/gu.jpg)             |              ![](images/Moraine1/paris.jpg)              |            ![](images/Moraine1/mantiuk.jpg)             |      ![](images/Moraine1/icam06.jpg)       |      ![](images/Moraine1/ours.png)       |
|              ![](images/Moraine2/durand.jpg)               |            ![](images/Moraine2/gu.jpg)             |              ![](images/Moraine2/paris.jpg)              |            ![](images/Moraine2/mantiuk.jpg)             |      ![](images/Moraine2/icam06.jpg)       |      ![](images/Moraine2/ours.png)       |
|               ![](./images/moto/durand.jpg)                |             ![](./images/moto/gu.jpg)              |               ![](./images/moto/paris.jpg)               |             ![](./images/moto/mantiuk.jpg)              |       ![](./images/moto/icam06.jpg)        |       ![](./images/moto/ours.png)        |
|         ![](./images/nancy_cathedral_2/durand.jpg)         |       ![](./images/nancy_cathedral_2/gu.jpg)       |        ![](./images/nancy_cathedral_2/paris.jpg)         |       ![](./images/nancy_cathedral_2/mantiuk.jpg)       | ![](./images/nancy_cathedral_2/icam06.jpg) | ![](./images/nancy_cathedral_2/ours.png) |
|               ![](./images/orion/durand.jpg)               |             ![](./images/orion/gu.jpg)             |              ![](./images/orion/paris.jpg)               |             ![](./images/orion/mantiuk.jpg)             |       ![](./images/orion/icam06.jpg)       |       ![](./images/orion/ours.png)       |
|              ![](./images/rend01/durand.jpg)               |            ![](./images/rend01/gu.jpg)             |              ![](./images/rend01/paris.jpg)              |            ![](./images/rend01/mantiuk.jpg)             |      ![](./images/rend01/icam06.jpg)       |      ![](./images/rend01/ours.png)       |
|             ![](./images/Rockies3b/durand.jpg)             |           ![](./images/Rockies3b/gu.jpg)           |            ![](./images/Rockies3b/paris.jpg)             |           ![](./images/Rockies3b/mantiuk.jpg)           |     ![](./images/Rockies3b/icam06.jpg)     |     ![](./images/Rockies3b/ours.png)     |
|             ![](./images/tinterna/durand.jpg)              |           ![](./images/tinterna/gu.jpg)            |             ![](./images/tinterna/paris.jpg)             |           ![](./images/tinterna/mantiuk.jpg)            |     ![](./images/tinterna/icam06.jpg)      |     ![](./images/tinterna/ours.png)      |
|                ![](./images/tmN/durand.jpg)                |              ![](./images/tmN/gu.jpg)              |               ![](./images/tmN/paris.jpg)                |              ![](./images/tmN/mantiuk.jpg)              |        ![](./images/tmN/icam06.jpg)        |        ![](./images/tmN/ours.png)        |
|            ![](./images/Vernicular/durand.jpg)             |          ![](./images/Vernicular/gu.jpg)           |            ![](./images/Vernicular/paris.jpg)            |          ![](./images/Vernicular/mantiuk.jpg)           |    ![](./images/Vernicular/icam06.jpg)     |    ![](./images/Vernicular/ours.png)     |
|            ![](./images/vinesunset/durand.jpg)             |          ![](./images/vinesunset/gu.jpg)           |            ![](./images/vinesunset/paris.jpg)            |          ![](./images/vinesunset/mantiuk.jpg)           |    ![](./images/vinesunset/icam06.jpg)     |    ![](./images/vinesunset/ours.png)     |







