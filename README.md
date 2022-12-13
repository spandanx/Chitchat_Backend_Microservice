# CHITCHAT ANDROID APPLICATION

This is an android chat application. It uses websocket connection for live chat.

## Technologies used

Frontend - React Native

Backend - Spring boot, spring security, Microservice

Backend MicroServices - 
1.  UserService - used for authentication and storing phone_number - user_id mapping
		Database - Cassandra
  
2.  WebSocketService - chat server
		Tech - RabbitMQ

3.  Service Registry - for registering the micro-services.
		Tech - Netflix Eureka server

4.  gateway - for routing requests to different services.
		Tech - Spring cloud gateway

## Steps to run locally



### Step 1. Clone the repository



### Step 2. Install required softwares

`Node.js`
`Cassandra`
`RabbitMQ`
`Java 11`

### Step 2. Install required softwares

## Youtube link

https://youtu.be/KSSpvPWO5no
