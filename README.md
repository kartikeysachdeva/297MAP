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

