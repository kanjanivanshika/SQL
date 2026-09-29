## ⚡ VOLTVISTA – EV CHARGING MANAGEMENT & ANALYTICS SYSTEM ##

## Scenario ##

VoltVista is a growing EV charging-network company that provides charging services to electric vehicle owners across different cities in India.

The company operates multiple charging stations, and each station provides different types of charging facilities such as AC, DC Fast Charging, and DC Ultra Fast Charging.

VoltVista wants to develop an EV Charging Management and Analytics System to store and analyze its daily charging operations in a structured database.

The system will maintain information about:

Customers
Vehicles
Charging Stations
Charging Sessions
Payments
Maintenance

The objective is to help management understand customer behavior, charging activity, station performance, revenue, energy consumption, and maintenance requirements.


## 1. 👤 Customers ##

VoltVista stores information about every customer using its charging network.

The system maintains:

Customer ID
Customer name
Email
Phone number
City
Registration date
Customer status

A customer can own one or more EVs and can perform multiple charging sessions.

| Column            | Data Type |
| ----------------- | --------- |
| customer_id       | INT       |
| customer_name     | VARCHAR   |
| email             | VARCHAR   |
| phone             | VARCHAR   |
| city              | VARCHAR   |
| registration_date | DATE      |
| customer_status   | VARCHAR   |

## 2. 🚗 Vehicles ##

Customers can register one or more electric vehicles with VoltVista.

The system stores:

Vehicle ID
Customer ID
Vehicle number
Vehicle model
Vehicle type
Battery capacity
Registration date

A customer can have multiple vehicles, while each vehicle belongs to one customer.

| Column               | Data Type |
| -------------------- | --------- |
| vehicle_id           | INT       |
| customer_id          | INT       |
| vehicle_number       | VARCHAR   |
| vehicle_model        | VARCHAR   |
| vehicle_type         | VARCHAR   |
| battery_capacity_kwh | DECIMAL   |
| registration_date    | DATE      |


## 3. ⚡ Charging Stations ##

VoltVista operates multiple charging stations across different cities.

For each station, the company stores:

Station ID
Station name
City
Area
Charger type
Number of connectors
Station status
Installation date

A charging station can handle many charging sessions.

| Column            | Data Type |
| ----------------- | --------- |
| station_id        | INT       |
| station_name      | VARCHAR   |
| city              | VARCHAR   |
| area              | VARCHAR   |
| charger_type      | VARCHAR   |
| total_connectors  | INT       |
| installation_date | DATE      |
| station_status    | VARCHAR   |


## 4. 🔋 Charging Sessions ##

Customers use VoltVista stations to charge their vehicles.

For every charging session, the system records:

Session ID
Customer
Vehicle
Charging station
Start time
End time
Energy consumed
Charging duration
Charging cost
Session status

One customer can perform many charging sessions.

One station can also have many charging sessions.

| Column                | Data Type |
| --------------------- | --------- |
| session_id            | INT       |
| customer_id           | INT       |
| vehicle_id            | INT       |
| station_id            | INT       |
| start_time            | DATETIME  |
| end_time              | DATETIME  |
| energy_consumed_kwh   | DECIMAL   |
| charging_duration_min | INT       |
| charging_cost         | DECIMAL   |
| session_status        | VARCHAR   |

## 5. 💳 Payments ##

VoltVista records payment information for completed charging sessions.

The system stores:

| Column         | Data Type |
| -------------- | --------- |
| payment_id     | INT       |
| session_id     | INT       |
| payment_date   | DATE      |
| payment_method | VARCHAR   |
| amount         | DECIMAL   |
| payment_status | VARCHAR   |



## 6. 🔧 Maintenance ##

VoltVista regularly performs maintenance on its charging stations.

The system records:

| Column           | Data Type |
| ---------------- | --------- |
| maintenance_id   | INT       |
| station_id       | INT       |
| maintenance_date | DATE      |
| issue_type       | VARCHAR   |
| downtime_hours   | DECIMAL   |
| maintenance_cost | DECIMAL   |
| status           | VARCHAR   |



📊 VOLTVISTA SQL PROJECT – BUSINESS ANALYSIS QUESTIONS

## A. Customer & Basic Analysis:
1. VoltVista wants to maintain a customer directory. Display complete details of all registered customers.

2. Management wants to know the different cities from which VoltVista customers are coming. Display unique customer cities.

3. Identify all customers whose current status is Active.

4. Find active customers who are currently registered in Mumbai.

5. Find customers who are registered in either Mumbai or Pune.

6. Identify customers who are registered in cities other than Mumbai.

7. Find customers who registered between two specified dates.

8. Identify customers belonging to Mumbai, Pune, Nashik, or Nagpur.

9. Find customers whose names begin with the letter A.

10. Identify customers whose email address is not available.

