# Restoring Ancient Painting
## Description 
--------------------------------------------------------------------------------------
An image was given that is related to the ancient art. The image is dark, blur and unclear, therefore, the issue for this
challenge is to use image processing techniques to improve the visual appearance of the art. 

Image Provided : 
![Challenge1_qingmingShanghe](https://github.com/eethiing/Restoring-Ancient-Painting/assets/85276977/4c10b681-6504-40a4-bfdd-47ba9db510e6)

## Techniques Applied
-----------------------------------------------------------------------------------
### 1st Strategy
The first strategy was to apply two times of sharpening filter on the original
image to enhance the output of the image quality and one time of bilateral filter on the
sharpened image to remove the noise. For this process, a kernel is needed to be used on the
image. The kernel for sharpening is [ [0,-1,0] [-1,5,-1] [0,-1,0] ]. The output of the
first sharpening has improved the visual appearance of the image but it is still blurry.
Therefore, sharpening filter was applied again on the sharpened image. To remove the noise of the sharpened image,  a smoothing filter known as bilateral filter is used. The reason the filter is picked because it will try to
preserve the edges as compared to the median blur and blur filters. The output can be seen in the figure below. 

![image](https://github.com/eethiing/Restoring-Ancient-Painting/assets/85276977/7cc780d5-55a5-4e6f-81e9-8a631e9f47a6)

### 2nd Strategy
The second strategy tested was by using laplacian filter to remove the noise on the
original image, followed by sharpening filter using the kernel. The laplacian
filter is used to detect the blurry edges in the original image. Once the blurry edges are
gotten, the original image will be used to minus out the blurry edges that were detected. The output of the image is an enhanced and brighter image as compared to
the original image. However, there are still some blurriness on the enhanced image.
Therefore, sharpening kernel was applied on the enhanced image and the output
can be seen below.

![image](https://github.com/eethiing/Restoring-Ancient-Painting/assets/85276977/baf6ebed-9564-452d-80b4-f16d336ba6f2)
