# Detailed Design Doc #
## Solar Scooter Project##

**2.1 – Project description**

**2.2 – Data Dictionary, meaning a bullet list of the final tables/columns with a complete description of each**

- Station info

| Station ID | Location Name? | Longitude | Latitude | Part IDs |
| --- | --- | --- | --- | --- |
| Unique ID that can be used as the primary key... might want to generate randomly for security reasons | Descriptive name of where the station is located (e.g. Lincoln and Manchester Station, Manhattan Beach Pier Station) | The geographical longitude of the stations location | The geographical latitude of the stations location | IDs of the solar panels which are associated with this station |

- Advertisement info (who the ad is from, info about ad content, dates it runs for, etc.)

| Ad ID | Company | Start date | End date | Station IDs |
| --- | --- | --- | --- | --- |
| Randomly generated unique ID | The company whom the ad belongs to | Day that the ad starts showing | Day that the ad ends showing | The stations which this particular ad will be displaying at |

- Bays

| Bay ID | Bay available | Vehicle ID |
| --- | --- | --- |
| Randomly generated unique ID | A simple true / false that indicates whether a scooter can be placed in that bay | The ID of the scooter that is currently parked in a bay (if there is one) |

- Vehicle

| Vehicle ID | Vehicle Type | Cost | Location | In Use |
| --- | --- | --- | --- | --- |
| Randomly generated unique ID | Scooter or Bike | Cost of the Vehicle to ride | Location of vehicle | Boolean indicating if scooter is in use  |

- Parts - every single part that is being used in a station

| Part ID | Part Number | Description | Station IDs | Purchase Date | Cost |
| --- | --- | --- | --- | --- | --- |
| Randomly generated unique ID | The official part number | What the part does / what it is for | The station each part is associated with | When the part was purchased | The cost of the part |

- Error Log

| Date | Error ID | Description | Station ID |
| --- | --- | --- | ---|
| Date of Occurrence | Error ID number maps to Error Table | Description of Error | Station ID |

- Errors

| Error ID | Error Name|
| --- | --- |
| Date of Occurrence | Error ID number maps to Error Table |

- History

| Scooter ID | Start Location | End location |
| --- | --- | --- |
| unique ID | starting location | end location after a ride |


**2.3 – Final ERD**

![ERD](./images/ERD2.png)
