# Single-human 6D pose estimation based on fusion of IMU and multi-view images

The context of our framework:
  1. Human upper body model
  2. 
  Human upper model includes 10 joint-links. Root joint <img src="http://chart.googleapis.com/chart?cht=tx&chl= h_0" style="border:none;"> (hip) is regraded as human base coordinate, which represented in the global coordinate. The root joint is represented by the rotation matrix <img src="http://chart.googleapis.com/chart?cht=tx&chl= R_{h_0}^g" style="border:none;"> and translation offest vector <img src="http://chart.googleapis.com/chart?cht=tx&chl= t_{h_0}^g" style="border:none;"> , the other joints are represented w.r.t the root joint by the rotation and translation.
  ![Uploading image.png…]()

  2. Cost function

  3. Optimization


The features of our methods:
  
