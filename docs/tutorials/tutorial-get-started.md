# Get started

 In this tutorial, you will see how easy it is to add a new host.

## Before you  start a tutorial

You must follow the steps below before you try the tutorials for the Gracious Host service. These steps should take about 20 minutes to complete.

### Tools to complete the tutorials in this section

The instructions below are for a Windows system (PC). For a MacOS system, see the [MacOS installation guide](macos-installation).

* A [GitHub account](https://github.com)
* A PC that is running a current or
long-term support (LTS) version of the OS
* A Windows command window (for the command line)
* [GitHub Desktop](https://desktop.github.com) (optional)
* A fork of the [Gracious Host service](https://github.com/shellyannrose/warm-welcome-home-swap-hosting)
* A current or LTS version of [node.js](https://nodejs.org/en/). Node Package Manager (npm) installs when you install node.js.
* A current version of [json-server](https://www.npmjs.com/package/json-server). To install it, open a command window and run ```npm install -g json-server```.
* A current copy of the service's database file (`warm-welcome-home-swap-hosting-db-source`). You can get this by syncing your fork.
    * **TIP**: If you use a fork of the repository (repo), create a working branch for the tutorial. For each tutorial, create a new branch. Doing this stops a mistake in one branch from affecting your work in another.
* A copy of the [Postman desktop app](https://www.postman.com/downloads/). You will run the Gracious Host service on your PC using an `http://localhost` hostname. Because of this, the web-version of Postman cannot perform the exercises.

### Test your development system

To test your system, follow the steps below.

1. Create and checkout a working branch of your fork of the Gracious Host repo.
1. Open a command window. The GitHub repo workspace is the directory that contains your fork of the Gracious Host repo.

    ```shell
    cd <your GitHub repo workspace>
    dir
    # (see the Gracious Host directory in the list)
    cd HomeExchangeHaven\warm-welcome-home-swap-hosting
    cd api
    start-server.bat
    ```

    If you installed the tools correctly, the service should start. A list of the resources appears and the URL of the service shows as `http://localhost:3000`.

1. Open a new command window.  Make a test call to the service using the cURL command line that's included in Windows and other platforms.

    ```shell
    curl http://localhost:3000/hosts
    ```

1. If the service is running correctly, you should get a list of hosts from the service. See the example below.

    ```js
    [

     {
      "last_name": "Smith",
      "first_name": "Wallace",
      "email": "w.smith@example.com",
      "id": "1"
    },
    {
      "last_name": "Gibson",
      "first_name": "Harley",
      "email": "h.gibson@example.com",
      "id": "2"
    },

    ]
    ```

If you do not get a list of hosts or receive an error, stop. Investigate and fix the error before you go on. Some common reasons for errors include:

1. You mistyped a command
2. You are not in the correct directory
3. A required software component did not install correctly
4. A required software component is not up to date

If you see the list of hosts from the service, you are ready to do the tutorials.

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
* [Add a task for a host to prepare for a guest](tutorial-add-new-task.md)
