# Get started

 In this tutorial, you will see how easy it is to add a new host. To be successful, be sure to set up your development system first; see [Before you start a tutorial](before-you-start-tutorials.md).

## Add a new host to the service

Expect this tutorial to take about 15 minutes to complete.

### Run the local service

First, confirm that your local service is running in a command window. Use the following:

     ```shell

    cd <your GitHub repo workspace>
    dir
    # (see the Gracious Host directory in the list)
    cd HomeExchangeHaven\warm-welcome-home-swap-hosting
    cd api
    start-server.bat
    ```

### Start the Postman app

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request and enter the values below.
    * **METHOD**: POST
    * **URL**: `{server_url}/hosts`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        The table below lists the required properties for each host.

    | Property name | Type | Description |
    | ------------- | ----------- | ----------- |
    | `last_name` | String | Host’s last name |
    | `first_name` | String | Host’s first name|
    | `email` | String |Host’s email address |

1. In the Request body, enter the JSON script for the properties as shown below.

   ```js

    {
      "last_name": "Rochester",
      "first_name": "Edward",
      "email": "ed.rochester@example.com"
    }

   ```

1. In the Postman app, make the request by choosing **Send**. The Response body should look like the output below. Note that the content should be the same as you entered in the Request body. Also, the response should now include the new host's unique `id`.

```js
[
    {
    "last_name": "Rochester",
    "first_name": "Edward",
    "email": "ed.rochester@example.com",
    "id": 5
    } 
]
   ```

## Next steps

After doing this tutorial in Postman, you might like to repeat it in your favorite programming language. To do this, adapt the values from the tutorial to the properties and arguments that the language uses to make REST API calls.

## Related topics

* [Add a new guest for a host](tutorial-add-new-guest.md)
* [Add a task to prepare for a guest](tutorial-add-new-task.md)
