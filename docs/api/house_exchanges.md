---
layout: page
---
# `guests` resource

Base endpoint

```shell
{server_url}/guests
```

Contains information about guests and the details of their stay. Hosts add this information for a confirmed home exchange.

**Note** All properties are required, unless identified as optional.

## Resource properties

Sample `guests` resource

```js

{
    "host_id": 1,
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
| `host_id` | Number | Refers to the host id in the hosts resource |
| `arrival-date` | String | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the guest arrives. Update not supported |
| `departure-date` | String | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the guest leaves. Update not supported |
| `guest-names` | String |The names of all the guests |
| `last-name-primary` | String |The last name of the point of contact guest. Update not supported |
| `number-of-guests` | Number |The total number of guests expected |
| `type-of-exchange` | String |Indicates if swap is reciprocal or for guest points.Optional and update not supported |
| `id` | Number | Service-generated unique ID for the guest |

## Operations

The `guests` resource supports the operations below.

## CREATE (POST)

* [Add details for a new guest](../api/house_exchanges_CRUDref/create-add-house-guest.md)

## READ (GET)

* [Get all house guests](../api/house_exchanges_CRUDref/get-all-house-guests.md)
* [Get all guest names by id](../api/house_exchanges_CRUDref/get-all-guest-names-by-id.md)
* [Get all arrival dates](../api/house_exchanges_CRUDref/get-all-arrival-dates.md)
* [Get all reciprocal house swaps](../api/house_exchanges_CRUDref/get-all-reciprocal-house-swaps.md)

## UPDATE (PATCH/PUT)

* [Update (PATCH) number of guests by id](../api/house_exchanges_CRUDref/update-patch-number-of-guests-by-id.md)
* [Update (PUT) guest names by id](../api/house_exchanges_CRUDref/update-put-guest-names-by-id.md)

## DELETE (DELETE)

* [Remove a guest from a host's account by id](../api/house_exchanges_CRUDref/delete-house-guest-by-id.md)
