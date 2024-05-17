# Microservices Project with gRPC, Kafka, and GraphQL API Gateway

This project demonstrates a microservices architecture using Node.js, gRPC, Kafka, and Apollo Server for GraphQL.
It includes two microservices: `userMicroservice` and `productMicroservice`, which handle user and product data respectively.
An API Gateway facilitates interaction with these microservices via GraphQL and REST APIs.

## Project Structure


├── apiGateway.js   # API Gateway for handling GraphQL and REST API requests 

├── userMicroservice.js   # Microservice for managing users

├── productMicroservice.js   # Microservice for managing products

├── resolvers.js   # GraphQL resolvers

├── schema.js   # GraphQL schema definitions

├── user.proto   # gRPC proto file for users

├── product.proto    # gRPC proto file for products

├── .env   # Environment variables

└── README.md   # Project documentation


## Prerequisites

- Node.js
- Kafka
- Docker (optional, for running Kafka)
- gRPC
- Apollo Server
- Postman (for API testing)

2. Install Depenposdencies

npm install


Start the Microservices and API Gateway

node userMicroservice.js

node productMicroservice.js

node apiGateway.js

## Usage:

GraphQL API
Endpoint
http://localhost:3000/graphql

## Queries and Mutations:

Create a User 

Get All Users

Get User by ID

Update User

Delete User

Create a Product
Get All Products

Get Product by ID

Update Product

Delete Product


## Kafka Integration:

Kafka is used to publish and consume events for user and product operations. 
Events are published to the topics users-topic and products-topic. 
The API Gateway consumes these events and logs them to the console.

## Topics:

users-topic: For user-related events

products-topic: For product-related events

Sample Kafka Messages

When events are published, you should see logs similar to the following in your API Gateway console:

Received event: UserCreated { type: 'UserCreated', user: { id: user_id, username: 'user_name'}
