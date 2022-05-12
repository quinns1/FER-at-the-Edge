
Facial Emotion Recognition at the Edge
---------------------------------------------

High level ML architecture for work carried out in this project visualised below.

![plot](./images/ML_Architecture.png)

**Face detection**

2 baseline CNN based models were built using tensorflow. 

**Model Compression**

*Quantization*
Various permutations of quantization and pruning were incorporated and evaluated in terms of top-1 accuracy, latency and model size. The best performing model was retained and deployed to an edge device (Raspberry Pi).

*Pruning*
Utilizing 2 by 4 structured pruning with FLOAT16 Quantization yielded a x6 reduction in model size, x6.3 reduction in latency with a 2.5% trade-off in accuracy



**Face detection**
We investigate a number of face detection methods including Viola Jones, HOG/SVM & MTCNN. For deployment on low-cost edge device (Raspberry Pi), lowest latencies were found using Viola Jones method for face detection.


Edge-FER implementation runs at 5.4FPS with face detection on edge device.
