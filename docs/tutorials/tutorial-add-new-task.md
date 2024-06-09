# Tutorial: Add a new task for your host to prepare for a guest

 This tutorial explains how to create a new task that a host will do to prepare for a guest.

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
1. In the Postman app, create a new request and enter the values below.
    * **METHOD**: POST
    * **URL**: `{server_url}/prep-checks`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        The table below lists the required properties for each task.

   | Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `host_id` | Number | Refers to the host id in the hosts resource |
| `guest_id` | Number |Refers to the guest id in the guests resource |
| `title` | String |The name of the task |
| `room-area` | String|The part of the home that requires the task |
| `due-date` | String | The date the host chooses to finish the task |
| `warning` | Number |The number of minutes relative to the due date to alert the host to finish the task. This is normally a negative number to alert the host before the due date |

1. In the Request body, enter the JSON script for the properties as shown below.

   ```js
     {
        "host_id": 5,
        "guest_id": 1,
        "title": "Hide insane wife",
        "room-area": "Secret room",
        "due-date": "2024-11-25",
        "warning": "-180"        
     }

   ```

1. In the Postman app, make the request by choosing **Send**. The Response body should look like the output below. Note that the content should be the same as you entered in the **Request body**. Also, the response should now include the new host's unique `id`.

   ```js
   [
     {
      "host_id": 5,
      "guest_id": 1,
      "title": "Hide insane wife",
      "room-area": "Secret room",
      "due-date": "2024-11-25",
      "warning": "-180",
      "id": 1        
     }
   ]
   ```

## Next steps

Good on ya! Looks like your host will be ready for this guest. After doing this tutorial in Postman, you might like to repeat it in your favorite programming language. To do this, adapt the values from the tutorial to the properties and arguments that the language uses to make REST API calls.
