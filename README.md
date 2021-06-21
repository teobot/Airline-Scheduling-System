# Airline-Scheduling-System

## Project Information
*Unit title*: **Advanced Programming**  
*Project Language*: **Java**  
*Assignment set by*: **K. Welsh**  
*Assignment ID*: **1CWK50**  
*Assignment title*: **Airline Scheduling System**  
*Assessment weighting*: **50%**  
*Assessment Grade*: **🌟90%🌟**   
*Type*: (Group/Individual) **Individual**  
*Hand-in deadline*: **21:00 10th January 2020**  

## Table of Contents
- [Airline-Scheduling-System](#airline-scheduling-system)
  - [Project Information](#project-information)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [The System](#the-system)
    - [Introduction](#introduction-1)
    - [Exporting data from different file types](#exporting-data-from-different-file-types)
      - [Test Results](#test-results)
    - [Creating a scheduler](#creating-a-scheduler)
    - [Scheduler Competition](#scheduler-competition)
    - [Competition Prize Marks Table](#competition-prize-marks-table)
  - [Appendices](#appendices)
    - [Test Log](#test-log)
    - [Competition Scheduler Log](#competition-scheduler-log)

## Introduction
In this project, the task was to create the key components of a system that can plan which
plane an airline uses to fly passengers on each of their flights, and choose which pilots and cabin crew
are rostered for each flight. This is a simplified but representative version of a real problem faced by
airlines and other businesses. The University has consulted with several businesses in other sectors in
the region to develop this kind of software over recent years.

Because large aircraft weigh more and consume more fuel than smaller ones, airlines try to allocate
the smallest aircraft with enough seats to accommodate the booked passengers to a flight. Pilots and
cabin crew, however, are only qualified to operate certain types of aircraft. Such “type ratings” can
take a considerable amount of time and money to obtain, so it is rare for staff to be qualified to
operate all the types of aircraft that an airline may possess.

The rules governing how long and how often airline staff may work are complex and strict. They are
designed to ensure passenger safety, and are negotiated nationally and internationally between pilot
and cabin crew unions and government safety agencies. Thus, deciding which type of plane to fly on a
particular route on a particular day is a complex decision factoring in passenger demand, the
availability of aircraft, and the availability of qualified pilots and cabin crew.

This assignment simulates some of the constraints that could be found when working under when
developing software in industry. I was supplied with certain key interfaces to which my
software must conform, the system will have to operate on data supplied in various formats, as
if it were exported from separate existing, so-called legacy systems. I will have to use specific
libraries to complete the work.

## The System

### Introduction
The assignment is split into three sections:
- [Exporting data from different file types](#Exporting-data-from-different-file-types)  
- [Creating a scheduler](#Creating-a-scheduler) 
- [Scheduler Competition](#Scheduler-Competition) 

### Exporting data from different file types
The first part of the assignment was to take the different formats that legacy system could create and convert them to Java Objects. The following are the different types that were converted.
- Exporting Aircraft data from **CSV**
- Exporting Employee data from **JSON**
- Exporting Route data from **XML**
- Exporting Flight Booking data from **SQLite Database**

#### Test Results
Once the data was converted it was then tested against three different tests see **[HERE](#test-log)** for the complete test log.  
Here are the results from the tests below:
|             Section              | Tests Failed | Tests Passed |
| :------------------------------: | :----------: | :----------: |
|     Aircraft Data Exporting      |      0       |      16      |
|       Crew Data Exporting        |      0       |      17      |
| Passenger Numbers Data Exporting |      0       |      8       |
|       Route Data Exporting       |      0       |      17      |
|            Scheduler             |      0       |      2       |
|  **Schedule Competition Score**  | 985,379,178  |

### Creating a scheduler
This section required me to use all the exported data from the previous classes and write a new method that allocates and generates a schedule specifying which aircraft will be used on which route on which days, and which pilots and cabin crew will staff the flight.

For a schedule to be valid, every flight in the time period must be allocated a plane and a full crew.
A full crew is defined as a captain, first officer and at least the minimum number of cabin crew for
the aircraft type (see the getRequiredCrew() method in the Aircraft class). In addition, no crew
member or plane may be allocated to two flights at the same time (i.e. if any part of two flights
overlap).

### Scheduler Competition
The final marks on this assessment will be allocated by way of a competition. All students whose
work generates a valid schedule (i.e., with a plane and full crew scheduled to undertake each flight,
and no plane/crew in two places at once) will be entered into the competition. In the competition,
your scheduler will be allowed a maximum of two minutes to create the best schedule possible. Once
two minutes have elapsed, your scheduler will be stopped, and the best schedule it has created will be
assessed to generate a points score. 

Marks will be awarded as follows:
 
### Competition Prize Marks Table
|   Finishing Position    |  Marks   |
| :---------------------: | :------: |
| Bottom 50% of schedules | 5 Marks  |
|  Top 50% of schedules   | 7 Marks  |
|  Top 25% fo schedules   | 10 Marks |
|  Top 10% of schedules   | 15 Marks |

My submission was within the top 50% of the competition which throughout the whole year meant it was position in the top 4% as the competition has very hard to enter. 
Check [the TEST RESULTS](#test-results) for my scheduler competition score.

## Appendices
### Test Log
```
Running from Package. Source:
file:/D:/Marking/AdvProg/A1/Summative/X5d09f7ba/File%20submissions/AdvancedProgrammingAssessment1/bin/marker.jar
Testing Solution: .\solution
Starting Tests in section: Aircraft
Running Test: AircraftDAO Data Loading Test
Result: PASS
Running Test: AircraftDAO Presence Test
Result: PASS
Running Test: AircraftDAO Data Correctness Test
Result: PASS
Running Test: AircraftDAO Find Aircraft By Seats Test
Result: PASS
Running Test: AircraftDAO Find Aircraft By Starting Position Test
Result: PASSRunning Test: AircraftDAO Find Aircraft By Tailcode Test
Result: PASS
Running Test: AircraftDAO Find Aircraft By Type Test
Result: PASS
Running Test: AircraftDAO Number of Aircraft Test
Result: PASS
Running Test: AircraftDAO Nonexistent Path Test
Result: PASS
Running Test: AircraftDAO Null Path Test
Result: PASS
Running Test: AircraftDAO Malformed Data Test 1
Result: PASS
Running Test: AircraftDAO Malformed Data Test 3
Result: PASS
Running Test: AircraftDAO Malformed Data Test 2
Result: PASS
Running Test: AircraftDAO Multiple Load Test
Result: PASS
Running Test: AircraftDAO List Removal Test
Result: PASS
Running Test: AircraftDAO Reset Test
Result: PASS
Starting Tests in section: Crew
Running Test: CrewDAO Loading Test
Result: PASS
Running Test: CrewDAO Presence Test
Result: PASS
Running Test: CrewDAO Data Correctness Test
Result: PASS
Running Test: CrewDAO Find Cabin Crew By Home Base & Type Rating Test
Result: PASSRunning Test: CrewDAO Find Cabin Crew By Home Base Test
Result: PASS
Running Test: CrewDAO Find Cabin Crew By Type Rating Test
Result: PASS
Running Test: CrewDAO Find Pilots By Home Base & Type Rating Test
Result: PASS
Running Test: CrewDAO Find Pilots By Home Base Test
Result: PASS
Running Test: CrewDAO Find Pilots By Type Rating Test
Result: PASS
Running Test: CrewDAO Nonexistent Path Test
Result: PASS
Running Test: CrewDAO Null Path Test
Result: PASS
Running Test: CrewDAO Malformed Data Test 1
Result: PASS
Running Test: CrewDAO Malformed Data Test 2
Result: PASS
Running Test: CrewDAO Malformed Data Test 3
Result: PASS
Running Test: CrewDAO Multiple Load Test
Result: PASS
Running Test: CrewDAO List Removal Test
Result: PASS
Running Test: CrewDAO Reset Test
Result: PASS
Starting Tests in section: Passenger Numbers
Running Test: PassengerNumbersDAO Loading Test
Result: PASS
Running Test: PassengerNumbersDAO Presence TestResult: PASS
Running Test: PassengerNumbersDAO Non-Existant Flight Test
Result: PASS
Running Test: PassengerNumbersDAO Nonexistent Path Test
Result: PASS
Running Test: PassengerNumbersDAO Nonexistent Path Test
Result: PASS
Running Test: PassengerNumbersDAO Multiple Load Test
Result: PASS
Running Test: PassengerNumbersDAO Reset Test
Result: PASS
Running Test: PassengerNumbersDAO Malformed Data Test
Result: PASS
Starting Tests in section: Route
Running Test: RouteDAO Loading Test
Result: PASS
Running Test: RoutesDAO Presence Test
Result: PASS
Running Test: RouteDAO Data Correctness Test
Result: PASS
Running Test: RouteDAO Find Routes By Date Test
Result: PASS
Running Test: RouteDAO Find Routes By Day-Of-Week Test
Result: PASS
Running Test: RouteDAO Find Routes By Departure Airport & Day Test
Result: PASS
Running Test: RouteDAO Find Routes By Departure Airport Test
Result: PASS
Running Test: RouteDAO Nonexistent Path Test
Result: PASSRunning Test: RouteDAO Null Path Test
Result: PASS
Running Test: RouteDAO Malformed Data Test 1
Result: PASS
Running Test: RouteDAO Malformed Data Test 2
Result: PASS
Running Test: RouteDAO Malformed Data Test 3
Result: PASS
Running Test: RouteDAO Malformed Data Test 4
Result: PASS
Running Test: RouteDAO Malformed Data Test 5
Result: PASS
Running Test: RouteDAO Multiple Load Test
Result: PASS
Running Test: RouteDAO List Removal Test
Result: PASS
Running Test: RouteDAO Reset Test
Result: PASS
Starting Tests in section: Scheduler
Running Test: Schedule Generation Test
Result: PASS
Running Test: Scheduler Presence Test
Result: PASS
Done Testing
```
### Competition Scheduler Log
```
This solution is eligible for the scheduling competition.
Initialising DAOs...
Initialising Scheduler with dates: 2020-07-01 to 2020-08-31
Running Scheduler...
Finished Running Scheduler (took 6754ms)Quality score of generated schedule: 985,379,178
Quality Score Breakdown:
6,223,158 Points from allocating aircraft larger or smaller than the forecast passenger numbers
347,300 Points from aircraft schedules with short turnarounds
14,280,000 Points from scheduling aircraft to depart from airports other than where they last landed
81,694,000 Points from captains and first officers scheduled to fly in the wrong seat
546,150,000 Points from crew members scheduled to fly on aircraft types for which they are unqualified
86,240,000 Points for crew departing a UK airport without enough rest after their previous UK landing
9,300,000 Points for crew members not having a long break during each week in lieu of a weekend
6,172,500 Points for crew members not having enough rest before departing a UK airport other than their home
base
5,911,000 Points for crew members not having enough rest after landing at a UK airport other than their home
base
118,405,000 Points for flying to an airport outside the UK without an upcoming return flight
110,363,000 Points for flying from an airport outside the UK without having landed there recently
293,220 Points for crew members working more than their monthly limit
Competition Run Complete
```
