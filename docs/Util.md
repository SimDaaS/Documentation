# Util
## Version
### Developer

## 1. Summary
This module is designed to assist other modules, such as lidar and camera functionalities, within LimulatorUE. Additionally, it helps in logging, writing JSON files, and performing various functions regularly utilized in LimulatorUE, such as unit conversions specific to Unreal Engine and obtaining file locations within the project. 


## 2. Method
Util module consisits five class `ImageUtil`, `LidarUtil`, `JSONUtil`, `LimulatorHelper`, `LimulatorLogger`. 
<br>

ImageUtil is used by Image data worker to convert binary image data captured by camera sensor into JPG or PNG format. 
1. `ConvertToPng`: Convert binary image data to PNG format. 
2. `ConvertToJpg`: Convert binary image data to JPG format.
3. `SaveToFile`: Save binary image data to input file.
4. `SavePngFile`: First converts binary data to PNG format and then save to file.
5. `SaveJpgFile`: First converts binary data to JPG format and then save to file. 
<br>

The LidatUtil module consists of various functions used by lidar sensor:
1. `GetMaterialNameByHitResult`: This function returns the material of hit point resulting from ray casting.
2. `GetIncidentAngle`: This function returns the incident angle of lidar rays upon hitting a surface.
3. `ComputeIntensityRotatingLidar`: This function calculates the intensity for a Lidar sensor using the formula provided in the documentation for [Lidar Sensor](LidarSensor.md). 
4. `ComputeIntensitySolidStateLidar`: This function calcultes the intensity for a Solid state Lidar sensor using the formula provided in the documentation for [Lidar Sensor](LidarSensor.md).
5. `GetClassTagByHitResult`: This function returns the class of the hit point resulting from ray casting.
6. `AddRandomNoise`: This function adds noise to the resulting hit points.
<br>

The LimulatorHelper module consists of various helper functions designed to help in different tasks:
1. `ComputeAngleBetweenTwoVectors`: This function calculates the angle in degrees between two vectors.
2. `VectorUnrealToNormal`: It converts an Unreal Engine vector to a typical vector format used outside of Unreal.
3. `VectorNormalToUnreal`: This function converts a typical vector to an Unreal Engine vector.
4. `RotatorNormalToUnreal`: It converts rotations in the usual format to Unreal Engine rotations.
5. `LocationToPosition`: This function converts an Unreal Engine location to a roamanager::position.
6. `PositionToFVector`: It converts a roamanager::position to an Unreal Engine location vector.
7. `GetXoscFilePath`: This function returns the path of the input Xosc file.
8. `GetXodrFilePath`: This function returns the path of the input Xodr file.

JSONUtil is used by bounding box sensor to save bounding box information into JSON file. 
<br>

LimulatorLogger is used to log anything in Limulator category. 
## 3. Requirements
1. Unreal Engine 
