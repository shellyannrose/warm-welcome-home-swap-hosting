
# Before you start a tutorial

You must follow the steps below before you try the tutorials for the Gracious Host service. These steps should take about 20 minutes to complete.

## Tools to complete the tutorials

The instructions below are for a Windows system (PC).

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

## Test your development system

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

## Related topics

* [Get started](tutorial-get-started.md) tutorial
