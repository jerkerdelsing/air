# Use Cases

This folder gathers use cases, each of which is meant to describe a particular way in which AIR can facilitate a concrete scenario.
Each use case is described as (1) a name, (2) an overview and (3) a sequence of steps, as exemplified below.
Optionally, use cases can be accompanied by a [SysML Use Case Diagram](https://sysml.org/sysml-faq/what-is-use-case-diagram.html).
Use cases should only be as specific as required to highlight how they relate to AIR.

Each use case file has a name starting with three digits and a dash, as well as have the extension `.md`, which makes it a markdown file.
An example file name could be `001-listing-service-registry-records.md`.

## Example

### Listing service registry records

An _Operator_ uses a _Graphical User Interface_ (GUI) to list the service records of a _Service Registry_ in a particular local cloud.

| Step | Actor    | Action                               | Uses                      | Results                             | State |
|-----:|:---------|:-------------------------------------|:--------------------------|:------------------------------------|:------|
|    1 | Operator | Clicks on service registry system.   | GUI                       | Opens services panel.               | Empty services panel open.
|    2 | GUI      | Fetches services of clicked system.  | Service Discovery service | Lists retrieved services.           | Populated services panel open.
|    3 | Operator | Clicks on service discovery service. | GUI                       | Opens service discovery panel.      | Empty service discovery panel open, no layout.
|    4 | GUI      | Fetches AIR for clicked service.     | Repository service        | AIR retrieved.                      | Empty service discovery panel open, no layout.
|    5 | GUI      | Processes AIR.                       | AIR                       | Service discovery panel has layout. | Empty service discovery panel open, has layout.
|    6 | GUI      | Sends queries stated in AIR.         | Service Discovery service | Lists retrieved service records.    | Populated service discovery panel open.

The meanings of the table columns are as follows:

- _Step_ enumerates each action of the use case.
- _Actor_ declares who is performing the use case action.
- _Action_ describes what the actor does.
- _Uses_ lists all entities being used by the actor.
- _Results_ outlines the immediate effects produced by the action.
- _State_ describes the situation produced by each action.
