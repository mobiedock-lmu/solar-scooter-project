# 8.0    Software Test Plan
## 8.1    Introduction

This test plan document covers all the tests that will be uses to do testing on the MobieDock App, and covers all levels of the testing process that will be performed.

### 8.1.1 Format

The document is formatted as follows: 
```
 8.1    Introduction
 8.2    Unit Test Plan
 8.3    Integration Test Plan
 8.4    Acceptance Test Plan
 8.5    Test Configuration Control
 8.6    Items Not Tested
 8.7    Test Verification Matrix
```
## 8.2    Unit Test Plan
The test and integration plan provides an overview of the testing framework and specific tests that will be used to assess the functionality of our application.  Since the desired outputs for front-end and back-end components are known, a white-box approach will dictate the approach to testing.  React Native is an extension of Javascript, so the time-proven [Jest](https://jestjs.io/) will be used in combination with [Enzyme](https://airbnb.io/enzyme/) in order to assess correct implementation of the actual code components.
### 8.2.1 Unit Test Descriptions
  **Login Test** ensures that the user can properly sign in with Google.
  **Map Test** ensures that a React-Native map opens on the users location and can be manipulated with various gestures.
  **Search Test** ensures that locations can be searched and displayed from the map screen.
  **Menu Test** ensures that the user can use the menu to navigate to all pages in the app.
  **Profile Test** ensures that the user can edit their profile and sign out.
  **Vehicle Display Test** ensures that the electric mobility devices can be seen and filtered from the map screen, and that relevant data is accurate.
### 8.2.1.1 Login Test
The following procedure tests that the user has a unique profile and login:
  1. Open a fresh install of the application.
  2. Under "Create an Account", enter your information.
  3. Use that information to log in.
  3. Verify that you now have full access to the application.
### 8.2.1.2 Map Test
The following procedure tests that the map interface works as intended:
  1. Open the Mobiedock application.
  2. Verify that a map is showing upon application startup, and the map is centered on the user's current location, which is indicated by a blue dot.
  3. Scroll with a single finger or thumb to verify that the surrounding area can be viewed.
  4. Pinch to verify that zooming works.
### 8.2.1.3 Search Test
The following procedure tests that the user can properly search for a location:
  1. From the map screen, select the search bar in the upper part of the screen, and verify that the map has not moved or changed appearance.
  2. Verify that a keyboard is now displayed on the lower half of the screen.
  3. Search for a nearby location, and verify that the map pans to that location's surrounding area and drops a pin on the specific coordinates.
### 8.2.1.4 Menu Test
  1. Select the circular menu indicator near the bottom of the screen.  Verify that the menu expands, allowing access to the "map", "incentives", "settings", and "management" pages.
  2. Click on each of the icons to ensure that selection brings the user to the proper page.  Also verify that the page you are on is grayed out in the menu.
  3. From any page, swipe left from the left side of the screen or right from the right side of the screen to ensure that you can also navigate between pages this way.
### 8.2.1.5 Profile Settings Test
  1. From the top left of any screen, select the icon to open the drawer navigator.
  2. From there, navigate to profile settings.
  3. Verify that you may log out, and are taken back to the login page.
  4. Click "Change profile picture".
  5. Verify that you may upload or take a new profile picture.
  6. Click "Change password".
  7. Verify that you may change your password.
  8. Click "Change email address".
  9. Verify that you may change your email address.
### 8.2.1.6 Vehicle Display Test
  1. From the map screen, select company logos displayed on the left side of the screen.
  2. Verify that the desired company vehicles are shown on the map when their logo is highlighted in the list on the left.
  3. Select a couple of vehicles on the map to verify that their charge amount and distance away is correct.

## 8.3    Integration Test Plan
 **App Settings Test** ensures that iOS and map settings can be manipulated from this page.
  **Trip Test** simulates a scooter/bike trip and ensures that location tracking is accurate.
  **Management Test** ensures that station maintenance is possible through the station directory.
  **Incentives Ranking Test** ensures that the Bayesian network algorithm properly determines which station visits should be incentivized the most.
### 8.3.1 Integration Test Descriptions
#### 8.3.1.1 App Settings Test
  1. Use the menu to navigate to the "settings" page.
  2. Toggle the "notifications" and "location" settings off and back on.  Verify that you get an iOS prompt to allow the app to use your location and send notifications.
  3. Use the "Vehicle radius" setting to change the radius that the app searches for nearby vehicles.  Verify that changing this setting is reflected in the map.
#### 8.3.1.2 Trip Test
  1. Select the "take a trip" button from the map screen.
  2. Search for a location or drop a pin and confirm.
  3. Verify that the map now shows a recommended route, distance away, and estimated time of travel.
#### 8.3.1.3 Management Test -- DEPRECATED AS OF 01/19. WILL BE MIGRATED TO A SEPARATE ADMIN TOOL
  1. Use the menu to navigate to the "management" page.
  2. Ensure that the scrollable interface includes stations within the radius specified in the "settings" page.
  3. Select a station to verify that the following metrics are visible: solar efficiency, distance away, level of pedestrian traffic, and number of bays available.
  4. Navigate back to the main "management" page and use the search bar at the top to verify that you may search for a station by name or location.
#### 8.3.1.4 Incentives Ranking Test
  1. Use the menu to navigate to the "incentives" page.
  2. Verify that an ordered list of 10 stations is show.
  3. Using the "management" page, verify that the stations with highest incentives need more scooters, are in locations with high pedestrian traffic, and are somewhat nearby the user's desired location.

## 8.4    Acceptance Test Plan
In order to fully demonstrate that our application works as intended, we'll want to walk the user through booking a simple scooter / bike trip.  This will require them to:
- Create an account
- Login
- Search for a location
- Plan a trip to that location by searching for nearby scooters and / or charging stations
- Indicate that their trip is complete and lock up their vehicle in the bay at their end location.
### 8.4.1  Acceptance Tests Planned
- 8.2.1.1 Login / Create an account
- 8.2.1.2 Utilize the map
- 8.2.1.3 Search for a location that they would like to travel to
- 8.2.1.6 Find nearby free-standing or docked vehicles from the map
- 8.3.1.2 Plan a trip, and use the app to end the trip and subsequently dock the scooter.
### 8.4.2  Final Acceptance Test Procedures
Guide a user through the entire process of booking and completing a round-trip scooter excursion (after creating a Mobiedock account and loggin in):
- The trip should involve at least 4 total miles of travel.
- On the way there, have the user choose any scooter or bike that is near them (undocked).
- Plan the trip from that scooter to a charging station that is at least 2 miles away.
- Once unlock the scooter from the app, verify that the trip has started.
- When they arrive at their destination, have them end the trip from the app and lock up the scooter.
- Now, they will start a new trip from the charging station to their original location.
- Once again, they will unlock a scooter from the app, remove it from station, and ride to their original location.
- When they arrive, they will end the ride from the app.
- After all is said and done, verify that the distance traveled, trip history, and any associated charges are correct.
## 8.5    Test Configuration Control
## 8.6    Items Not Tested
### 8.6.1 Coord API Locations
As of December 2018, The Coord API has been disabled and removed, making us unable to test specific locations of Scooters and e-Bikes. 
### 8.6.2 Charging Dock Locations & Data
As of February 2019, the engineering team has not created a prototype with location tracking abilities or data output that we can recieve on the software side.
## 8.7    Test Verification Matrix
Requirement # | Element | Test Description
:-------:|:-------:|:-----:
1 | Login Page|
2 | Home page|
3 | Charging station menu|
4 | User Menu|
5 | Location Search |