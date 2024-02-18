#  Function overview 

##  1. Algorithm overview 

   The phase correlation method is used to register the two point clouds. See the paper for more details: 

>  [1] Dimitrievski M , Hamme D V , Veelaert P , et al. Robust Matching of Occupancy Maps for Odometry in Autonomous Vehicles[C]// International Conference on Computer Vision Theory & Applications. 2016. 

##  2. Main functions 

 Overloaded function 1: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574566945
  ```  
   Two point clouds are registered using a phase correlation algorithm. The function first performs registration by converting the two point clouds into two-dimensional occupancy grids on the X-Y plane centered on the origin (0, 0, 0). The occupancy of each grid cell is determined by the z-coordinate values of points within the grid. Overload Function 2: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574566945
  ```  
   Returns the registration error, overloaded function 3: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574566945
  ```  
   Returns the peak correlation value of the phase difference of two occupied grids. Overload function 4: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574566945
  ```  
   The return value corresponds to the content of the parameter. 

#  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574566945
  ```  
#  III. Display of results 

 ![avatar]( 33428c583c1f426b941d618a02765448.png) 

#  IV. Parameter analysis 

##  input parameter 

##  Name-value corresponding parameter 

##  output parameter 

 Tips: 

>  When the transformation can be described in terms of translation of the X-Y plane and rotation of the z-axis, the phase correlation method is most suitable for registering point clouds. For example, a ground vehicle moves with a horizontally mounted lidar on a flat surface. The phase correlation algorithm expects the motion to only follow the X-Y plane, just like the ground plane. If the motion is not in the X-Y plane, the normalRotation function can be used to transform the point cloud. For example, in vehicle motion, the effect of vehicle suspension or pavement features such as potholes and speed bumps can be reduced by using the normalRotation function. Increasing the size of the occupied mesh increases the computational requirements of this function. The size of the occupied mesh can be controlled by modifying the gridSize and gridStep parameters. 4. If the registration result is poor and the peak correlation value is less than 0.03, try setting the Window parameter to false. 

#  V. Reference links 

 Matlab point cloud toolbox - pcregistercorr 

