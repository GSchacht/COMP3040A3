## Winnipeg Transit
---
An API is an interface where the routines and features of a website or platform are provided. This document introduces the Winnipeg Transit which provides a way for you to retrieve live status and information according to your needs. It provides specifications for exchanging both static and real time public transit information, including information about stops, routes, schedule, service alerts, and other details. It documents resources, query parameters, response structures and data types. The Winnipeg Transit API has a number of endpoints shown below.

## List of Endpoints with Parameters

1. **ticketFair(age)**<br>
This endpoint takes in age of the user as it's parameter and returns the cost of the ticket which applies to that age group.
1. **peggoPass()** <br>
This endpoint returns all the information about different kinds of bus passes available.
1. **busInfo()** <br>
This endpoint returns information about all the busses, like their bus number, their start location and their destination

## Sample Request with Sample response

1) This is a sample request for ticketFair 

https://api.wpg-transit.org/ticketFair/json?age=76

Sample Response: 
```
"result" : {
    "id" : "1",
    "type" : "Senior Fare",
    "cash_price" : "2.50",
    "ticket_price" : "1.33",
    "monthly_pass_price" : "51.05"
},
"status" : "success"
```
2) Sample request and response to peggoPass()

https://api.wpg-transit.org/peggoPass/

Sample Response:
```
"result" : [
    {
        "id" : "1",
        "type" : "Reduced Fare",
        "colour" : "Green",
        "passenger_type" : [
            "Seniors",
            "Youth",
            "Student"
        ]
    },
    {
        "id" : "2",
        "type" : "Full Fare",
        "colour" : "White",
        "passenger_type" : [
            "Full-fare"
        ]
    }
],
"status" : "success"
```

3) Sample request request and response to getAllBusRoutes()

https://api.wpg-transit.org/getAllBusRoutes/

Sample Response:
```
"results" : [
    {
        "id" : "1"
        "bus_number" : "74",
        "route_name" : "Kenaston"
        "start_location" : "Polo Park", 
        "end_location" : "University of Manitoba"
    },
    {
        "id" : "2"
        "bus_number" : "75",
        "route_name" : "Crosstown East"
        "start_location" : "Kildonan Place", 
        "end_location" : "university of Manitoba"
    },
    {
        "id" : "3"
        "bus_number" : "77",
        "route_name" : "Crosstown North"
        "start_location" : "Polo Park", 
        "end_location" : "Kildonan Place"
    },
    {
        "id" : "4"
        "bus_number" : "78",
        "route_name" : "Waverly"
        "start_location" : "Polo Park", 
        "end_location" : "Universty of Manitoba"
    },
    {
        "id" : "5"
        "bus_number" : "79",
        "route_name" : "Charleswood"
        "start_location" : "Polo Park", 
        "end_location" : "Westdale"
    }
],
"status" : "success"
```
