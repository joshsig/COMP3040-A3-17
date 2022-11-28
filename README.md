Find Restaurant API
=================

## Description
---
Find Restaurant API is an online tool that provides information of the nearest restaurant. The purpose of this API is to find a suitable restaurant for the user according to what cuisine they like/want to eat. This API specifically built for restaurants that resides inside Manitoba. 

## Endpoints
---
_Restaurant API uses REST API with `GET` request._ 

### GET/restaurant 
Locate a nearby restaurant by entering the postal code, cuisine and whether or not the restaurant delivers or not

GET: `https://find-restaurant-nearby/api/restaurant`

## Parameters
---
#### 1) postal-code(string)
Find nearby restaurant by entering your postal code
```
https://find-restaurant-nearby/api/restaurant?postal-code=R3t
```

#### 2) cuisine(string)
Find the restaurant with specific type of cuisine
```
https://find-restaurant-nearby/api/restaurant?cuisine=mexican
```

#### 3) deliver(boolean)

Find if the restaurant delivers food or not

```
https://find-restaurant-nearby/api/restaurant?deliver=true
```


## Description of Resources
---

## Sample Request and Response
---

## Group 17
 - Josh Sigurdson, 7858405
 - Vedant Pulahru, 7876784
 - Taylor Roy, 7812747
 - Mansimar Bhasin, 7875461
