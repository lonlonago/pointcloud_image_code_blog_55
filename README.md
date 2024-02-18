#  I. Overview 

##  1. Preface 

    There are ready-made call functions in matlab that can directly realize the construction of rotation matrices, such as rotating 30 ° around the x-axis, rotating 1 ° around the y-axis, first rotating around the x-axis, then rotating around z, and finally rotating around y and a series of basic operations. It's a matter of one line of code, and there is no need to write a fancy implementation process according to the formula. The purpose of using tools is to simplify complex problems. If you have to show your strong mathematical skills, wouldn't it be more advanced to do it by hand? 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574554216
  ```  
    Create a matrix for the angle of rotation of the vector or matrix around the axis (in angles, not radians). 

 When operating on a matrix, each column of the matrix represents a different vector. For rotation matrices and vectors, the rotation vector is given by. Similarly, the function of rotation around the y-axis is: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574554216
  ```  
 The function of rotation around the z-axis is: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574554216
  ```  
#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574554216
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574554216
  ```  


--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Implementation process 

   If the target point set corresponds to the reference point set, the corresponding points are satisfied: the number of points in the two point sets is equal, and the points in the point sets should correspond one-to-one. Let the rotation transformation vector be a unit quaternion: the rotation matrix can be obtained. Let the translation transformation vector be: the complete coordinate transformation vector can be obtained. Then the problem of finding the best coordinate transformation vector between the corresponding point sets can be transformed into the problem of getting a function: minimization. In the unit quaternion method, at least 3 pairs of coordinates of one-to-one corresponding points need to be known. The algorithm process is as follows: 1. Find the center of gravity respectively. The center of gravity of the original point is: After the conversion, the center of gravity of the point is: where, there is a pair of corresponding points, which 2. The constructed covariance matrix is: 3. The constructed matrix is: where, is the trace of the matrix; is, the identity matrix; is: where,. 4. Calculate the eigenvalue and eigenvector of the matrix, where the eigenvector corresponding to the largest eigenvalue is the unit quaternion. 5. Calculate the rotation matrix as: where, 6. Calculate the translation matrix as:  

##  2. References 

 [1]滕志远,张爱武.单位四元素法在激光点云坐标转换中的应用[J].测绘通报,2010(11):7-10.  

##  3. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574563595
  ```  
 Quaternion to Rotation Matrix 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574563595
  ```  
#  III. Display of results 

 ![avatar]( 93910a84fa454170b060795c446f2800.png) 

#  IV. Reference link 

 quat2dcm 

#  Test data 

 The test data is generated by MATLAB code, which is as follows: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574563595
  ```  


--------------------------------------------------------------------------------

#  I. Overview 

   See: matlab point cloud random coloring 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574538941
  ```  
#  III. Display of results 

 ![avatar]( 00793ffaf9254fbba12639f51a5a62ba.png) 

 Red, purple, green.  



--------------------------------------------------------------------------------

#  First, statistical filtering 

##  1. Algorithm principle 

   Statistical analysis of the neighborhood of each point assumes that the distances of the points in the point cloud constitute a Gaussian distribution, the shape of which is determined by the mean and standard deviation. Let the coordinates of the first point in the point cloud be, and the distance from that point to any point is: Calculate the mean of the distance between each point traversed to any point as follows: Standard deviation is:  

   Let the standard deviation multiple be that only input is required during the implementation of the algorithm, and two thresholds are required. When a point is close and the average distance of points is within the standard range, the point is retained, and if it is not within the range, it is defined as outlier deletion. 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574560733
  ```  
 Returns a filtered point cloud that removes outliers. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574560733
  ```  
 Returns the index of outliers and non-outliers 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574560733
  ```  
 Use one or more of the specified additional options. Additional items are mainly: 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574560733
  ```  
#  III. Display of results 

 ![avatar]( 5ff9192a7be64d259cf693394128f4a2.png) 

