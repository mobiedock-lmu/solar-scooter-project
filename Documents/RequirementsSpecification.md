# Requirements Specifications

## 5.1  Introduction

The MobieDock Application will be the software component of the Solar Scooter Charger project. The application will based on existing electric scooter applications, with the intention to eventually be able to collaborate and integrate with their existing applications.

**Acronyms**

The acronyms contained in this document are as folllows:

Acronym | Meaning
|-----|--------|
CSCI  | Computer Software Configuration Item
CSC   | Computer Software Component
CSU   | Computer Software Unit
GUI   | Graphical User Interface

## 5.2  CSCI Component Breakdown CSC

CSCI MobieDock Mobile Application is comprised of the following CSCs

### 5.2.1 Graphical User Interface Client CSC

The Graphical User Interface (GUI) is the interface the user will be interacting with. The GUI will be composed of the following CSUs.

#### 5.2.1.1 Main Page CSU

#### 5.2.1.2 Charging Station Preview CSU

#### 5.2.1.3 Charging Station Menu CSU

##### 5.2.1.3.1 Statistics Subpage

##### 5.2.1.3.2 Rewards Subpage

##### 5.2.1.3.3 Heatmap Subpage

#### 5.2.1.4 User Menu CSU

### 5.2.2 Database CSC

The Database for the mobile application will track data relevant to the charging stations, energy use, and company information regarding advertisements and data to be determined with future partnerships.

## 5.3  Functional Requirements by CSC

### 5.3.1 Graphical User Interface

#### 5.3.1.1 Main Page

* The main page shall be displayed to the user upon opening the main application.

* The main page shall display a full-screen map that displays the location and surrounding map of the user.

* The main page shall display an icon that marks the location of the user on the map.

* The main page map shall display icons corresponding to the locations of nearby charging stations.

* The main page map shall display icons corresponding to the locations of nearby electric scooters and bikes.

* The main page shall display a search bar at the top of the screen for the user to search for a location.

* The main page map shall move to the location that a user inputs into the search bar to display nearby charging stations and vehicles at that given location.

* The main page shall display a circular button on the bottom of the screen to open the user menu.

#### 5.3.1.2 Charging Station Preview

* The charging station preview shall appear when a user taps a charger icon on the main page.

* The charging station preview shall cover roughly 1/4 the screen's width.

* The charging station preview shall display the street view of the charging station location.

* The charging station preview shall display a button to open the location on the Google Maps mobile application.

* The charging station preview shall display a button to open the charging station menu.

* The charging station preview shall display the location name of the selected charging station.

* The charging station preview shall display how many bays are available at the seleted charging station.

#### 5.3.1.3 Charging Station Menu

* The charging station menu shall be displayed when a user clicks on the button to view the menu from the charging station preview.

* The charging station menu shall take up most of the screen with small margins on all sides, and shall not cover the circular user menu button on the bottom of the screen.

* The charging station menu shall display the street view of the charging station location which will pan accordingly to any finger swiping interaction with the viewing window.

* The charging station menu shall display the location name of the charging station.

* The charging station menu shall display the location coordinates of the charging station.

* The charging station menu shall display the distance in miles of the charging station from the user.

* The charging station menu shall display the distance in minutes of the charging station from the user.

* The charging station menu shall display an announcement to the user to earn a reward for using the station.

* The charging station menu shall display a warning for heavy traffic if necessary.

* The charging station menu shall display the assigned bay number for the user.

* The charging station menu shall provide a link for the user to report any problems with the application or charging station.

* The charging station menu shall display a button for the user to start their trip.

* The charging station menu shall display a button for the user to reserve a bay.

#### 5.3.1.4 User Menu

* The user menu shall display a window when a user clicks on the user menu button on the bottom of the main page.

* The user menu shall take up most of the screen with small margins on all sides, and shall not cover the circular user menu button on the bottom of the screen.

* The user menu shall display tabs on the top of the window for the user to select a subpage. The tabs include: 1) Statistics 2) Rewards 3) Heatmap

* The user menu shall stop displaying if open when the user clicks on the user menu button on the bottom of the screen.

#### 5.3.1.5 Statistics Subpage 

* The statistics subpage shall display within the user menu window when a user clicks on the "Statistics" button on the top of the user menu window.

* The statistics subpage shall display statistics on charging station data and user data (*Note: These specific statistics shall be finalized when partnering with electric scooter companies and with further discussions with the engineering teams. Example statistics may include: Amount of energy saved by using charging stations, number of stations used this week, and miles traveled*).

#### 5.3.1.6 Rewards Subpage 

* The rewards subpage shall display within the user menu window when a user clicks on the "Rewards" button on the top of the user menu window.

* The rewards subpage shall display the rewards availble for a user to achieve in a list-like view.

* The rewards subpage shall display a progress bar under each reward tracking the progress to a reward.

* The rewards subpage shall feature a "Redeem" button under each reward for a user to redeem a reward, but will be greyed out and unclickable if the user has not yet achieved the reward.

* The rewards subpage shall feature a "View Reward" button under each reward for the user to view more details on the reward on click.

* The rewards subpage shall implement a page scrolling functionality within the user menu window.

#### 5.3.1.6 Heatmap Subpage

* The heatmap subpage shall display within the user menu window when a user clicks on the "Heatmap" button on the top of the user menu window.

* The heatmap subpage shall display a map, with default location set to the user's current location.

* The heatmap subpage shall display colored areas on the map that correspond to the most used areas and charging stations.

* The heatmap subpage map shall include scrolling, zooming, and panning fuctionality.

### 5.3.2 Database

* The database shall be a relational database.

* The database shall be only accessible by the front end when logged in to a valid account.

* The database shall record the location of the charging station by its coordinates.

* The database shall record the number of bays available at a station.

* The database shall record the number of total bays that comprise a station.

* The database shall record whether a given by is available or not.

* The database shall record the lase maintenance date of the charging station.

* The database shall record errors reported at each charging station.

* The database shall record ad information (to be finalized with further partnerships and discussions).

* The database shall record a history of the vehicles that have docked at the station.

* The database shall record the types of vehicles that are docked at the location (scooter, bike, etc.)

* The database shall record the cost to ride the vehivle.


## 5.4  Performance Requirements by CSC

## 5.5  Project Environment Requirements

#### 5.5.1   Development Environment Requirements

#### 5.5.2   Execution Environment Requirements

