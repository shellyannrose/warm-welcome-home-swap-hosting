
# The Gracious Host Service

World travelers now have the option to live like locals. Home exchange is one way to do this, for a fraction of the housing cost. Unlike hotels or rentals, travelers swap homes with people who live in a place they want to visit. For example, a woman from Ireland longs to explore the Yukon. She trades homes with a Canadian who loves Yeats.

## The problem: a host’s harried life  

To ensure house exchanges go smoothly, the host must take care to track the upcoming guest stays. This includes tracking:

* Who is coming; this includes the names and total number of guests
* When a guest arrives and leaves
* What tasks the host must complete before a guest arrives

Using spreadsheets or written notes to track this information creates more problems than they solve.

## The solution: a service for hosts to manage their guest stays

For a hassle-free solution, hosts can use the Gracious Host service. It is a cloud-based solution that has an API interface that is easy to use. It:

* Simplifies the tracking of dates, times, tasks, and people
* Ensures that hosts are well-prepared for their guests
* Stores all hosting information in one place

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

Now that you know a bit about this service, try [adding a new host](tutorials/tutorial-add-new-host.md) to the service. You will see how easy it is for hosts to give their guests a warm welcome!

## Tutorials

Learn how to do common tasks within the service.

### [Add a new host to the service](tutorials/tutorial-add-new-host.md)

## API reference docs

Detailed descriptions of the service's resources.

The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When running a local test, the `{base_url}` is
generally `http://localhost:3000`.

* [hosts resource](api/users.md)
* [guests resource](api/house_exchanges.md)
* [prep-checks resource](api/prep_checks.md)
