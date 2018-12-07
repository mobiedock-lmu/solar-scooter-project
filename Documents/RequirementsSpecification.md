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

#### 5.2.1.1 Login Page CSU

The Login Page allows the user to log in to their account via their Google account.

#### 5.2.1.2 Main Page CSU

The Main Page displays a map of electric scooter and charging station locatios around the user and allows the user to search for stations near them.

#### 5.2.1.3 Charging Station Preview CSU

The Charging Station Preview is a popup window that will display when a user taps on a charging station and provides a preview of information on the charging station. A button will direct the user to open the Charging Station Menu.

#### 5.2.1.4 Charging Station Menu CSU

The Charging Station Menu displays information on the selected charging station, and the ability to reserve a bay.

#### 5.2.1.5 User Menu CSU

The User Menu will provide the user with subpages including: 1) Statistics 2) Rewards 3) Heatmap

##### 5.2.1.5.1 Statistics Subpage

The Statistics subpage displays statistics about the user, including miles traveled and energy saved.

##### 5.2.1.5.2 Rewards Subpage

The Rewards subpage displays the rewards a user can attain from using charging stations, as well as the user's progress.

##### 5.2.1.5.3 Heatmap Subpage

The Heatmap subpage displays a heatmap highlighting the user's most used areas where they have used a charging station.


### 5.2.2 Database CSC

The Database for the mobile application will track data relevant to the charging stations, energy use, and company information regarding advertisements and data to be determined with future partnerships.

## 5.3  Functional Requirements by CSC

### 5.3.1 Graphical User Interface

#### 5.3.1.1 Login Page

* The login page shall be displayed to the user upon opening the main application.

* The login page shall display the MobieDock logo.

* The login page shall display a "login" button.

* Upon clicking the "login" button, the login page shall display an alert to the user to sign in using a Google account.

* The login page shall direct the user to a Google sign in page where a user shall input their username and password.

#### 5.3.1.2 Main Page

* The main page shall be displayed once a user has successfully logged in from the login page.

* The main page shall display a full-screen map that displays the location and surrounding map of the user.

* The main page shall display an icon that marks the location of the user on the map.

* The main page map shall display icons corresponding to the locations of nearby charging stations.

* The main page map shall display icons corresponding to the locations of nearby electric scooters and bikes.

* The main page shall display a search bar at the top of the screen for the user to search for a location.

* The main page map shall move to the location that a user inputs into the search bar to display nearby charging stations and vehicles at that given location.

* The main page shall display a circular button on the bottom of the screen to open the user menu.

#### 5.3.1.3 Charging Station Preview

* The charging station preview shall appear when a user taps a charger icon on the main page.

* The charging station preview shall cover roughly 1/4 the screen's width.

* The charging station preview shall display the street view of the charging station location.

* The charging station preview shall display a button to open the location on the Google Maps mobile application.

* The charging station preview shall display a button to open the charging station menu.

* The charging station preview shall display the location name of the selected charging station.

* The charging station preview shall display how many bays are available at the seleted charging station.

#### 5.3.1.4 Charging Station Menu

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

#### 5.3.1.5 User Menu

* The user menu shall display a window when a user clicks on the user menu button on the bottom of the main page.

* The user menu shall take up most of the screen with small margins on all sides, and shall not cover the circular user menu button on the bottom of the screen.

* The user menu shall display tabs on the top of the window for the user to select a subpage. The tabs include: 1) Statistics 2) Rewards 3) Heatmap

* The user menu shall stop displaying if open when the user clicks on the user menu button on the bottom of the screen.

#### 5.3.1.6 Statistics Subpage 

* The statistics subpage shall display within the user menu window when a user clicks on the "Statistics" button on the top of the user menu window.

* The statistics subpage shall display statistics on charging station data and user data (*Note: These specific statistics shall be finalized when partnering with electric scooter companies and with further discussions with the engineering teams. Example statistics may include: Amount of energy saved by using charging stations, number of stations used this week, and miles traveled*).

#### 5.3.1.7 Rewards Subpage 

* The rewards subpage shall display within the user menu window when a user clicks on the "Rewards" button on the top of the user menu window.

* The rewards subpage shall display the rewards availble for a user to achieve in a list-like view.

* The rewards subpage shall display a progress bar under each reward tracking the progress to a reward.

* The rewards subpage shall feature a "Redeem" button under each reward for a user to redeem a reward, but will be greyed out and unclickable if the user has not yet achieved the reward.

* The rewards subpage shall feature a "View Reward" button under each reward for the user to view more details on the reward on click.

* The rewards subpage shall implement a page scrolling functionality within the user menu window.

#### 5.3.1.8 Heatmap Subpage

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

### 5.4.1 Graphical User Interface

#### 5.4.1.1 Login Page

* User shall be logged in within 5 seconds of entering their username and password.

* Main login screen shall be displayed within 3 seconds of opening the application.

#### 5.4.1.1 Home Page

* Location search results shall be returned within 3 seconds of query.

* The map shall pan and zoom instantaneously and smoothly in response to touch.

* The map shall load within 3 seconds of entering the home screen.

* The icons that designate the locations of charging stations and vehicles shall load within 2 seconds of loading the map.


## 5.5  Project Environment Requirements

### 5.5.1   Development Environment Requirements

The following sections outline the environment requirements for development of the iOS application. 

#### 5.5.1.1 Hardware Requirements

Category | Requirement
|--------|------------|
Hard Drive Space | 10GB
RAM | 4GB required, 8GB recommended
Display | 2,880 x 1,800 or smaller

#### 5.5.1.2 Software Requirements

Category | Requirement
|--------|------------|
Operating System | Mac OSX
IDE | Xcode
API | Coord API
API | React Native Maps API
Database | PostgreSQL
Database Manager | pgAdmin 4

### 5.5.2   Execution Environment Requirements

The following sections outline the environment requirements to run the application, assuming the application is running locally and not downloaded from the App Store.

#### 5.5.2.1 Hardware Requirements

Category | Requirement
|--------|------------|
Hard Drive Space | 500MB
RAM | 1GB
Display | 1242 x 2688 or smaller

#### 5.5.2.2 Software Requirements

Category | Requirement
|--------|------------|
Operating System | Mac OSX
Database | PostgreSQL

The application will run on Mac OSX with an iOS Simulator. 
