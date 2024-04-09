# Share Your Thoughts

Share Your Thoughts is a web API where users can make friends and share their thoughts. Friends can leave reactions to other user's thoughts. All of these can be updated or deleted as well. Now, go out there and Share Your Thoughts!

 ## Table of Contents:  

[Description](#Description)  
[Installation](#Installation)  
[Tests](#Tests)  
[License](#License)     
[Author](#Author)

## Description:
This is a set of API for a social network that uses a MongoDB database so that the website can handle large amounts of unstructured data, Express.js for routing, Mongoose ODM, and the moment package to format time stamps.

## Installation:

1. Clone the repo to a local repository
2. You must have mongoDB installed
3. Run the following at the command line
```
    - npm init -y
    - npm install express
    - npm install mongoose
    - npm install moment
```
4. Start the server
```
    $ npm start
```

## Tests:  

Testing restful API calls using Insomnia  

---
**`/api/users`**
* `GET` all users
* `POST` a new user:
    ```json
    // example data
    {
        "username": "johnchewning",
        "email": "johnchewning@gmail.com"
    }
    ```
---
**`/api/users/:userid`**
* `GET` a single user by its `_id` 
* `PUT` to update a user by its `_id`
* `DELETE` to remove user by its `_id`
---
**`/api/users/:userId/friends/:friendId`**
* `POST` to add a new friend to a user's friend list
* `DELETE` to remove a friend from a user's friend list
---
**`/api/thoughts`** 
* `GET` to get all thoughts
* `POST` to create a new thought
    ```json
    // example data
    {
    "thoughtText": "Here's a thought!",
    "username": "johnchewning",
    "userId": "66149acb88cb63996eb4d08f"
    }
    ```
---
**`/api/thoughts/:thoughtId`**
* `GET` to get a single thought by its `_id`
* `PUT` to update a thought by its `_id`
* `DELETE` to remove a thought by its `_id`
---

**`/api/thoughts/:thoughtId/reactions`**

* `POST` to create a reaction 
    ```json
    // example data
    {
    "reactionBody":"Me too!!",
    "username":"newUser"
    }
    ```
---
**`/api/thoughts/:thoughtId/reactions/:reactionId`**
* `DELETE` remove a reaction by the `reactionId` 

## License: 
 This project is under the ISC license.  

## Author:

github: https://github.com/JohnChewning
