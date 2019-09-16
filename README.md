# A*3D: An Autonomous Driving Dataset in Challeging Environments

**Night-time high-density** examples from the proposed A*3D dataset with RGB images and their corresponding LiDAR data. 

<div align=center><img width = '500' src ="images/Example.png"/></div>

### Sensor Setup
We collect raw sensor data using the A*STAR autonomous vehicle, which is equipped with the following sensors:
  - Two PointGrey Chameleon3 USB3 Global shutter color cameras (CM3-U3-31S4C-CS) with 55Hz frame rate, 2048 × 1536 resolution.
  - A Velodyne HDL-64ES3 3D-LiDAR with 10Hz spinrate, 64 laser beams.
  
The following depicts the Sensor setup for A*3D data collection vehicle platform. 
  <div align=center><img width = '350' src ="images/Vehicle.png"/></div>
  
### Data Collection
- The data collection covers **the entire Singapore** including highways, neighborhood roads, tunnels, urban, suburban, industrial, HDB car parks, coastline, etc. 
- NuScenes only covers a small portion of Singapore roads (highlighted in red).

  <div align=center><img width = '450' src ="images/DrivingRoutes.png"/></div>

### Dataset Statistics
- **High-density frames**. 
	- The number of annotations per frame for A*3D dataset are much **higher than KITTI dataset**.
	- The A*3D dataset comprises **7 annotated classes** corresponding to the most common objects in road scenes.

<div align=center><img width = '450' src ="images/statistics1.png"/></div>

- **Heavily occluded frames**. 
	- About half of the vehicles are partially or highly occluded.
	<div align=center><img width = '450' src ="images/statistics2.png"/></div>

	- Average number of points inside the bounding box of each class and the Log number of points within bounding box.
  	<div align=center><img width = '450' src ="images/statistics3.png"/></div>

### Benchmarking
- Object-density: Cross-dataset Evaluation
  - A pre-trained model of PointRCNN on KITTI suffers almost a 15% drop in mAP on A*3D validation set. 
  - When trained on our high-density subset, PointRCNN achieves much better performance on the KITTI validation set, especially on Moderate and Hard with almost 10% improvements.
   <div align=center><img width = '450' src ="images/results1.png"/></div>
   
- High object-density vs. Low object-density
  - When increasing the training data, the performance improvements are marginal.
  - The best result comes from mixing high and low density samples.
    <div align=center><img width = '450' src ="images/results2.png"/></div>

- Day-time vs. Night-time
  - We are the first to provide a systematic study on the effects of night-time on 3D object detection systems. 
    <div align=center><img width = '450' src ="images/results3.png"/></div>




