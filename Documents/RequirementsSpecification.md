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

### 5.2.1 Graphical User Interface Client

The Graphical User Interface (GUI) is the interface the user will be interacting with. The GUI will be composed of the following CSUs.

#### 5.2.1.1 Main Page CSU

#### 5.2.1.2 Charging Station Preview CSU

#### 5.2.1.3 Charging Station Menu CSU

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



### 5.3.2 Database


## 5.4  Performance Requirements by CSC

## 5.5  Project Environment Requirements

#### 5.5.1   Development Environment Requirements

#### 5.5.2   Execution Environment Requirements

