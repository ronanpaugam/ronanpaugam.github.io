---
layout: post
title: First Step for Grass Fuel Consumption Estimation from UAV
description: Estimating Digital Surface Model from UAV borne visible images to calculate vegetation volume     
thumbnail: "/data/FuelLoadEstimationFromUAV/thumbnail.png"
tags: [remoteSensing,fieldwork]
---
As a first step to estimate fuel consumption of a fire using commercial UAV and stereo-matching algorithm, in summer 2017 I worked with Jim Cronan from the Pacific North West US Fores Service Lab on the estimation of fuel height in the homogeneous grass fields for Carnation Farm in Washington State near Seattle.

Using an "out of the shelf" Phantom 4 Pro DJI drone and ground control points located with a trimble differential GPS, we run the Agisoft software to extract point cloud representation of three grass fields. Below is an example of our last flights when we finally got our methodology working. Unfortunately this happened after the farmer mowed the field, so the grass is pretty much low.  
{% include pointscene.html id="0cf80235" campos="579329.752,5280505.242,17.278" lookat="579309.841,5280503.095,8.983" label="Georeferenced MIR images from the skukuza6 burn"%}

Using the built-in capabilities of Agisoft, we extracted from our point clouds orthomosaic photo (see figure below) and Digital Surface Model (DSM).
{% include image.html file="/data/FuelLoadEstimationFromUAV/ortho_CaranationFarm_test03_f06.png" alt="orthomosaic "
                      caption= "orthomosaic nadir view of the scene from Caranation Farm third test campaign generated with Agisoft with images collected by a Phantom 4 DJI UAV"%}

The methodology to estimate fuel consumption relies on the difference between a pre-burn and a post-burn DSM. It gives the volume of the burnt vegetation, and the corresponding mass is then calculated using distribution of bulk density  estimated from pre-burn orthomosaic map and in-situ destructive sampling done on the side of the plot.

To make sure that DSM retrieved from Agisoft can be used to get a correct measure of grass height, we were interested first in comparing DSM extracted from different flights of the same scene. Below is an example for the scene shown in the above orthomosaic.  
{% include image.html file="/data/FuelLoadEstimationFromUAV/DSMDiff_CaranationFarm_test03_f07f06.png" alt="DSM difference "
                      caption= "Digital Surface Model (DSM) difference btween 2 flights of the scene from Caranation Farm third test campaign. DSM were generated with the Agisoft Software from images collected by a Phantom 4 DJI UAV"%}
A slope shows up in the DSM difference map with difference ranging from -5 cm the bottom left corner to 6 cm  in the upper right corner. The grass was so short, that this is certainly not coming from wind effect. We think that the mismatch is probably due to the DGPS height accuracy of our ground control points. Further test with total station or more accurate DGPS unit (e.g. Javad Triumph-1) would be required.
