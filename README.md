Find Restaurant API
=================

## Description

Find Restaurant API is an online tool that provides information of the nearest restaurant for users within the province of Manitoba. The purpose of this API is to find a suitable restaurant for the user according to desired cuisine, distance and delivery options. 

## Endpoint

_Restaurant API uses REST API with `GET` request._ 

### `GET` /restaurant 
Locate a nearby restaurant by entering the postal code, cuisine and whether or not the restaurant delivers or not

`GET`: `https://find-restaurant-nearby/api/restaurant`

### Parameters

#### 1) Postal-code (String)

First three digits of the requested postal code. \
_(Required)_

#### 2) Cuisine (String)

The type of cuisine requested, in text. \
_(Optional)_

#### 3) Delivery (Integer)

0 or 1 (0 default). 0 for delivery optional. 1 for delivery required. \
_(Optional)_

## Resource

    {
        "results": [
            {
                "restaurant-name"
                "street-address"
                "city"
                "postal-code"
                "cuisine"
                "delivery"
            },
            {
                "restaurant-name"
                "street-address"
                "city"
                "postal-code"
                "cuisine"
                "delivery"
            },
            ...
        ]
        "status": "OK"
    }

## Sample Request and Response


### Request 1

`https://find-restaurant-nearby/api/restaurant?postal-code=r3c&cuisine=mexican&delivery=0`

### Response

    {
        "results": {
            {
                "restaurant-name":"La Roca",
                "street-address":"155 Smith St"
                "city":"Winnipeg"
                "postal-code":"R3C 1J7",
                "cuisine":"Mexican",
                "delivery":"no",
            },
            {
                "restaurant-name":"Habanero Sombrero",
                "address":"212-1 Forks Market Rd",
                "city":"Winnipeg"
                "postal-code":"R3C 4L9",
                "cuisine":"Mexican",
                "delivery":"yes",
            },
            ...
        }
        "status": "OK"
    }

### Request 2

`https://find-restaurant-nearby/api/restaurant?postal-code=r3c&cuisine=mexican&delivery=true`

### Response

    {
        "results": {}
        "status": "INVALID_DELIVERY"
    }


## Status Code
* "OK": indicates no errors;
* "INVALID_REQUEST": indicates postal-code is missing or invalid;
* "INVALID_DELIVERY": indicates wrong format for delivery;
* "ERROR_404": indicates server side error. 

## Group 17
 - [Josh Sigurdson](https://github.com/joshsig),  7858405
 - [Vedant Pulahru](https://github.com/Vedant1206),  7876784
 - [Taylor Roy](https://github.com/TayRoy),      7812747
 - [Mansimar Bhasin](https://github.com/mansimars), 7875461
