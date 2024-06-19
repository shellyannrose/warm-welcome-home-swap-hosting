# Tutorial: Add a new guest for a specific host

 In this tutorial, you will learn how to add a guest for a host. Be sure to [set up](before-you-start-tutorials.md) your system first.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

First, confirm that your local service is running in a command window. Use the following:

    ```shell
    
         cd <your-github-workspace>/warm-welcome-home-swap-hosting/api
        # Run the service and monitor its database file for updates
        json-server -w warm-welcome-home-swap-hosting-db-source.json
        
    ```

## Start the Postman app

1. Open the Postman app on your desktop.
1. [Find the host id](../api/users_CRUDref/get-all-hosts.md) using a GET request.
1. In the Postman app, create a new request and enter the values below.
    * **METHOD**: POST
    * **URL**: `{server_url}/guests`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        The table below lists the required properties for each guest.

    | Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `host_id` | Number | Refers to the host id in the hosts resource |
| `arrival-date` | String | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the guest arrives. Update not supported |
| `departure-date` | String | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the guest leaves. Update not supported |
| `guest-names` | String |The names of all the guests |
| `last-name-primary` | String |The last name of the point of contact guest. Update not supported |
| `number-of-guests` | Number |The total number of guests expected |
| `type-of-exchange` | String |Indicates if swap is reciprocal or for guest points. Optional and update not supported |

1. In the Request body, enter the JSON script for the properties as shown below.

    ```js

   {
     "host_id": 5,
     "arrival-date": "2024-11-26T14:00",
     "departure-date": "2024-12-03T12:00", 
     "guest-names": "Jane Eyre",
     "last-name-primary": "Elliot",
     "number-of-guests": 1,
     "type-of-exchange": "Reciprocal"    
   }

    ```

1. In the Postman app, make the request by choosing **Send**. The Response body should look like the output below. Note that the content should be the same as you entered in the **Request body**. Also, the response should now include the new guest's unique `id`.

```js
[
   {
     "host_id": 5,
     "arrival-date": "2024-11-26T14:00",
     "departure-date": "2024-12-03T12:00", 
     "guest-names": "Jane Eyre",
     "last-name-primary": "Elliot",
     "number-of-guests": 1,
     "type-of-exchange": "Reciprocal",
     "id": 1
    
   }
]
```

## Next steps

You just added your first guest. You're doing great! Now, [add a task](tutorial-add-new-task.md) for that guest.

After doing this tutorial in Postman, you might like to repeat it in your favorite programming language. To do this, adapt the values from the tutorial to the properties and arguments that the language uses to make REST API calls.

## Related topics

[Guests resource](../api/house_exchanges.md)
