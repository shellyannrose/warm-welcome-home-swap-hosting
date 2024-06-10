
# The Gracious Host Service

Give your guests a welcome to write home about!

You are a world traveler who wants to live like a local when you visit new places. Home swapping is one way to do this, for a fraction of the housing cost. Your next destination? The Yukon. So, you have traded your home in Ireland with a Canadian who loves the poet Yeats.

Now what?

## The problem: a host’s harried life  

As a host, it is your job to prepare for your guest and ensure that the home swap goes smoothly. This includes tracking:

* Who is coming
* When your guest arrives and leaves
* What tasks you must complete before the guest arrives

Using spreadsheets or written notes to track this information creates more problems than they solve.

## The solution: a service for hosts to manage their guest stays

For a hassle-free solution, use the Gracious Host service. It is a cloud-based solution that has an API interface that is easy to use. It:

* Simplifies the tracking of dates, times, tasks, and people
* Ensures that hosts are well-prepared for their guests
* Stores all hosting information in one place

The Gracious Host makes it easy for hosts to give their guests a warm welcome.

## Resources and basic workflow

There are three resources:

* [Hosts](api/users.md) – This contains basic information about the host subscriber, like name and email address.
* [Guests](api/house_exchanges.md) – Once the host has a confirmed home swap, the host adds details about the guest. This resource stores guest details, like arrival date, number of guests, guest points usage, and so on.
* [Prep-checks](api/prep_checks.md) – The host then creates tasks for making the home ready. This includes cleaning rooms or buying utensils and food. This resource stores these tasks and alerts the host about a task’s due date.

## App integrations

Possible app integrations include:

* Hotel bookings
* Vacation (travel) bookings
* Rental property management

Now that you know a bit about this service, [get started](tutorials/tutorial-get-started.md) by learning how to add a new host to the service.

## Tutorials

Learn how to do common tasks within the service.

### [Add a new host to the service](tutorials/tutorial-add-new-host.md)

### [Add a new guest for a host](tutorials/tutorial-add-new-guest.md)

### [Add a task for a host to prepare for a guest](tutorials/tutorial-add-new-task.md)

## API reference docs

Detailed descriptions of the service's resources.

The API reference docs refer to a `{server_url}` when they
refer to the URL of a resource. This is synonymous with `{base_url}`. Its value depends
on how you implement the service.

When running a local test, the `{base_url}` is
generally `http://localhost:3000`.

* [hosts resource](api/users.md)
* [guests resource](api/house_exchanges.md)
* [prep-checks resource](api/prep_checks.md)

## Contact us

We are here to help. Send us an email at help@gracioushost.com.
