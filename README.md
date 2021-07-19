# Single-human 6D pose estimation based on fusion of IMU and multi-view images

The context of our framework:
  1. Human upper body model
 
 人体上肢运动学模型为包含 10 个连杆的运动系统, 其中根连杆h0（髋部）为人体基坐标系, 包含相对世界坐标系表示的姿态R和位移t, 其余子连杆hj, j ∈ {1,2, · · · , 9}通过球形关节与父连杆连接, 相对于父连杆有旋转R和常量连杆位移t. 
  
 ![QQ截图20210719081923](https://user-images.githubusercontent.com/52600391/126127071-12ac66d1-6809-457d-8863-1a365f19c269.png)

![image](https://user-images.githubusercontent.com/52600391/126116124-7167d3e3-5b78-4a1c-9c63-8892489ee3cb.png)


  2. Cost function

    IMU error
    
    Position error

  3. Optimization
  
  在优化问题中给定接近最优解的初始迭代值能够提升梯度下降的效率, 并减少求解陷入局部最优的可能性, 为此使用前一组数据所求得的姿态结果作为初始迭代值来进行优化问题的求解. 而对于优化第一组数据, 由于没有上一时刻的结果可以利用, 设计了初始化阶段以提供最初的迭代值. 在初始化阶段中, 预先定义了一个初始姿态 θ_init （一般为T-pose：即保持身体直立, 双手向两侧平举的姿态）,操作人员需要和初始姿态保持吻合, 再以初始姿态θ_init 作为当前优化问题的初始值进行姿态求解, 以计算得到第一组数据的姿态估计结果. 

The features of our methods:
  
