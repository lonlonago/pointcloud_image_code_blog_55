#  I. Overview 

##  1. Algorithm overview 

   projectLidarPointsOnImage: Projecting LiDAR point cloud data onto an image coordinate system 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574519789
  ```  
 Using a rigid conversion tform between the lidar sensor and the camera, and a set of intrinsic parameters from the camera, the lidar point cloud data is projected onto the image coordinate frame. The output imPts contain the 2d coordinates of the projected points in the image frame. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574519789
  ```  
 The LIDAR point (designated as the three-dimensional coordinate in the world coordinate system) is projected onto the image coordinate system. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574519789
  ```  
 Returns the linear index of the projected points in the point cloud using any combination of the input parameters in the previous syntax. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574519789
  ```  
 In addition to the parameter combinations in the previous syntax, you specify options for parameters using one or more name-values. For example, 'ImageSize', [250, 400] sets the size of the image on which you want to project points to 250 x 400 pixels. 

#  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574519789
  ```  
#  III. Display of results 

 ![avatar]( 8a223900571d461c92ff3f25e435f4be.png) 

#  IV. Parameter analysis 

##  input parameter 

##  Name-value corresponding parameter 

##  output parameter 

#  V. Reference links 

 Matlab Point Cloud Toolbox - projectLidarPointsOnImage 

