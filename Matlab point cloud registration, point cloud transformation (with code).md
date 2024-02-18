#  I. Overview 

##  1. Algorithm overview 

   PCtransform: 3D point cloud transformation 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957455630
  ```  
 The transformation matrix applied to the point cloud, the transformation matrix may be a rigid body transformation may be an affine transformation. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957455630
  ```  
 Apply a displacement field D to the point cloud. Transform each point in the point cloud using the translation defined by the displacement field. 

#  Second, rigid transformation 

##  1. Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957455630
  ```  
##  2. Results display 

 ![avatar]( 4d3504f3448d488bae5f0860e03d4ab5.png) 

#  III. Affine transformation 

##  1. Code example 

   This example shows an affine transformation of a three-dimensional point cloud. The specified forward transformation can be either rigid or non-rigid. The transformation shown includes rotation (rigid transformation) and shear (non-rigid transformation) of the input point cloud. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957455630
  ```  
##  2. Results display 

 ![avatar]( 4458df063f924b24a2b2d4cf3d1e07d7.png) 

#  Point cloud transformation based on displacement field 

##  1. Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957455630
  ```  
##  2. Results display 

 ![avatar]( df7de29fc2d04ec99be38158caa252bc.png) 

#  Parameter analysis 

##  input parameter 

##  output parameter 

#  VI. Reference link 

>  Matlab point cloud toolbox - pctransform 

#  Seven, warning!!! 

   The rigid3d function is a new function in matlab 2020a and above, so why do some bosses make mistakes?? Why ask??????  

