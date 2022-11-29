Find Restaurant API
=================

## Description

Find Restaurant API is an online tool that provides information of the nearest restaurant within the province of Manitoba. The purpose of this API is to find a suitable restaurant for the user according to desired cuisine, distance and delivery options.

## Endpoint

_Restaurant API uses REST API with `GET` request._ 

### `GET` /restaurant 
Locate a nearby restaurant by entering the postal code, cuisine and whether or not the restaurant delivers or not

`GET`: `https://find-restaurant-nearby/api/restaurant`

### Parameters

#### 1) postal-code (string)

First three digits of the requested postal code. \
_(Required)_

#### 2) cuisine (string)

The type of cuisine requested, in text. \
_(Optional)_

#### 3) delivery (integer)

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


### Request

`https://find-restaurant-nearby/api/restaurant?postal-code=r3c&cuisine=mexican&delivery=0`

### Response

    {
        "results": [
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
        ]
        "status": "OK"
    }

## Status Code


## Group 17
 - Josh Sigurdson, 7858405
 - Vedant Pulahru, 7876784
 - Taylor Roy, 7812747
 - Mansimar Bhasin, 7875461
