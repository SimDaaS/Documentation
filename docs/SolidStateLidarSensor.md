# Module Name
Solid-State LIDAR Sensor 
## Version
### Developer

## 1. Summary
The Lidar sensor is designed to simulate a Soild-state Lidar sensor using ray-casting. It utilizes Lidar parameters such as channels both horizontal and vertical, scanning frequency, field of view both horizontal and vertical, and range to generate a point cloud output. The resulting point cloud contains location, time, distance, intensity, label and scan angle information in `ply` format.


## 2. Method
To simulate the rotating LIDAR sensor, the sensor is first initiallised by computing horizontal and vertical angle for each horizontal and veritcal channel/laser within there respective FOV.  Ray-casting is then performed for each horizontal and veritical channel/laser with a rate of `1/frequency`. The point cloud obtained from ray-casting contains information about the hit point's **location** (in xyz), **time** , **distance**, **intensity**, **label** and **scan angle**. 

Rest of all funcitionality is same as [Rotating Lidar Sensor](LidarSensor.md). 

### Solid State Lidar attributes

| Input attribute  | Type   | Default    | Description     |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `channelsH`         | int    | 128    | Number of lasers in horizontal.  |
| `channelsV`         | int    | 32     | Number of lasers in vertical.  |
| `frequency`| float  | 20.0 | Sensor frequency (in Hz).       |
| `wavelength`     | float  | 1.4   | Wavelength at which solid-state Lidar sensor operates (in micrometer). |
| `minRange`            | float  | 0.0  | Minimum distance at which a point can be detected by the Lidar sensor (in cm).  |
| `maxRange`            | float  | 10000.0  | Maximum distance at which a point can be detected by the Lidar sensor (in cm).      |
| `negHorizontalFOV`        | float  | -45.0 | Minimum horizontal Angle (in degrees).         |
| `posHorizontalFOV`        | float  | 75.0  | Maximum horizontal Angle (in degrees).        |
| `negVerticalFOV`        | float  | -10.0 | Minimum vertical Angle (in degrees).         |
| `posVerticalFOV`        | float  | 20.0  | Maximum horizontal Angle (in degrees).        |
| `atmosphereAttenuationRate`     | float  | 0.004 | Coefficient that measures the solid state Lidar instensity loss per meter, |



### Output attributes

| Sensor data attribute            | Type  | Description        |
| ----------------------- | ----------------------- | ----------------------- |
| `x`            | float   | X coordinate of hit point.                      |
| `y`            | float  | Y coordinate of hit point.       |
| `z`            | float   | Z coordinate of hit point.       |
| `intenstity`            | float   | Intensity of the reflected leaser from the hit point.               |
| `time`        | float| Simulation time of the measurement in seconds since the beginning of the episode.        |
| `label`        | uint | Label of hit point (see class-label mapping). |
| `r`   | uint | red value of the color of label.              |
| `g`         | uint  |  green value of the color of label.    |
| `b`       | uint  |  blue value of the color of label.  |
| `scan_angle`         | float | Horizontal angle of the hit point.      |
| `distance`         | float| Distance of hit point from  Lidar sensor (im cm).          |



## 3. Requirements