11. Identify customers who have a registered email address.

12. Display customers in alphabetical order based on customer name.

13. Identify the most recently registered customers.


## B. Customer Profile & Vehicle Analysis:
1. Identify customers who own at least one registered EV.

2. Find customers who own more than one vehicle.

3. Find customers using SUV vehicles.

4. Identify customers whose vehicle battery capacity is greater than 50 kWh.

5. Find customers using vehicles from a particular model.

6. Display the number of vehicles owned by each customer.

7. Identify cities having the highest number of registered EVs.

8. Find the most common vehicle type.

## C. Charging Station Analysis:

1. Display all charging stations along with city and area details.

2. Identify charging stations located in Maharashtra.

3. Find the number of charging stations operating in each city.

4. Calculate the number of charging connectors available at each station.

5. Identify stations having more than 5 charging connectors.

6. Find the station with the highest number of connectors.

7. Identify currently active charging stations.

8. Find stations using DC Fast Charging.

9. Find stations using DC Ultra Fast Charging.

10. Identify cities with more than 3 charging stations.

## D. Charging Activity Analysis:

1. Display all charging sessions along with customer, vehicle, station and charging details.

2. Identify customers who have completed at least one charging session.

3. Find customers who have performed more than 3 charging sessions.

4. Identify charging sessions where energy consumption is greater than 40 kWh.

5. Calculate the total energy consumed for each charger type.

6. Calculate the average energy consumed per charging session.

7. Calculate the total charging revenue generated by each station.

8. Find the station with the highest total charging revenue.

9. Find the average charging duration by charger type.

10. Identify the longest charging session.

11. Find the shortest charging session.

12. Identify charging sessions costing more than ₹500.

## E. Revenue & Payment Analysis

1. Display all payments along with their corresponding charging-session details.

2. Identify all successful payments.

3. Find payments made using UPI.

4. Calculate total revenue generated through each payment method.

5. Calculate the average payment amount for each payment method.

6. Find the highest-value payment.

7. Identify customers whose total charging expenditure exceeds ₹5,000.

8. Calculate total revenue generated by each city.

9. Find the city generating the highest charging revenue.

10. Calculate monthly charging revenue.

## F. Station Performance Analysis

1. Calculate the total number of charging sessions at each station.

2. Find the station with the highest number of charging sessions.

3. Calculate total energy consumption by station.

4. Find the station generating the highest revenue.

5. Calculate the average revenue per charging session for each station.

6. Identify stations having more than the average number of charging sessions.

7. Rank stations based on total revenue.

8. Rank stations based on charging-session volume.

## G. Maintenance Analysis 
1. Display all maintenance records along with station details.

2. Identify stations that have undergone maintenance.

3. Calculate total maintenance cost for each station.

4. Calculate total downtime for each station.

5. Find the station with the highest downtime.

6. Identify the most frequently occurring maintenance issue.

7. Calculate the average downtime by issue type.

8. Find stations where maintenance cost exceeds ₹10,000.

9. Identify stations requiring repeated maintenance.

10. Compare station charging activity with maintenance downtime.

## H. Customer Charging Behavior##

1. Identify customers whose total charging expenditure is greater than the average customer expenditure.

2. Identify customers who have completed more than 5 charging sessions.

3. Find customers who have both an active account and completed charging sessions.

4. Identify customers who own multiple EVs.

5. Find customers who have used more than one charging station.

6. Identify customers who have used both AC and DC chargers.

7. Find customers with the highest total energy consumption.

8. Identify customers who have spent more than ₹10,000 on charging.

## I. Consolidated EV Network Analysis##

1. Display each customer's name along with their vehicle and primary charging city.

2. Identify all registered customers and display their vehicle details, including customers who have not completed a charging session.

3. Generate a consolidated view showing:
Customer Name

Vehicle Model

City

Station Name

Charger Type

Energy Consumed

Charging Cost

Payment Status

5. Identify stations operating in the same city.

6. Display customer-wise:
Total Sessions

Total Energy Consumed

Total Amount Spent

6. Create a consolidated station performance view showing:

Station

City

Total Sessions

Total Energy

Total Revenue

Total Downtime

## J. Advanced SQL Analysis

1. Top 5 customers by total charging expenditure.
2. Top 5 stations by total revenue.
3. Rank cities based on charging revenue.
4. Rank stations based on charging-session volume.
5. Find customers whose spending is above the average customer spending.
6. Find stations whose revenue is above the average station revenue.
7. Calculate running monthly revenue.
8. Calculate month-over-month revenue.
9. Find the highest-revenue station in each city.
10. Find the most-used charger type in each city.

For these, we'll use:

JOIN

GROUP BY

HAVING

CASE
Subqueries
CTEs
RANK()
DENSE_RANK()
ROW_NUMBER()
Window Functions
