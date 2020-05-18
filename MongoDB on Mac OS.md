# MongoDB on Mac OS 

### Install MongoDB on Mac OS


[install mongoDB on Mac](https://zellwk.com/blog/install-mongodb/)
### MongoDB version

```
> mongo --version
```
### Start the server mongoDB 

```
> mongod
```

Then, you open a new command line window without close the current one.

And type:


```
waltervives$ mongo
```
The output will be:

```
Enable MongoDB's free cloud-based monitoring service, which will then receive and display
metrics about your deployment (disk utilization, CPU, operation statistics, etc).

The monitoring data will be available on a MongoDB website with a unique URL accessible to you
and anyone you share the URL with. MongoDB may use this information to make product
improvements and to suggest MongoDB products and deployment options to you.

To enable free monitoring, run the following command: db.enableFreeMonitoring()
To permanently disable this reminder, run the following command: db.disableFreeMonitoring()
---

> 
```
### Show users
```
> db.getUsers()

```

### Create new users
```
> use admin
 
> db.createUser({user:'USERNAME', pwd:'PASSWORD', roles: ['userAdminAnyDatabase']}) 
```
close the terminal and open it again and type the next command:

```
waltervives$ mongo admin -u waltervives -p 
 Enter password:
```
Then, you will have access to mongoDB shell:

```
Enable MongoDB's free cloud-based monitoring service, which will then receive and display
metrics about your deployment (disk utilization, CPU, operation statistics, etc).

The monitoring data will be available on a MongoDB website with a unique URL accessible to you
and anyone you share the URL with. MongoDB may use this information to make product
improvements and to suggest MongoDB products and deployment options to you.

To enable free monitoring, run the following command: db.enableFreeMonitoring()
To permanently disable this reminder, run the following command: db.disableFreeMoqnitoring()


> 
```
### Exit mongoDB

```
> exit
```
or 

```
> quit()
```
### Remote connection

From the command line, type:

```
waltervives$ mongo "link" --username USERNAME
```
You only need to change **USERNAME**  
then, type the password and now you're connected. :).

### Show the databases
```
> show databases;
```

### Create or select a database

with the **use** command you can select a databse, if the database does not exit then, will be create a new one.

```
> use database1;
```
### Show the collections

First we need to select the database with **use** commnad to select your database and then type:

```
> show collections;
```
### Create a collection
First we select our database.

```
> use walter;
```
Create a collection:

```
> db.createCollection("yourcollectionname");
```
*Example:*

```
> db.collection("clients");
```

### Insert data into your collection

```
> db.collection.insertOne();
```

*Example:*

```
> db.clients.insertOne({"Nombre": "Walter",
  "Apellido": "Vives", "Edad": 20})
```

or **db.collection.insertMany()**:

```
> db.clients.insertMany([{"Nombre": "Walter",
  "Apellido": "Vives", "Edad": 20},
  {"Nombre": "Juan",
  "Apellido": "Vazquez", "Edad": 20},
  {"Nombre": "Carlos",
  "Apellido": "Santana", "Edad": 20}]);
```


