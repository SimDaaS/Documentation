
# Visualizer
## Version 1.0
### Developer

## 1. Summary
The Visualizer module is employed for the real-time visualization of sensor output data. It utilizes a TCP socket to manage incoming data and transmits it to the visualization window. The TCP server functionality is implemented based on an open-source project, ensuring robust handling of data transfer for effective visualization.

## 2. Method

### 2.1 Camera Visualization
Data is sent from limulator in form of jpg byte stream. This byte stream is traferred using TCP Connection and images are displace with Python Imaging Library on a tkinter window. Images are constantly updated on windows depending upon the sensor frequency. 

### 2.2 Lidar Visualization 
Data sent from the lidar sensor in from of numpy array file format bytestream. This is constanly updated in a double ended queue and diplayed on a openGL window.  

## 3. Requirements

