# Airline Database Analysis | PostgreSQL

### 1. Project Overview

As part of my capstone project, I worked on an **Airline Database Analysis Project Using SQL** to derive meaningful insights from airline operations, flight schedules, passenger bookings, aircraft utilization, and financial transactions.

The project involved writing and optimizing SQL queries to solve real-world airline management challenges. I used SQL concepts such as Common Table Expressions (CTEs), window functions, joins, aggregations, subqueries, and date-time functions to analyze data and support data-driven decision-making.

### 2. Objectives

- Analyze passenger booking patterns and identify high-value customers.
- Examine flight schedules, delays, cancellations, and route performance.
- Evaluate seat allocation and aircraft utilization.
- Calculate booking revenue and identify passengers eligible for refunds.
- Analyze airport performance and aircraft range.
- Apply advanced SQL techniques to solve practical business questions.

### 3. Tools and Technologies

- **Database:** PostgreSQL
- **Query Language:** SQL
- **SQL Concepts:** Joins, CTEs, subqueries, aggregations functions, window functions, logical/arithmetic operations and date-time functions
- **Analysis Techniques:** Ranking, filtering, grouping, revenue analysis, and query optimization

### 4. Key Contributions and Responsibilities

#### 4.1 Data Exploration and Query Optimization
- Explored airline database tables to understand their structure and relationships.
- Wrote SQL queries using CTEs, window functions, and aggregate functions.
- Applied joins, subqueries, and conditional filters to retrieve relevant information.
- Improved query readability and worked on efficient data retrieval.

#### 4.2 Passenger and Booking Analysis
- Identified high-value passengers based on booking amounts.
- Analyzed monthly passenger spending and revenue contributions.
- Examined passenger journeys involving multiple flights.
- Identified bookings without boarding passes.
- Formatted booking dates and analyzed passenger booking patterns.

#### 4.3 Flight Operations Analysis
- Identified the longest flights and analyzed scheduled flight timings.
- Examined morning flights and the earliest morning flights departing from each airport.
- Identified the first and last scheduled flights from each airport on different dates.
- Analyzed delayed and cancelled flights.
- Investigated departure patterns and flight availability between airports.

#### 4.4 Seat and Aircraft Utilization
- Identified the least-allocated seat numbers.
- Analyzed seat counts across different fare conditions for each aircraft.
- Identified aircraft types offering business-class seats.
- Examined aircraft range and aircraft utilization patterns.

#### 4.5 Revenue and Refund Analysis
- Calculated booking amounts and analyzed passenger spending.
- Identified passengers eligible for refunds because of flight cancellations.
- Calculated refund amounts based on the applicable booking and cancellation rules.
- Examined how flight cancellations can affect airline revenue.

#### 4.6 Airport and Route Analysis
- Identified airports with the highest and lowest numbers of scheduled departures.
- Analyzed flight counts from selected departure airports.
- Examined flight connections between specific airport pairs.
- Identified airports operating in the Europe/Moscow time zone.
- Investigated cancelled arrivals and aircraft range requirements.

### 5. SQL Business Questions and Queries

The project covers the following 29 SQL questions. Each question should be documented with its PostgreSQL query and the corresponding result.

#### 5.1 Booking and Passenger Analysis

**Question 1: Booking Date Formatting**

Represent the `book_date` column in the `bookings` table in `YYYY-Mon-DD` format.

**Expected output:** `book_ref`, formatted `book_date`, `total_amount`.

**Question 2: Passenger and Boarding Information**

Retrieve the following columns in the exact order specified:

- `ticket_no`
- `boarding_no`
- `seat_number`
- `passenger_id`
- `passenger_name`

**Question 3: Monthly Highest-Paying Passenger**

Identify the passenger who paid the highest total amount in each month.

**Expected output:** Month in `Mon-YY` format, passenger ID, passenger name, and total amount.

**Question 4: Monthly Lowest-Paying Passenger**

Identify the passenger who paid the lowest total amount in each month.

**Expected output:** Month in `Mon-YY` format, passenger ID, passenger name, and total amount.

**Question 5: Passengers with Multiple-Flight Journeys**

Identify passengers with journeys involving more than one flight.

**Expected output:** Passenger ID, passenger name, ticket number, and flight count.

**Question 6: Tickets Without Boarding Passes**

Count the number of tickets that do not have boarding passes.

**Expected output:** A single count value.

#### 5.2 Seat and Aircraft Analysis

**Question 7: Least-Allocated Seat**

Find the seat number that has been allocated the least across the available seat records or boarding-pass records, according to the chosen definition of allocation.

**Expected output:** Seat number and allocation count.

**Question 8: Seat Count by Aircraft and Fare Condition**

Calculate the number of seats available for each fare condition for every aircraft code.

**Expected output:** Aircraft code, fare condition, and seat count.

**Question 9: Aircraft with Business-Class Seats**

Count the aircraft codes that have at least one business-class seat.

**Expected output:** Count of aircraft codes.

#### 5.3 Flight Schedule and Operations Analysis

**Question 10: Longest Flight**

Identify the longest flight using the `flights` table.

**Expected output:** Flight number, departure airport, arrival airport, aircraft code, and flight duration.

