# ARISE_Summer_2023
NYU Tandon's ARISE (Applied Research Innovation in Science & Engineering) program is a 7 week summer internship that allows students to work within research labs. FloodNet is a cooperative of communities, researchers, and New York City government agencies working to better understand the frequency, severity, and impacts of flooding in New York City. They aim to provide access to real-time information and data on flooding to aid city agencies and residents.


**Table of Contents**

- Introduction
- Sensors
    - Sensor Scouting 
    - Sensor Placement Strategy
    - Flood Sensor Community Build Guide
- FieldKit Weather

## Introduction
intro text

## Sensors
yum

### Sensor Scouting
FloodNet takes community need very seriously and as such uses this [Google Form](https://forms.gle/4kJpujo9pDt7hZmRA) to allow NYC residents to suggest locations for deployment of sensors. In addition to this, FloodNet is partnered with NY Sea Grant and the Science and Resilience Institute of Jamaica Bay; these organizations, along with the NYC Mayor’s Office of Climate Resiliency and other partners, co-founded a [Community Flood Watch Project](https://www.srijb.org/jbfloodwatch/) that has helped to inform their outreach.

Once a location is proposed, FloodNet consults the [NYC Stormwater Flood Maps](https://experience.arcgis.com/experience/4b290961cac34643a49b9002f165fad8/) to confirm that this location is likely to be impacted by flooding in a Moderate Stormwater Event. 

<p align="center">
  <img width="200" alt="Screen Shot 2022-06-24 at 11 43 52 AM" src="https://user-images.githubusercontent.com/59215820/175576645-eda4971e-e09d-4b02-a26d-a11e77c93043.png">
</p>
<p align="center">
  An example on NYC Stormwater Flood Maps, of an area prone to flooding, where a sensor has been deployed.
</p>

Once a potential sensor location has been identified; FloodNet must ensure that it is proximate to a LoRaWAN gateway, which allows the sensor to operate smoothly. In this [Sensor Locations Planner](https://www.google.com/maps/d/edit?mid=1njszfj9XP9E2616GYRWTTzQ7gLllMuxZ&usp=sharing), existing locations of gateways that we have installed have been mapped. If a gateway is not present, FloodNet follows [this](https://github.com/floodnet-nyc/floodnet-gateway) guide.


After confirming that a location is flood-prone and proximate to a gateway, we need to determine where we will mount the sensors. We use the street view feature in Google Maps to locate sign posts in the region we have chosen, and cross-reference these locations with the [NYC Stormwater Flood Maps](https://experience.arcgis.com/experience/4b290961cac34643a49b9002f165fad8/) to verify that the specific mounting location we have chosen is flood-prone. If there are tall buildings on the south side of the street, we try to select mounting locations on the north side. This ensures that our sensors will have plenty of sun exposure. It is also important to reconsider the proximity to the nearest gateway and ensure that the signpost is within a distance of about a mile or less. Once these conditions are satisfied, we compile street view and map images in a Google Sheet, which our technical team can reference in the field. Alongwith these images the Google sheet also includes the intersection where the sign post is located, a Google maps link to the location, the latitudinal and longitudinal coordinates of the sign post, the location of the closest gateway and the distance to it, and the flooding profile of the area. 

<p align = "center">
<img width ="240" alt ="hoyt 5th" src="https://user-images.githubusercontent.com/105950235/175569789-9e65056a-1ca5-41c5-b0f1-3fcdd978370e.jpg">
<img width ="200" alt ="126th 7th" src="https://user-images.githubusercontent.com/105950235/175575464-7dc1b4c6-d0c3-47ff-9cde-ca8c4f0bdc40.jpg">

</p>
<p align = "center">
Deployed sensors on ideal sign post locations
</p>



### Sensor Placement Strategy
poo

### Flood Sensor Community Build Guide
poo

## FieldKit Weather
poo
