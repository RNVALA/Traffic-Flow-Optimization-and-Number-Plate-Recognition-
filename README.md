# Traffic-Flow-Optimization-and-Number-Plate-Recognition

<div align="center">
  
![traffic-light](https://github.com/RNVALA/Traffic-Flow-Optimization-and-Number-Plate-Recognition-/assets/112707550/24db5ee6-601d-4c78-8ca1-3a566fa5f789)

</div>

# Problem Statement

## Traffic signal
With the increasing population and number of automobiles in cities, traffic congestion has become a major issue. Traffic jams not only cause delays and stress for drivers but also contribute to increased fuel consumption and air pollution. In order to address this problem, a <code>Computer Vision-based traffic signal controller</code> has been developed to improve traffic management. The system aims to automatically adapt to the traffic situation at the traffic signal by allocating time to specific lanes based on the density of traffic.


## Number plate detection

With the increasing crime and vehicle missing in cities. it has become  difficult for police and management to  track of the vehicles. The developed system aims to <code>automaticaly capture every vehicle details passed by juction or lane.</code>

# Solution
Our proposed system is designed to enhance traffic management at a traffic junction by taking an image from the CCTV camera as input for real-time traffic density analysis. The system is divided into three modules, including vehicle detectionand recognition,  signal switching, and visualization.

##  Detection and Recognition Module:
- This module captures an image of a specific signal when a lane is closed and stores it in a corresponding lane folder.
- The captured image is then loaded back, and the module performs detection and recognition on all classes present in the COCO dataset, which contains 80 classes.
  However, we are specifically interested in storing details for four classes: cars, bikes, trucks, and buses.
- Based on the number of vehicles detected for each class, we have developed an algorithm that provides the required time for the particular lane to pass all vehicles.
- This calculated time is then assigned to the Signal Module, which simulates a green signal for that time period, along with displaying the assigned time.
 Other signals are set to red, indicating their waiting time before opening.
- The algorithm assigns a time within a range of 5 to 30 seconds for the green signals based on the density of vehicles. so, maximum waiting time for signal next to open signal is 30 second and minimum is 5 second. similarly we will give time to all remaining lane with red signal.
  
## Signal switching Module
Finally, the signal switching module sets the green signal timer according to traffic density detected by the vehicle detection module and updates the red signal timers of other signals accordingly. The signal switches clockwise  according to the timer.

## Visualization Module
- Simultaneously, all the data is stored in a CSV file, including the time, day, month, number of cars, number of bikes, number of trucks, number of buses, and the link to the captured image.
- This data is imported into Power BI, where we create a dashboard to visualize the information.
- The dashboard provides insights such as traffic patterns on specific days of the week, the busiest months of the year, and the overall traffic situation in the city.
Additionally, the dashboard allows users to view individual junctions' traffic data, including specific lanes.
- This comprehensive visualization aids in making future traffic predictions, such as anticipating heavy traffic during festivals and facilitating the diversion of vehicles accordingly.


## Flow chart For out proposed solution

<div align="center">
  
![WhatsApp Image 2023-07-01 at 09 38 35](https://github.com/RNVALA/Traffic-Flow-Optimization-and-Number-Plate-Recognition-/assets/112707550/b1e24760-d482-49d4-9bbc-74eee7e3ba15)
</div>








