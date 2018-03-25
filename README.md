# 平台工具集：
- Windows7 64位
- Visual Studio 2017
- OpenCV 3.4.1

# 项目简介：
    > 在运动目标的，最常见的问题包括：光照变化、运动目标发生形变、目标被遮挡等。本项目针对运动目标被遮挡，提出BP神经网络+Kalman滤波器的联合预测模型。传统的卡尔曼预测的基本思想是：构建状态方程，由当前时刻的位置计算出下一时刻目标的位置（状态值），同时，将当前时刻的位置作为下一时刻的观测值，然后将两者的值融合，得出最优估计值，即卡尔曼滤波器预测出的目标位置。

    > 为提高预测的精准度，将神经网络引入Kalman滤波器中。根据前六个时刻目标的位置关系，用其差值对神经网络进行训练，然后再用相邻三个时刻的位置差值进行预测，得出下一时刻目标的可能位置，用神经网络的预测值代替传统卡尔曼滤波器中的观测值。
    
    > 用本方法构建的神经网络-Kalman滤波器模型的预测值误差要小于传统Kalman滤波器的预测值；

# 步骤：

  1. 事先用鼠标点击保存一视频中行人的位置(每隔五帧取一个点);
  
  2. 读取保存的点坐标，依次做差;
  


