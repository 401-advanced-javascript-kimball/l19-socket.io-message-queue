# l19-socket.io-message-queue
Message Queue server that monitors database events, and then modifying our API server to fire events into that Queue on all CRUD operations in our models. This uses a 3rd party library (@nmq/q) to do this work.
# l19-socket.io-message-queue

https://github.com/401-advanced-javascript-kimball/l19-socket.io-message-queue/pull/1
https://travis-ci.com/401-advanced-javascript-kimball/l19-socket.io-message-queue

# LAB - 

## Project Name

### Author: Student/Group Name

### Links and Resources
* [submission PR](http://xyz.com)
* [travis](http://xyz.com)
* [back-end](http://xyz.com) (when applicable)
* [front-end](http://xyz.com) (when applicable)

#### Documentation
* [api docs](http://xyz.com) (API servers)
* [jsdoc](http://xyz.com) (Server assignments)
* [styleguide](http://xyz.com) (React assignments)

### Modules
#### `modulename.js`
##### Exported Values and Methods

###### `foo(thing) -> string`
Usage Notes or examples

###### `bar(array) -> array`
Usage Notes or examples

### Setup
#### `.env` requirements
* `PORT` - Port Number
* `MONGODB_URI` - URL to the running mongo instance/db

#### Running the app
* `npm start`
* Endpoint: `/foo/bar/`
  * Returns a JSON object with abc in it.
* Endpoint: `/bing/zing/`
  * Returns a JSON object with xyz in it.
  
#### Tests
* How do you run tests?
* What assertions were made?
* What assertions need to be / should be made?

#### UML
Link to an image of the UML for your application and response to events

----------

# LAB: Socket.io - Message Queue Server

For this lab assignment, we will be writing a Message Queue server that monitors database events, and then modifying our API server to fire events into that Queue on all CRUD operations in our models. This will use a 3rd party library (@nmq/q) to do this work.

## Before you begin
Refer to *Getting Started*  in the [lab submission instructions](../../../reference/submission-instructions/labs/README.md) for complete setup, configuration, deployment, and submission instructions.


## Getting Started

Get your api server up and running!  You're going to be modifying it in this lab.

You will likely be creating 3 new git repositories to house the servers for this lab assignment

### Assignment - Message Queue Server and Logger

* Create a message queue server
* Initiate a queue called "files" that monitors "save" and "error" events
* Initiate a queue called "database" that monitors "create", "read", "update", "delete" and "error" events
* Create a logger application 
* Connects to the "file" and "database" queues
* Performs a custom `console.log()` on the events named above

### Assignment 1 - File Writer (warm-up)
This will be a repeat of the previous labs, this time using your new message queue server.

* In the starter code, you'll once again find an `app.js` that reads and modifies a file.
* On a successful write, publish a "save" event to the "file" queue
* On error, publish an "error" event to the "file" queue
* Modularize the file reader

### Assignment 2 - API Server
Alter your API server to publish events on all CRUD Operations

* Import the Queue client library
* Perform a publish into the database queue, after "create", "update", "delete" and on any errors in your models.

**Questions**

* Where is the best place to do this? In the `mongo.js`? In each mongoose model?
* How will you trap and publish error events?
* Where will you identify the Queue server?

### Testing
* What will your approach be to asserting the API server published the right event?
* How will you write assertions on the logger?

### Deployment
* Deployment is not required


### Assignment Submission Instructions
Refer to the the [lab submission instructions](../../../reference/submission-instructions/labs/README.md) for the complete lab submission process and expectations

----------

