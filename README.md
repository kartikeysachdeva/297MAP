# Map-Go-Brr

A GIS (Geographic Information System) software that displays maps and relevant information (street names, point of interests, subways etc.) for various major cities around the world. The project was created in C++ and uses APIs based on OSM (Open Street Maps) data. The graphics were created using EZGL Graphics Library in addition to GTK and Glade.

This project was created with a team of two other members for ECE297 which is a course at the University of Toronto on software design and communication. As part of the course guidelines, the source code cannot be publicly shared, however, a detailed description and final software images are given below.

## Design and Layout

### 1. Welcome Menu
- A brief welcome menu is displayed when the map is initially loaded
- Directs the user towards the help menu in case the user is unfamiliar with the software
![initialLoad](https://user-images.githubusercontent.com/69488258/120865339-d9b2c680-c55b-11eb-9513-e92ff1e13966.png)

### 2. Main User Interface

- Top Left Corner: Input boxes are used to get travel directions between a starting and ending intersection. Drop down menu below to load other maps
- Top Right Corner: Buttons to toggle other modes and features
- Bottom Right Corner: Buttons for zoom and pan. The scroll wheel can be used to zoom and pan as well.
- Bottom Left Corner: Dynamic status updates in reponse to user actions
![](https://github.com/lilkarti/297MAP/blob/main/Images/mainUI.jpg)

## Key Features
All selections and items displayed on the map can be cleared using the "Clear" button underneath the maps drop down menu and all input boxes have an autocomplete feature. Any additional windows can be hidden or shown using the "Additional Window" option in the top right corner.

### 1. Loading Maps 
- Maps can be loaded using the drop down menu and the "Load Map" button underneath
- Any other city can be added to the drop down menu as long as the osm.bin file is installed

![](https://github.com/lilkarti/297MAP/blob/main/Images/loadMap.gif)

### 2. Travel Directions
- The user can enter a start and end intersection to get travel directions which are displayed in a separate window
- The shortest path is found using an A* algorithm

![](https://github.com/lilkarti/297MAP/blob/main/Images/travelDirections.png)

### 3. Point of Interest Search
- Point of Interests such as restaurants, banks, hospitals, schools, etc. can be specifically searched for

![](https://github.com/lilkarti/297MAP/blob/main/Images/POISearch.png)

### 4. Subway Stations
- Displays all subway stations for the city

![](https://github.com/lilkarti/297MAP/blob/main/Images/subwayStations.png)

### 5. Viewing Modes
- There are two different viewing modes (dark more and colourblind mode) to allow for greater accssibility and ease of use

#### Dark Mode 
![](https://github.com/lilkarti/297MAP/blob/main/Images/darkMode.png)

#### Colour Blind Mode 
![](https://github.com/lilkarti/297MAP/blob/main/Images/colourblindMode.png)

### 6. Intersections Between Two Streets
- Intersections can be either clicked on or searched for through the two input boxes
- An additional window is displayed with all names of the intersections currently being highlighted on the map

![](https://github.com/lilkarti/297MAP/blob/main/Images/intersectionsBetweenTwoStreets.gif)

### 7. Icons and Language Support

- Point of Interests are represented using easily recognizable icons
- One way streets are identified by a blue arrow
- Certain maps such as Tokyo and Tehran have street names displayed in Japanese and Arabic, respectively.

#### Icons and Arrows 

![](https://github.com/lilkarti/297MAP/blob/main/Images/iconsAndArrows.png)


#### Language Support  

![](https://github.com/lilkarti/297MAP/blob/main/Images/languageSupport.png)

### 8. Error Messages and Help Menu


- Error messages are provided when an invalid input is given or the user misuses the system
- A help menu is available for further guidance

#### Error Messages
![](https://github.com/lilkarti/297MAP/blob/main/Images/errorMessages.png)


#### Help Menu 

![](https://github.com/lilkarti/297MAP/blob/main/Images/helpMenu.png)

## Notable Algorithms

### 1. Dijkstra's and A* Algorithms

- The main path finding algorithm used was Dijkstra's Algorithm
- To imporve the performance an A* heuristic was implemented that uses the shortest travel time for a more directed search

### 2. Travelling Salesman Problem 

An algorithm was implemented to solve a version of the Traveling Saleman Problem. An iterative approach was taken with the following algorithms used to generate a valid solution within 50 seconds:

- Greedy Algorithm: To generate an intial solution quickly
- Local Pertubations: Swaps and a custom reversal operator was used to improve the initial solution
- Multistart: Multiple start locations were considered and the best one was selected to explore the solution space more

The algorithm was tested for different inputs on multiple maps. These test cases were used to produe an average Quality of Result (QoR). Here is the average QoR for the iterative approach to the problem:


![](https://github.com/lilkarti/297MAP/blob/main/Images/m4Improvement.png)


