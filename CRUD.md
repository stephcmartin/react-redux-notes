# Express

It is built on top of node.js http module, and adds support for routing, middleware, view system etc.
It is very simple and minimal, unlike other frameworks that try do way to much, thereby reducing the flexibility for developers to have their own design choices.

# Mongoose

Mongoose is an ODM (Object Document Mapping) tool for Node.js and MongoDB. It helps you convert the objects in your code to documents in the database and vice versa.

# Body Parser

body-parser is a module that parses the request (of various content types)
and creates a req.body object that we can access in our routes.

A middleware is a function that has access to the request and response objects. It can execute any code, transform the request object, or return a response.


## Step 1: Setting up the web servers

First, We import express and body-parser modules. Express, as you know, is a web framework that we’ll be using for building the REST APIs, and body-parser is a module that parses the request (of various content types) and creates a req.body object that we can access in our routes.

Then, We create an express app, and add two body-parser middlewares using express’s app.use() method.

A middleware is a function that has access to the request and response objects. It can execute any code, transform the request object, or return a response.

Then, We define a simple GET route which returns a welcome message to the clients.

Finally, We listen on port 3000 for incoming connections.

## Step 2: Configuring and Connecting to the database

## Step 3: Defining the Model

The Note model is very simple. It contains a title and a content field. I have also added a timestamps option to the schema.

Mongoose uses this option to automatically add two new fields - createdAt and updatedAt to the schema.

## Step 4: Defining Routes using Express

## Step 5: Writing the Controller functions

The controller will contain methods for handling all the CRUD operations.

## Step 6: Test APIs!
