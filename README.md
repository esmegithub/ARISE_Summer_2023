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

Once a potential sensor location has been identified; FloodNet must ensure that it is proximate to a LoRaWAN gateway, which allows the sensor to operate smoothly. In this [Sensor Locations Planner](https://www.google.com/maps/d/edit?mid=1njszfj9XP9E2616GYRWTTzQ7gLllMuxZ&usp=sharing), existing locations of gateways that have been installed are mapped. If a gateway is not present, FloodNet follows [this](https://github.com/floodnet-nyc/floodnet-gateway) guide.


After confirming that a location is flood-prone and proximate to a gateway, determining where to mount the sensors is crucial. FloodNet uses the street view feature in Google Maps to locate sign posts in the chosen region, and cross-reference these locations with the [NYC Stormwater Flood Maps](https://experience.arcgis.com/experience/4b290961cac34643a49b9002f165fad8/) to verify that the specific mounting location is flood-prone. If there are tall buildings on the south side of the street, FloodNet tries to select mounting locations on the north side. This ensures that the sensors will have plenty of sun exposure. It is also important to reconsider the proximity to the nearest gateway and ensure that the signpost is within a distance of about a mile or less. Once these conditions are satisfied, street view and map images are complied in a Google Sheet, which the technical team can reference in the field. Along with these images the Google sheet also includes the intersection where the sign post is located, a Google maps link to the location, the latitudinal and longitudinal coordinates of the sign post, the location of the closest gateway and the distance to it, and the flooding profile of the area. [This](https://github.com/esmegithub/ARISE_Summer_2023/blob/main/Neighborhood%20Prioritization.md) document shares some of the data collected and what different areas of high risk for floods look like.

<p align = "center">
<img width ="240" alt ="hoyt 5th" src="https://user-images.githubusercontent.com/105950235/175569789-9e65056a-1ca5-41c5-b0f1-3fcdd978370e.jpg">
<img width ="200" alt ="126th 7th" src="https://user-images.githubusercontent.com/105950235/175575464-7dc1b4c6-d0c3-47ff-9cde-ca8c4f0bdc40.jpg">

</p>
<p align = "center">
Deployed sensors on ideal sign post locations
</p>



### Sensor Placement Strategy
Once the sensor deployment location is identified, the following offers a brief summary of the next steps to deploy a [FloodNet](https://www.floodnet.nyc) flood sensor. A more in-depth overview can be found [here](https://github.com/floodnet-nyc/flood-sensor/blob/main/deployment/flood-sensor-deployment-manual.md?plain=1) .

### Before Leaving the Lab
This section details how we prepare for sensor deployment. Steps include compiling tools, preparing mounting equipment, and adding the sensor to the TTN app. 

This section contains the checklist for necessary tools, hardware, and equipment needed for the sensor deployment process.
| No | Item                                       | Count/sensor |
|----|--------------------------------------------|-------|
| 1  | [High leverage combination pliers](https://www.knipex.com/products/combination-and-multifunctional-pliers/high-leverage-combination-pliers/high-leverage-combination-pliers/0205200)           | 1     |
| 2  | [Adjustable wrench](https://www.kleintools.com/catalog/adjustable-wrenches/adjustable-wrench-standard-capacity-18-inch)                          | 1     |
| 3  | [Phillips #2 screwdriver](https://www.kleintools.com/catalog/screwdrivers/2-phillips-screwdriver-4-round-shank)                    | 1     |
|  4  | [Oversized Clipped Washers](https://www.mcmaster.com/93409A136/)                                           |    4   |
|  5  | [Green Powder-Coated Steel Strut Channel with Mounting Plate]()                                           |    1   |
|  6  | [Stainless Steel Hex Head Screw - 7/16"-14 thread size](https://www.mcmaster.com/92800A393/)                                           |    4   |
|  7  |  [Locknuts - 7/16"-14 thread size](https://www.mcmaster.com/90630A112/)                                        |    4   |
|  8  | Ratchet Wrench - 7/16", 1/2", 9/16" and 13mm                                                                        |1|
|  9  | Wire cutter                                                                                   |1|
| 10  | Plier                                                                                          |1|
| 11  | Zipties                                                                                           |5|
| 12  | Sockets - 12mm, 13mm and 14mm                                                                       |1 |
| 13  | Power Drill                                                                                     |  1|
| 14  | Steel Straps and strapping tool                                                                                          |1|
| 15  | Circuler Bubble Level                                                                                           |  1 |
| 16  | 3" Hex head M8 bolts and 3" Hex head M6 bolts                                                                 | 2+2 |
| 17  | M8 Lock nut and Lock washer                                                                                   | 4 |
| 18  | M6 Lock nut and Lock washer                                                                                   | 4 |
| 19  | 1.5" Hex head M8 bolts and 1.5" Hex head M6 bolts                                                                 | 2+2 |
| 20  | Foldable Ladder                                                                                                 |1|    
| 21  | 3" mending plate                                                                                                |1|

After we have identified the ideal mounting infrastructure (see [Flood Hotspots Identification](https://github.com/floodnet-nyc/flood-sensor/blob/main/deployment/hotspot%20identification/flood-hotspots-identification.md) document), the next step is to identify the mounting position on the post/pole itself. Next, we register the sensor on TTN by following these [steps.](https://github.com/floodnet-nyc/flood-sensor/tree/main/firmware) We have blanket approval from DOT to mount sensors on drive rails, also known as U-Channel posts. Each month, we update them on where new sensors have been installed. Though we try to identify optimal sensor placement [before leaving the lab](https://github.com/floodnet-nyc/flood-sensor/blob/main/deployment/hotspot%20identification/flood-hotspots-identification.md), unexpected obstacles can arise once we arrive at the mounting site. All the potential locations according to their priority are scouted and saved in the [FN Field Map](https://www.google.com/maps/d/u/1/edit?mid=1piTISi5Sm9NA6EmDnJhYw2CSyvhEOpE&ll=40.70724807589592%2C-73.93295012773706&z=17)

Potential obstacles include:
- Drive rail is slanted, or is not well secured. 
- Mounting location is overly shaded by a large building or aboveground train track or trees.
- Mounting location is in the path of a truck or bus, and sensor mounting arm would have to point into the street.
- Mounting location is on grass.

Sometimes, a new mounting location will have to be selected in the field. Helpful clues for selecting a flood-prone location include:
- Drive rail is close to a storm drain
- Street near drive rail is muddy and/or marked by the accumulation of trash
- Drive rail is located on the north side of the street, or has good sunlight exposure
- Drive rail is tall enough for sensor to be out of reach

## Sensor Installation Process
To ensure the optimal sensor placement, we need to complete the following steps:

### Accessing the infrastructure
- Finalize the location for sensor placement: Carefully select the ideal spots to position the sensors throughout the area.
- Securely position the ladder: Place the ladder on the ground firmly and securely to ensure stability while accessing higher areas for sensor installation.
- Determine the sensor height: Assess the appropriate height at which the sensors should be placed. Generally, a range of 2-3 meters is suitable for optimal data collection and accuracy.
- Mind the street signs: Take into consideration the street signs in the vicinity. Avoid obstructing them during sensor placement. If necessary, temporarily remove the signs to achieve the perfect sensor positioning, ensuring they are securely reinstated once the sensors are installed. *<insert_image>* 

### Mount installation 
To ensure proper installation of the sensor mount, follow the appropriate method based on the specific conditions and types of U-posts, drive rails, and sign posts. There are three types of installation methods outlined below:

- **1. Mounting the sensor on the front side of the post:**<br>
 To mount the sensor on the front side of the post, follow these steps for a secure installation:
  - **Position the L plate on the post:** Take the L plate that is attached to the mount and carefully place it on the front side of the post, ensuring it is positioned at the desired height.
  - **Secure the sensor mount:** Using two M8 1.5" bolts, along with two M8 locknuts and four Oversized Clipped Washers, fasten the sensor mount firmly onto the U-post. Make sure the bolts are tightened securely to ensure stability.<br>

By properly positioning the L plate on the front side of the post and using the specified bolts, locknuts, and Oversized Clipped Washers to secure the sensor mount, you can achieve a robust and reliable installation for the sensor on the U-post. (Refer to the provided image for visual reference.)
  
  <br>
  <img src="img/IMG_3356.jpg "width="300" height="360" >
  <br>

- **2. Mounting the sensor on the back side of the post:**<br>
  To mount the sensor on the back side of the post, follow these steps for a secure installation:
   - **Position the L plate with a mending plate:** Take the L plate attached to the mount and place it on the back side of the post. Ensure that a mending plate is inserted between the L plate and the post. This additional plate provides reinforcement and stability.
   -  **Secure the sensor mount:** Use two M8 3" bolts, along with two M8 locknuts and four Oversized Clipped Washers, to firmly attach the sensor mount to the U-post. Fasten the bolts tightly to ensure a secure and stable mounting.<br>

By positioning the L plate with the mending plate on the back side of the post and using the specified M8 bolts, locknuts, and Oversized Clipped Washers, you can achieve a reliable and sturdy installation for the sensor on the U-post. (Refer to the provided image for visual reference.)
  
  <br>
  <img src="img/mounted-back-slotted-plate.png" "width="250" height="600">
  <br>

- **3. Mounting the sensor on the post with an obstacle such as a stop sign, parking sign, or do not enter sign:**<br>
  To mount the sensor on a post with an obstacle like a stop sign, parking sign, or do not enter sign, follow these steps for a successful installation:
  
  - **Prepare the area:** Begin by unbolting the sign from the bottom, allowing it to be rotated or temporarily moved to create sufficient space for installing the mount.
  - **Install the sensor mount:** Once the obstacle has been moved or rotated, proceed with the steps mentioned earlier to securely mount the sensor on the U-post. This involves using the appropriate mounting hardware and following the provided instructions.<br>

By carefully unbolting and repositioning the sign to create the necessary clearance, you can then proceed with the regular steps for mounting the sensor on the U-post. (Refer to the provided image for visual reference.)
  
  <br>
  <img src="img/Behind the signs.jpg" "width="300" height="500">
  <br>
  
- **4. Mounting on a direction or signage round pole:**<br>
To ensure secure placement of the sensor, we will employ steel straps and a strapping tool. Follow these steps for a successful installation:
  - **Determine the strap length:** Estimate the required length of the straps, ensuring they are long enough to securely fasten the sensor. Cut two pieces from the steel strap roll, matching the estimated length.
  - **Position the L plate on the round pole:** Attach the L plate to the mount and place it on the round pole at the desired location for sensor installation.
  - **Begin strapping the first strap:** Using the strapping tool, start securing the first strap around the round pole and the L plate. Apply tension to the strap using the tool and ensure it is tightly fastened.
  - **Repeat the process for the second strap:** Once the first strap is securely tightened, repeat the same procedure for the second strap. Apply tension to the strap using the strapping tool, ensuring a firm and stable attachment.<br>

By utilizing the steel straps and strapping tool, cutting the appropriate length of straps, and securely fastening the sensor to the round pole using the L plate, you can achieve a reliable and secure placement of the sensor.(Refer to the provided image for visual reference.)

  <br>
  <img src="img/Sensor on Round pole.jpeg" "width="280" height="500" >
  <br>

By carefully following these guidelines, you can ensure the proper and secure installation of the sensor mount, tailored to the specific conditions and post types involved.

### Solar Panel installation
To maximize solar power harvesting, the solar panel should be south-facing and exposed to direct sunlight. Though we try to avoid mounting on overly slanted drive rails, a bit of slant is almost unavoidable. Once the sensor is partially secured to the drive rail, we use a level to determine how the pitch of the drive rail is impacting the angle of the mounting infrastructure. We use washers, zip ties, or other spacers to adjust the angle at which the sensor is mounted to the drive rail.

Furthermore, achieving parallel alignment of the sensor with the ground is crucial. To accomplish this, follow these steps:
- Place the circular bubble level at the bottom of the cone and observe the reading.
- Next, position the level on the ground directly beneath the sensor and take a reading. The bubble in the level should be in the opposite direction, indicating that the sensor is parallel to the ground. If not then adjust the mount little bit. *<insert the image*>

## Joining the FloodNet network
Once the installation is complete, it is important to perform a final check to ensure the proper functioning of the sensor. Follow these steps:
- Verify the antenna tightness: Double-check that the antenna is securely tightened in place. This will help optimize the signal reception and transmission.
- Switch on the sensor: Power on the sensor, and you should observe a green light illuminating. This indicates that the sensor is receiving power and is operational.
- Establish connection to the gateway: Wait for a moment as the sensor establishes a connection with the gateway. The green light will turn off once the sensor successfully connects.
 
## Start Sensing!
Access data on The Things Network: With the sensor connected, the collected data will become visible on The Things Network platform. You can now monitor and analyze the data transmitted by the sensor. New sensor locations should be recorded into master spreadsheet as well as deployment map.

### Flood Sensor Community Build Guide
poo

## FieldKit Weather
poo
