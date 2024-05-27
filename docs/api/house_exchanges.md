---
layout: page
---
# `house-exchanges` resource

Base endpoint

```shell
{server_url}/house-exchanges
```

Contains information about guests and the details of their stay. Hosts add this information for a confirmed home swap.

**Note** All properties are required, unless identfied as optional.

## Resource properties

Sample `house-exchanges` resource

```js

{
    "user_id": 1,
    "arrival-date": "2024-08-12T17:00",
    "departure-date": "2024-08-20T12:00", 
    "guest-names": "Bill and Katie",
    "last-name-primary": "Collison",
    "number-of-guests ": "5",
    "type-of-exchange ": "Guest Points",  
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | Number | Refers to the host id in the users resource|
| `arrival-date` | String; update not supported |The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the guest arrives |
| `departure-date` | String; ; update not supported | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the guest leaves|
| `guest-names` | String |The names of all the guests |
| `last-name-primary` | String; update not supported |The last name of the point of contact guest |
| `number-of-guests` | Number |The total number of guests expected |
| `type-of-exchange` | String; optional and update not supported |Indicates if swap is reciprocal or for guest points |
| `id` | Number | Service-generated unique ID for the house-exchange |

## Operations

The `house-exchanges` resource supports the operations below.

## CREATE (POST)

* [Add details for a new house exchange guest](tbd)

## READ (GET)

* [Get all house-exchanges](tbd)
* [Get house-exchanges by id](tbd)
* [Get all guest-names by id](tbd)
* [Get all arrival-dates](tbd)
* [Get arrival-date by id](tbd)
* [Get all departure-dates](tbd)
* [Get departure-date by id](tbd)
* [Get last-name-primary by id](tbd)
* [Get guest by departure-date](tbd)
* [Get guest by arrival-date](tbd)
* [Get number-of-guests by id](tbd)
* [Get type-of-exchange by id](tbd)
* [Get all guest points type-of-exchange](tbd)
* [Get all reciprocal type-of-exchange](tbd)

## UPDATE (PUT/PATCH)

* [Update guest-names by id](tbd)
* [Update number-of-guests by id](tbd)

## DELETE (DELETE)

* [Remove house exchange guest from the service by id](tbd)
