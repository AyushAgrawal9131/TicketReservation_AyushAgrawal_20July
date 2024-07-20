# TicketReservation_AyushAgrawal_20July
Bus ticket Reservation System

Admin Register and login :-- 
POST :localhost:8080/admin/register - register as admin , you will get a key , for admin related requests you need to give that key (aid)
PUT : localhost:8080/admin/update - you can update the admin credentials

POST :localhost:8080/admin/login - you can login after register as login with key
POST : localhost:8080/admin/logout - you can logout as admin 


Admin specific apis - admin can add the bus,update the details of the bus and delete the bus with the help of busId
POST : localhost:8080/admin/bus/add 
PUT: localhost:8080/admin/bus/update
DELETE : localhost:8080/admin/delete/{busId}


these are general api's - anybody can use them (user and admin both)
GET: localhost:8080/bus/all   -- used to see all the bus registered 
GET : localhost:8080/bus/{busId} -- details of a specific bus with busId
GET: localhost:8080/bus/type/{busType} -- fetch the buses with BusType(Ex: Ac buses,non-ac buses)

user specific API Endpoints : 

POST: localhost:8080/user/register - used for registering a user ,you will get a key ,which you have to use for user related requests 
PUT: localhost:8080/user/update - used to update the login credentials of user 
POST: localhost:8080/user/login - used to login as user after registering 
POST: localhost:8080/user/logout - used to logout as a user



API's related to bus route : --- 

POST: localhost:8080/admin/route/add - after login admin can add the route of bus (ex: delhi to gurugram )
PUT: localhost:8080/admin/route/update - admin can update the bus route details
DELETE: localhost:8080/admin/route/delete/{routeId} - admin can delete the route with routeId

GET: localhost:8080/route/all - anybody can see all the routes of the buses
GET: localhost:8080/route/{routeId} - anybody can check the specific bus route details with routeId


Admin Permission related API endpoints : --- 

DELETE: localhost:8080/admin/user/delete/{userId} - admin can delete a particular user 
GET: localhost:8080/admin/user/{userId} - admin can view any user with userId
GET: localhost:8080/admin/user/all - admin can view all the users 


API endpoints related to Reservation in the bus :---

POST :localhost:8080/user/reservation/add - user can reserve the seat in the bus if seat is available 
PUT: localhost:8080/user/reservation/update - user can udpate the reservation details 
DELETE : localhost:8080/user/reservation/delete/{rid} -user can delete its reversation with reservation id
GET : localhost:8080/reservation/{rid} - anybody can see the reservation details with reservation id
GET :localhost:8080/reservation/all - anybody can see all the reservations done 
GET: localhost:8080/user/reservation/{uid} - user can see its reservation in the bus with userId


dummy values : 
Bus: 
{
       "busName": "16thBus",
       "driverName": "yash",
       "busType": "ac",
       "routeFrom": "mumbai",
       "routeTo": "lucknow",
       "busJourneyDate": "2023-05-08",
       "arrivalTime":"09:00:00",
       "departureTime":"12:00:00",
       "seats": 35,
       "availableSeats": 35,
       "fare": 350,
       "route": {
       "routeFrom": "a",
       "routeTo": "b",
       "distance": 2000
       }
}



Route :
{
   "routeId":"3",
   "routeFrom":"Delhi",
   "routeTo": "Noida",
   "distance" : "200"
}





