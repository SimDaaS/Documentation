
# Weather 
## Version 1.0
### Developer

## 1. Summary
The Weather module, as its name implies, is tasked with controlling the weather within the 3D environment. It manages elements such as sun position, fog, and precipitation, among other factors, to create a dynamic and realistic weather simulation. Weather module is mainly implemented in blueprints. See BP_Sky and BP_Wether for more. 

## 2. Method

### 2.1 BP_Sky
BP_Sky is the module that control the static environment and required DirectionalLight and Skylight to work. It can change the material applied on the planet mesh, sun postion, etc among other things. It provides interface for the following: 
1. Sun Altitude 
2. Sun Azimuth 
3. Cloudiness 
4. Fog 

BP_Sky is not meant to be directly controlled by the user. It is used as a componenet by BP_Weather. 

### 2.2 BP_Weather 
BP_Weather is mainly responsible for controlling the dynamic weather in the environment. BP_Weather depends on BP_Sky and will not work without it. It provides and interface to change the following: 
1. Cloudiness 
2. Precipitation
3. Precipitation Deposits 
4. Wind 
5. Sun Altitude 
6. Sun Azimuth 
7. Fog 
8. Wetness 
9. Scattering Intensity 
10. Dust 

  Note: Weather module is highly inspired from the weather module in CARLA. 

## 3. Requirements

## 4. How-to-guide

### 4.1 Step 1
  1. Step 1 - 1
  2. Step 1 - 2
  3. Step 1 - 3
### 4.2 Step 2
  1. Step 2 - 1
  2. Step 2 - 2
  3. Step 2 - 3
### 4.3 Step 3
  1. Step 3 - 1
  2. Step 3 - 2
  3. Step 3 - 3

## 5. Tutorials
