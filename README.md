Find Restaurant API
=================

## Description

Find Restaurant API is an online tool that provides information of the nearest restaurant within the province of Manitoba. The purpose of this API is to find a suitable restaurant for the user according to desired cuisine, distance and delvivery options.

## Endpoint

_Restaurant API uses REST API with `GET` request._ 

### `GET` /restaurant 
Locate a nearby restaurant by entering the postal code, cuisine and whether or not the restaurant delivers or not

`GET`: `https://find-restaurant-nearby/api/restaurant`

### Parameters

#### 1) postal-code (string)

First three digits of the requested postal code.
<br>(Required)

```
https://find-restaurant-nearby/api/restaurant?postal-code=R3t
```

#### 2) cuisine (string)

The type of cuisine requested, in text. 
<br>(Optional)

```
https://find-restaurant-nearby/api/restaurant?cuisine=mexican
```

#### 3) delivery (integer)

0 or 1 (0 default). 0 for delivery not required. 1 for delivery required.
<br>(Optional)

```
https://find-restaurant-nearby/api/restaurant?deliver=true
```

## Resource

    {
        "results": [
            {
                "restaurant-name",
                "address",
                "cuisine",
                "delivery",
            },
            {
                "restaurant-name",
                "address",
                "cuisine",
                "delivery",
            },
            ...
        ]
        "status": "OK"
    }

## Sample Request and Response

### Request

### Response


## Group 17
 - Josh Sigurdson, 7858405
 - Vedant Pulahru, 7876784
 - Taylor Roy, 7812747
 - Mansimar Bhasin, 7875461
