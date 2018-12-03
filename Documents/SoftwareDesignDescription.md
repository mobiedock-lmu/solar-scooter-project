# Software Design Description

## 6.1 Introduction

MobieDock is a mobile iOS application that will allow users to locate and interact with solar powered charging stations for electric scooters, which will be installed in the Los Angeles area. The application will be built using React Native, will contain a PostgreSQL Database, and will be a stand alone application. Future plans are developing to integrate with Bird and Lime scooter applications.  

### 6.1.1     System Objectives

MobieDock will allow users to interact with and locate nearby charging locations for their electric scooter or bike rented through Bird, Lime, or similar services. Users can see how many bays are avilable and reserve bays through the application. Users can earn incentives and rewards for using the charging stations, and can see statistics on how much energy they are saving. Companies can work with MobieDock to place rewards or advertisements on the app, and electric scooter companies can access charging station data. 

### 6.1.2     Hardware, Software, and Human Interfaces

#### 6.2.1 Hardware 

The application will run on will mainly be iOS devives, but future plans are developing to optimize for Android as well.

#### 6.2.2 Software 

The Front End of the application will be built using React Native. The Back End of the application will contain a PostgreSQL Database which will record and track relevant data such as bay and charging station data, error logs, and advertisement data (See Section 6.4 for more details).

#### 6.2.3 Human Interfaces

##### Figure 1: Bird - Station Status Example 1
<img src="./images/homescreen-mockup.png" height="400">

##### Figure 2: Lime - Station Status Example 2
<img src="./images/Lime_station_status_mockup.png" height="400">

##### Figure 3: Bird - Incentive Tracking
<img src="./images/Bird_incentive_tracking_mockup.png" height="400">

## 6.2       Architectural Design

### 6.2.1     Major Software Components

### 6.2.2     Major Software Interactions

### 6.2.3     Architectural Design Diagrams

## 6.3.      CSC and CSU Descriptions

### 6.3.1     Class Descriptions

#### 6.3.1.1   Detailed Class Description 1

#### 6.3.1.n   Detailed Class Description n

### 6.3.2     Detailed Interface Descriptions

### 6.3.3     Detailed Data Structure Descriptions

### 6.3.4     Detailed Design Diagrams


## 6.4       Database Design and Description

### 6.4.1     Database Design ER Diagram

#### ERD

![ERD](/Databases/images/ERD-final.png)

#### DATA DICTIONARY

#### Charging Station

| Station ID | Model Number | Available Bays | Last Maintenance Date | Location ID | Solar Efficiency |
| --- | --- | --- | --- | --- | --- |
| Unique ID that can be used as the primary key... might want to generate randomly for security reasons | The model of this particular station (we'll probably have 2-3 models) | The number of open bays at this station | The last date this station was maintenanced | ID connecting to the Locations table | Solar output (as a percentage) |

#### Locations

| Location ID | Longitude | Latitude |
| --- | --- | --- |
| Randomly generated unique ID | Longitude of station location | Latitude of station location |

#### Advertisement info (who the ad is from, info about ad content, dates it runs for, etc.)

| Ad ID | Company | Start date | End date | Station ID(s) |
| --- | --- | --- | --- | --- |
| Randomly generated unique ID | The company whom the ad belongs to | Day that the ad starts showing | Day that the ad ends showing | The stations which this particular ad will be displaying at |

#### Ad Company info

| Company | Phone Number | Ad ID | Station ID(s) |
| --- | --- | --- | --- |
| Company Name | Phone number/contact info for company | Randomly generated unique ID| The stations which this particular ad will be displaying at |

#### Bays

| Bay ID | Availability | Station ID |
| --- | --- | --- |
| Randomly generated unique ID | Boolean indicating whether a scooter can be placed in that bay | Unique ID of the station the bay belongs to|

#### Station Model info

| Station ID | Model Number | Parts | Total Bays |
| --- | --- | --- | --- |
| Randomly generated unique ID | Model Number | connects to Parts Table | Total Number of Bays |

#### Vehicle

| Vehicle ID | Vehicle Type | Cost | Location | In Use |
| --- | --- | --- | --- | --- |
| Randomly generated unique ID | Electric scooter, electric bike, or manual bike | Cost of the Vehicle to ride | Location of vehicle | Boolean indicating if scooter is in use |

#### Parts

| Serial Number | Part name | Model(s) | Purchase Date | Cost |
| --- | --- | --- | --- | --- |
| Can be used as primary key | Helps describe the part | The station models the part is used in | When the part was purchased | The cost of the part |

#### Error Log

| Date | Error ID | Description | Station ID |
| --- | --- | --- | ---|
| Date of Occurrence | Error ID number maps to Error Table | Description of Error | Station the error occurred at |

#### Errors

| Error ID | Error Name |
| --- | --- |
| Date of Occurrence | Type of error that occurred |

#### Ride History

| Scooter ID | Start Location | End location | Ride Duration |
| --- | --- | --- | --- |
| ID of the scooter for this entry | Ride start location | Ride end location | Ride duration |


### 6.4.2     Database Access

### 6.4.3     Database Security
