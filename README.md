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

Table: customers
Column	Data Type
customer_id	INT
customer_name	VARCHAR
email	VARCHAR
phone	VARCHAR
city	VARCHAR
registration_date	DATE
customer_status	VARCHAR

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

Table: vehicles
Column	Data Type
vehicle_id	INT
customer_id	INT
vehicle_number	VARCHAR
vehicle_model	VARCHAR
vehicle_type	VARCHAR
battery_capacity_kwh	DECIMAL
registration_date	DATE
Vehicle types
Hatchback
Sedan
SUV

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

Table: charging_stations
Column	Data Type
station_id	INT
station_name	VARCHAR
city	VARCHAR
area	VARCHAR
charger_type	VARCHAR
total_connectors	INT
installation_date	DATE
station_status	VARCHAR
Charger types
AC
DC Fast
DC Ultra Fast

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

Table: charging_sessions
Column	Data Type
session_id	INT
customer_id	INT
vehicle_id	INT
station_id	INT
start_time	DATETIME
end_time	DATETIME
energy_consumed_kwh	DECIMAL
charging_duration_min	INT
charging_cost	DECIMAL
session_status	VARCHAR

## 5. 💳 Payments ##

VoltVista records payment information for completed charging sessions.

The system stores:

Payment ID
Session ID
Payment date
Payment method
Amount
Payment status
Table: payments
Column	Data Type
payment_id	INT
session_id	INT
payment_date	DATE
payment_method	VARCHAR
amount	DECIMAL
payment_status	VARCHAR
Payment methods
UPI
Credit Card
Debit Card
Wallet

## 6. 🔧 Maintenance ##

VoltVista regularly performs maintenance on its charging stations.

The system records:

Maintenance ID
Station ID
Maintenance date
Issue type
Downtime hours
Maintenance cost
Maintenance status
Table: maintenance
Column	Data Type
maintenance_id	INT
station_id	INT
maintenance_date	DATE
issue_type	VARCHAR
downtime_hours	DECIMAL
maintenance_cost	DECIMAL
status	VARCHAR