**Question 11: Morning Flights**

Identify flights scheduled between 6:00 AM and 11:00 AM.

**Expected output:** Flight ID, flight number, scheduled departure, scheduled arrival, and flight duration or timing information.

**Question 12: Earliest Morning Flight from Every Airport**

Identify the earliest morning flight departing from each airport.

**Expected output:** Flight ID, flight number, scheduled departure, scheduled arrival, departure airport, and timing information.

**Question 13: Flights Without Actual Departure**

Count the flights departing from airport `DME` that do not have an actual departure recorded.

**Expected output:** Flight count.

**Question 14: Flights with Aircraft Range Between 3,000 and 6,000**

Identify flights whose aircraft have a range between 3,000 and 6,000.

**Expected output:** Flight number, aircraft code, and aircraft range.

**Question 15: Flights Between URS and KUF**

Count the flights operating between airports `URS` and `KUF`.

**Expected output:** Flight count.

**Question 16: Flights Departing from NOZ or KRR**

Count the flights departing from either `NOZ` or `KRR`.

**Expected output:** Flight count.

**Question 17: Departure Counts from Selected Airports**

Calculate the number of departing flights from `KZN`, `DME`, `NBC`, `NJC`, `GDX`, `SGC`, `VKO`, and `ROV`.

**Expected output:** Departure airport and flight count.

**Question 18: Aircraft Range Between 3,000 and 6,000 from DME**

Identify flights departing from `DME` that use aircraft with a range between 3,000 and 6,000.

**Expected output:** Flight number, aircraft code, aircraft range, and departure airport.

**Question 19: Date-Wise Last Flight from Every Airport**

Identify the last scheduled flight departing from each airport on each date.

**Expected output:** Flight ID, flight number, scheduled departure, and departure airport.

**Question 20: Date-Wise First Cancelled Flight from Every Airport**

Identify the first cancelled flight from each airport on each date.

**Expected output:** Flight ID, flight number, scheduled departure, and departure airport.

#### 5.4 Airport and Route Performance Analysis

**Question 21: Airports in the Europe/Moscow Time Zone**

Retrieve the airport codes for airports using the `Europe/Moscow` time zone.

**Expected output:** Airport code.

**Question 22: Airport with the Most Departures**

Identify the airport name with the highest number of departing flights.

**Expected output:** Airport name.

**Question 23: Airport with the Fewest Scheduled Departures**

Identify the airport name with the lowest number of scheduled departures.

**Expected output:** Airport name.

**Question 24: Airport with the Most Cancelled Arrivals**

Identify the airport receiving the highest number of cancelled arriving flights.

**Expected output:** Airport name.

### 5.5 Cancellation, Refund, and Aircraft Manufacturer Analysis

**Question 25: Cancelled or Delayed Airbus Flights**

Identify flight IDs operated using Airbus aircraft that were cancelled or delayed.

**Expected output:** Flight ID and aircraft model.

**Question 26: Cancelled or Delayed Boeing Flights**

Identify flight IDs operated using Boeing aircraft that were cancelled or delayed.

**Expected output:** Flight ID and aircraft model.

**Question 27: Passengers Eligible for Refunds**

Identify passengers eligible for refunds because of flight cancellations and calculate the total refund amount for each passenger.

**Expected output:** Passenger name and total refund.

**Question 28: Cancelled Airbus Flights**

Identify flight IDs operated using Airbus aircraft that were cancelled.

**Expected output:** Flight ID.

**Question 29: Aircraft with the Highest Range**

Identify the flight or aircraft records associated with the highest aircraft range.

**Expected output:** Flight number and aircraft range.

### 6. Key Findings and Business Impact

- Extracted more than 30 business insights from the project analysis.
- Investigated passenger spending patterns and monthly booking contributions.
- Examined flight delays, cancellations, departure schedules, and airport performance.
- Analyzed aircraft range, seat allocation, and business-class availability.
- Investigated cancellation-related refunds and their financial implications.
- Practiced writing structured SQL queries to support business analysis.

### 7. Challenges and Learning Outcomes

During this project, I strengthened my ability to:

- Understand relational database structures and table relationships.
- Write SQL queries involving multiple joins and nested conditions.
- Use CTEs and window functions for ranking and analytical calculations.
- Work with timestamps, date formatting, and flight duration calculations.
- Analyze missing boarding passes, cancellations, and refund eligibility.
- Translate business questions into structured SQL queries.

### 8. Business Recommendations

Based on the verified findings, the analysis can help identify opportunities to:

- Review flight schedules and departure patterns at busy airports.
- Investigate delays and cancellations to improve operational planning.
- Monitor aircraft and seat utilization to support capacity planning.
- Improve passenger communication and refund processing.
- Analyze monthly booking patterns to support revenue planning.

These recommendations should be refined according to the actual query results.

### 9. Conclusion

This Airline Database Analysis project provided practical experience in using PostgreSQL to investigate airline operations, passenger bookings, flight schedules, aircraft utilization, and financial transactions.

It strengthened my SQL skills and analytical thinking while demonstrating how database queries can help answer business questions and support data-driven decision-making.
