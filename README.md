# Single-human 6D pose estimation based on fusion of IMU and multi-view images

The context of our framework:
  1. Human upper body model
 
  Human upper model includes 10 joint-links. Root joint <img src="http://chart.googleapis.com/chart?cht=tx&chl= h_0" style="border:none;"> (hip) is regraded as human base coordinate, which is represented by the rotation matrix <img src="http://chart.googleapis.com/chart?cht=tx&chl= R_{h_0}^g" style="border:none;"> and translation offest vector <img src="http://chart.googleapis.com/chart?cht=tx&chl= t_{h_0}^g" style="border:none;"> in the global coordinate, the other links are represented w.r.t the root joint by the rotation and translation.
  
 ![QQ截图20210719081923](https://user-images.githubusercontent.com/52600391/126127071-12ac66d1-6809-457d-8863-1a365f19c269.png)

![image](https://user-images.githubusercontent.com/52600391/126116124-7167d3e3-5b78-4a1c-9c63-8892489ee3cb.png)


  2. Cost function

    IMU error
    
    Position error

  3. Optimization


The features of our methods:
  
