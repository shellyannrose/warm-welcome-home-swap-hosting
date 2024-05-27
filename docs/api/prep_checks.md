---
layout: page
---
# `prep-checks` resource

Base endpoint

```shell
{server_url}/prep-checks
```

Contains information about the tasks the host must completed befora a guest arrives.

**Note** All properties are required, unless identfied as optional.

## Resource properties

Sample `prep-checks` resource

```js

{
    "user_id": 1,
    "exchange_id": 1,
    "title": "Bed linen change",
    "room/area": "Bedrooms",
    "due date": "2024-08-10",
    "warning": "-12",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | Number | Refers to the host id in the users resource|
| `arrival-date` | String; change not supported |The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the guest arrives |
| `departure-date` | String; ; change not supported | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the guest leaves|
| `guest-names` | String |The names of all the guests |
| `last-name-primary` | String;; change not supported |The last name of the point of contact guest |
| `number-of-guests` | Number |The total number of guests expected |
| `type-of-exchange` | String; optional and change not supported |Indicates if swap is reciprocal or for guest points |
| `id` | Number | Service-generated unique ID for the house-exchange |

## Operations

The `prep-checks` resource supports the operations below.

## CREATE (POST)

* [Add details for a new house exchange guest](tbd)

## READ (GET)

* [Get all house-exchanges](tbd)
* [Get house-exchanges by id](tbd)
* [Get all guest-names by house-exchanges id](tbd)
* [Get all arrival-dates](tbd)
* [Get all departure-dates](tbd)
* [Get last-name-primary by house-exchanges id](tbd)
* [Get guest by departure-date](tbd)
* [Get guest by arrival-date](tbd)
* [Get number-of-guests by house-exchanges id](tbd)
* [Get type-of-exchange by house-exchanges id](tbd)

## UPDATE (PUT/PATCH)

* [Update guest-names house-exchanges id](tbd)
* [Update number-of-guests house-exchanges id](tbd)

## DELETE (DELETE)

* [Remove house exchange guest from service by house-exchanges id](tbd)
