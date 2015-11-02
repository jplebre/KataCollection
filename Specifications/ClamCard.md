# Specification
Implement a system for a contactless travel card for the London underground.

* The card does not need to be topped up.
* The card charges the owner's bank account directly when used.
* The card is used by touching in and out at train stations.
* The train system accepting this card has two categorical zones of stations, Zone A and Zone B.
* The stations within the zones are as follows:

|Zone A         |     Zone B     |
|---------------|----------------|
|Asterisk       |     Bison      |
|Antelope       |     Bugel      |
|Aldgate        |     Balham     | 
|Angel          |     Bullhead   |
|Aldgate East   |     Barbican   |

* Travelling within zone B is more expensive than travelling in Zone A.
* The price of zone B is inclusive of travelling within zone A.
* If one of the stations is within Zone 2 at any point in a journey, the price for zone 2 will be charged.
* The fares are as described below:

|  Zone  |  Single  |   Day   |    Week    |     Month   |
|--------|----------|---------|------------|-------------|
| ZoneA  |  £2.50   |  £7.00  |   £40.00   |    £145.00  |
| ZoneB  |  £3.00   |  £8.00  |   £47.00   |    £165.50  |

* A Single is a journey from one station to another.
* A Day fare includes all single journies made within a single day.
* A Week fare includes all single journies made within a single week.
* A month fare includes all single journies made within a single month.
* No matter how many journies are made within one of the time boundaries within a particular zone, the price will cap at that time period's fare.

# USE CASE SCENARIOS:

**Scenario:** One-Way Zone 1 Journey<br>
  Given Michael has an Oyster Card<br>
  And Michael travels from Asterisk to Aldgate<br>
  Then Michael will be charged £2.50 for his journey<br>

**Scenario:** One-Way Zone 1 to Zone 2 Journey<br>
  Given Michael has an Oyster Card<br>
  And Michael travels from Asterisk to Barbican<br>
  Then Michael will be charged £3.00 for his journey<br>

**Scenario:** Multiple journeys<br>
  Given Michael has an Oyster Card<br>
  And Michael travels from Asterisk to Barbican<br>
  And Michael travels from Barbican to Balham<br>
  Then Michael will be charged £3.00 for his journey<br>
  And a further £3.00 for his second journey<br>

**Scenario:** Multiple journeys reaching daily cap<br>
  Given Michael has an Oyster Card<br>
  And Michael travels from Asterisk to Barbican<br>
  And Michael travels from Barbican to Balham<br>
  And Michael travels from Balham to Bison<br>
  And Michael travels from Bison to Asterisk<br>
  Then Michael will be charged £3.00 for his journey<br>
  And a further £3.00 for his second journey<br>
  And a further £2 for his third journey<br>
  And a further £0.00 for any additional journies within the day<br>


# BONUS Scenario: 

Take into account for return journies, the new fares are as described below:

|  Zone  |  Single  |   Day   |    Week    |     Month   |
|--------|----------|---------|------------|-------------|
| ZoneA  |  £4.50   |  £8.50  |   £38.00   |    £120.00  |
| ZoneB  |  £5.50   |  £9.50  |   £47.00   |    £152.50  |

* A Single is a journey from one station to another.
* A Return is a single journey where the next immediate journey is the inverse of the previous journey.
* Travelling from station A to station B, then from Station B to station A, classifies as a return.
* A Day fare includes all single and return journies made within a single day.
* A Week fare includes all single and return journies made within a single week.
* A month fare includes all single and return journies made within a single month.
        
        
**Scenario:** Multiple Return Journeys<br>
  Given Michael has an Oyster Card<br>
  And Michael travels from Asterisk to Barbican<br>
  And Michael travels from Barbican to Asterisk within the same day<br>
  And Michael travels from Asterisk to Balham within the same day<br>
  And Michael travels from Balham to Asterisk within the same day<br>
  Then Michael will be charged £3.00 for his journey<br>
  And a further £2.50 for his second journey<br>
  And a further £3.00 for his third journey<br>
  And a further £1.00 for his final journey<br>
