# CHITCHAT ANDROID APPLICATION

This is an android chat application. It uses websocket connection for live chat.

## Technologies used

Frontend - React Native

Backend - `Spring boot`, `Spring Security`, `Microservice`

Backend MicroServices - 
1.  UserService - used for storing phone_number - user_id mapping <br />
		Database - `Cassandra`
  
2.  WebSocketService - chat server<br />
		Tech - `RabbitMQ`

3.  Service Registry - for registering the micro-services.<br />
		Tech - `Netflix Eureka server`

4.  gateway - for routing requests to different services.<br />
		Tech - `Spring cloud gateway`

## Steps to run locally



### Step 1. Clone the repositories



### Step 2. Install required softwares

`Node.js`
`Cassandra`
`OTP/Erlang 25.1.2`
`rabbitMQ Server 3.11.2`
`Docker`
`Java 11`

<details>
  <summary> Install and configure cassandra</summary>
  
1. install docker
2. install cassandra (docker)<br />
docker run --name cassandra2 -p 9042:9042 -d cassandra:latest
3. create tables
docker exec -it cassandra2 bash -c 'cqlsh'
4. Run the following commands

CREATE KEYSPACE chitchat WITH REPLICATION = { 'class' : 'NetworkTopologyStrategy', 'datacenter1' : 1 }; <br />
use chitchat;<br />
create table idtophone(id text primary key, phonenumber text);<br />
create table phonetoid(phonenumber text primary key, id text);

insert into idtophone (id, phonenumber) Values ('a5fffdea-5f64-11ed-9b6a-0242ac120002', '911234567890');<br />
insert into idtophone (id, phonenumber) Values ('63073d0e-5f65-11ed-9b6a-0242ac120002', '913334567890');<br />
insert into idtophone (id, phonenumber) Values ('7aa52c6e-5f65-11ed-9b6a-0242ac120002', '914444567890');<br />
insert into idtophone (id, phonenumber) Values ('84e3fa70-5f65-11ed-9b6a-0242ac120002', '915555567890');<br />
insert into idtophone (id, phonenumber) Values ('8d3f698e-5f65-11ed-9b6a-0242ac120002', '916666667890');<br />

insert into phonetoid (phonenumber, id) Values ('911234567890', 'a5fffdea-5f64-11ed-9b6a-0242ac120002');<br />
insert into phonetoid (phonenumber, id) Values ('913334567890', '63073d0e-5f65-11ed-9b6a-0242ac120002');<br />
insert into phonetoid (phonenumber, id) Values ('914444567890', '7aa52c6e-5f65-11ed-9b6a-0242ac120002');<br />
insert into phonetoid (phonenumber, id) Values ('915555567890', '84e3fa70-5f65-11ed-9b6a-0242ac120002');<br />
insert into phonetoid (phonenumber, id) Values ('916666667890', '8d3f698e-5f65-11ed-9b6a-0242ac120002');

</details>



### Step 2. Install required softwares

## Architecture
### High Level Design Diagram
![Chitchat_HLD](https://user-images.githubusercontent.com/56664469/207870169-23146e16-8add-4faa-918b-24d506c8d176.png)

### Functional Diagram

![Chitchat_Functional_Diagram](https://user-images.githubusercontent.com/56664469/207870382-fb966383-d7ad-4160-9df1-880d8607d1b1.png)


## Youtube link

https://youtu.be/KSSpvPWO5no