#  IV. Official website code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574560733
  ```  
#  V. Reference links 

 Matlab Point Cloud Toolbox - Remove noise from 3-D point clouds 

#  Attached: Distance statistical analysis histogram 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574560733
  ```  
 ![avatar]( b749e31e0f644bfc9ee36c75e3a99698.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Algorithm overview 

   ① Establish a horizontal grid according to the measurement range and number each grid unit; ② Project all data points vertically onto the grid. 

##  2. References 

>  Shi Wen, Li Bijun, Li Qingquan. Image segmentation method of vehicle laser scanning distance based on projection point density [J]. Chinese Journal of Surveying and Mapping, 2005 (02): 95-100. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574578320
  ```  
#  III. Display of results 

 ![avatar]( 8ac292145d75412c824eb48bdb556c41.png) 

 Point cloud, projected image  

#  Fourth, a warning!!! 

   The lasFileReader function is a new function in matlab 2020b and above, so why do some bosses make mistakes?? Why ask??????  



--------------------------------------------------------------------------------

#  Function overview 

##  1. Algorithm overview 

   Visual 3D point cloud 

##  2. Main functions 

 Overloaded function 1: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
   Displays points using the location and color stored in the point cloud object. Overload function 2: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
   Displays the points specified by the xyzPoint matrix, the default display is: elevation Z rendering. Overload function 3: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
   Displays the points contained in the xyzPoint matrix, with the color specified by color. Overload function 4: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
   Displays the points contained in the xyzPoint matrix, the color specified by colorMap. Overload function 5: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
   Displays the point cloud stored in the file specified by the filename. Overload function 6: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
   Based on the above syntax, use one or more names and values for additional options specified by the parameter. Overloaded function 7: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
   Displays the axes. 

#  Code example 

##  1、pcshow(ptCloud) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
 result display  

##  2、pcshow(xyzPoints) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
 result display 

 ![avatar]( 52513b7bdb8a46859e79d699f8e749af.png) 

##  3、pcshow(xyzPoints,color) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
 result display  

##  4、pcshow(xyzPoints,colorMap) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
 result display  

##  5、pcshow(filename) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
>  It doesn't seem practical?? 

 result display  

##  6、pcshow(___,Name,Value) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
 result display  

##  7、ax = pcshow (___) 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
 result display  

##  8. Texture mapping to draw spherical point clouds 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574510628
  ```  
 result display   

#  III. Parameter analysis 

##  input parameter 

##  Name-value corresponding parameter 

##  output parameter 

#  IV. Use skills 

>  You can use all the operation functions on the visual window to fine-tune the displayed results. 

#  V. Reference links 

 Matlab point cloud toolbox - pcshow 



--------------------------------------------------------------------------------

#  Function overview 

##  1. Algorithm overview 

   Visualize the difference between two clouds 

##  2. Main functions 

 Overloaded function 1: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957451315
  ```  
   Create a visualization that describes the differences between the two input point clouds. These differences are shown by mixing the magenta of point cloud A with the green of point cloud B. Overload function 2: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957451315
  ```  
   Visualize differences using one or more names, values, and additional options specified for parameters. Overload function 3: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957451315
  ```  
   Using any of the previous syntax, return the plot axis to the visualization of the differences. 

#  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957451315
  ```  
#  III. Display of results 

 ![avatar]( 6a8f1928114f42209e8d180878dfd92b.png) 

#  IV. Parameter analysis 

##  input parameter 

##  Name-value corresponding parameter 

##  output parameter 

#  V. Use skills 

>  You can use all the operation functions on the visual window to fine-tune the displayed results. 

#  VI. Reference link 

 Matlab point cloud toolbox - pcshowpair 



--------------------------------------------------------------------------------

#  Function overview 

##  1. Algorithm overview 

   Visualize 3D point cloud data streams from devices such as Microsoft Kinect. To improve performance, pcplayer automatically downsamples the point cloud during interaction with the graph. Downsampling occurs only in the visualization of the point cloud and does not affect saved points. 

##  2. Main functions 

 Overloaded function 1: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957458596
  ```  
   Sets the range of the visual player in each axis direction. Overload function 2: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957458596
  ```  
   Returns the player for additional properties specified by one or more name, value, and parameter pairs. 

#  Code example 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957458596
  ```  
#  III. Display of results 

 ![avatar]( 3e3fb3185b28430e87ed9b9e72a6e962.gif) 

#  IV. Parameter analysis 

##  input parameter 

##  Name-value corresponding parameter 

##  output parameter 

##  OpenGL Option 

 ![avatar]( 09a37da1e48046aaa03172b7d25d6e79.png) 

 PCPlayer only supports the "OpenGL" option for Renderer graphics properties.  

#  V. Reference links 

 pcplayer 



--------------------------------------------------------------------------------

#  Function overview 

##  1. Algorithm overview 

   Bounding box for visualizing point clouds 

##  2. Main functions 

 Overloaded function 1: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574569854
  ```  
   Displays one or more shape instances on the current axis at the specified position. Overload function 2: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574569854
  ```  
   Specify options for parameters using one or more name-values. For example, 'Color', 'yellow' specifies the color of the displayed shape as yellow. 

#  Code example 

##  1. Example 1 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574569854
  ```  
##  2. Results display 

 ![avatar]( fa69e7296ac84834a612a43010268125.png) 

##  3. Code example 2 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574569854
  ```  
##  4. Display of results 

 ![avatar]( 99677c9ae7734bd9b1d160bff852095e.gif) 

#  III. Parameter analysis 

#  IV. Reference link 

 Matlab point cloud toolbox - showShape 



--------------------------------------------------------------------------------

#  Function overview 

##  1. Algorithm overview 

 ![avatar]( 16f7719c912f41a2ae67ac94276d81ff.gif) 

   Update the graph window and process callbacks  

##  2. Main functions 

 The drawnow function is used, and the non-point cloud handles the core function, so no analysis is done. You can view the detailed analysis by entering: help drawnow in the matlab command line window. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957451055
  ```  
#  III. Display of results 

 ![avatar]( 16f7719c912f41a2ae67ac94276d81ff.gif) 

#  IV. Reference link 

 drawnow 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

 The method here is to first fill the point cloud into a fixed-size 3D grid, and then select the first point in each grid to generate a new point cloud. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574564867
  ```  
#  III. Display of results 

 ![avatar]( bc1b635bb6234edb82e5fe44b63edcd3.png) 



--------------------------------------------------------------------------------

#  First, voxel filtering 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574542676
  ```  
 Use a voxel filter to return to the downsampled point cloud. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574542676
  ```  
#  III. Display of results 

##  1. Primitive point cloud 

 ![avatar]( c3434aea9243430a9e89014a33a809b9.png) 

##  1. Filtering results 

 ![avatar]( 8a5dc6f999ce4bb79bea1d91bbb37650.png) 

#  IV. Reference link 

 Matlab point cloud tool - pcdownsample 



--------------------------------------------------------------------------------

#  Function overview 

##  1. Algorithm overview 

    The Poisson reconstruction method involves the following steps: 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574520113
  ```  
   Create a surface mesh from the input point cloud ptCloudIn using the Poisson reconstruction method. The function also returns the octree depth and vertex density used in the reconstruction depth vertex density. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574520113
  ```  
 Also specify the octree depth value for the Poisson reconstruction method. 

##  3. Input and output parameters 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574520113
  ```  
#  III. Display of results 

##  1. Primitive point cloud 

 ![avatar]( 439153fccedd4413b2849bb38ea84dc6.png) 

##  2. Reconstruction results 

 ![avatar]( 513c38d394f54b20afd204539950c8dc.png) 

#  Fourth, a warning!!! 

   Copy and paste the code to run directly, and do not read other content of the blog. If you report an error, you will directly open "Why did I report an error, what kind of garbage code is this"??? pc2surfacemesh is a new function in matlab2022b and above, so why do some bosses make mistakes?? Why ask?????  



--------------------------------------------------------------------------------

#  Function overview 

##  1. Algorithm overview 

   Read point cloud data from LAS or LAZ files 

##  2. Main functions 

 Overloaded function 1: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574533778
  ```  
   Read point cloud data from the input LAS or LAZ file. Overload function 2: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574533778
  ```  
   Read the specified point attribute, ptAtt, from a LAS or LAZ file. In addition to the point cloud, the function also returns a structure, ptAttributes, containing the specified attribute for each point in the point cloud. Overload function 3: 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574533778
  ```  
   In addition to any parameter combination in the above syntax, specify the option to use one or more name-value pairs of parameters. For example, 'ROI', [5 10 5 10 5 10] sets the function to read the Region of Interest (ROI) of the point cloud. 

#  Example code 

##  1. Read point cloud data from LAZ files 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574533778
  ```  
 result display  

##  2. Point cloud visualization based on LAZ file classification data 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574533778
  ```  
 result display  

##  3. Read point cloud data from LAS files 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574533778
  ```  
 result display  

#  III. Parameter analysis 

##  input parameter 

##  Name-value corresponding parameter 

##  output parameter 

#  IV. Reference link 

 Matlab point cloud toolbox - ReadPointCloud 



--------------------------------------------------------------------------------

#  I. Overview 

   The LAS file format is an industry standard binary format developed and maintained by the American Society for Photogrammetry and Remote Sensing (ASPRS) for storing LiDAR data. The LAZ file format is a compressed version of the LAS file format. The LAS file contains a common header with LiDAR metadata, followed by LiDAR point records. Each point record contains attributes such as 3D coordinates, intensity, and GPS timestamp. A lasFileReader object stores metadata in a LAS or LAZ file as read-only attributes. The object function, readPointCloud, uses these attributes to read point cloud data from the file. 

##  main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574583707
  ```  
   Read metadata from a LAS or LAZ file and store it as an output property. 

#  Format analysis 

#  III. Sample code 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574583707
  ```  
#  IV. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574583707
  ```  
 ![avatar]( 3f12932500d44c7689e4bd775b90f926.png) 

#  V. Reference links 

 Matlab point cloud toolbox - lasFileReader 

#  Warning!!! 

   The lasFileReader function is a new function in matlab 2020b and above, so why do some bosses make mistakes?? Why ask??????  



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

   For any point, if the point has fewer than the specified number of neighbors within a certain neighborhood range, the point is deleted as noise. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574582838
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574582838
  ```  
 ![avatar]( 06d7b73158bc4ec1abb7c655f2f44d44.png) 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

##  1. Algorithm flow 

#  Code implementation 

 RansacPlaneCircle.m 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574559724
  ```  
 main.m 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574559724
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574559724
  ```  
 ![avatar]( befdf5965181461c93690cff63afe4ec.png) 

#  IV. Test data 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574559724
  ```  


--------------------------------------------------------------------------------

