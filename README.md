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

## Dark Mode 

## Colour Blind Mode 

