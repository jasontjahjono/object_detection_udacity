# Object Detection Writeup

1. **Project overview**: This section should contain a brief description of the project and what we are trying to achieve. Why is object detection such an important component of self-driving car systems?

In this project, we are doing object detection. This is important because we want to detect objects on the road from the background. We want to detect cars, bicyclist, pedestrians, and objects on the road so that our algorithm can avoid it.

1. **Set up**: This section should contain a brief description of the steps to follow to run the code for this repository.

I followed all the steps in the instructions. So first I used a pretrained fpn resnet model, and then I used it to train the waymo open dataset. I also changed some parts in the config file to fine-tune the parameters for better performance. Lastly, I did data augmentation to improve performance.

1. **Dataset**
    1. *Dataset Analysis*: This section should contain a quantitative and qualitative description of the dataset. It should include images, charts, and other visualizations.
    2. *Cross-validation*: This section should detail the cross-validation strategy and justify your approach.

The dataset contains images of streets with road users, completed with the bounding-box labels. Charts are attached in the project zip.

1. **Training**
    1. *Reference experiment*: This section should detail the results of the reference experiment. It should include training metrics, Tensorboard charts, and a detailed explanation of the algorithm's performance.
    2. *Improve on the reference*: This section should highlight the different strategies you adopted to improve your model. It should contain relevant figures and details of your findings.

The results of the reference experiments results in a very large loss. After 2500 steps, it resulted in a loss of 250, which or target should be below 1. However, after I changed the batch size to 4, the number of steps to 4000, the learning rate, and added data augmentations, the final result is below 1. The charts are attached in the project zip.