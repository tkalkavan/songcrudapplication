
# ****Spring Boot + Angular 9 CRUD + MongoDB + Tutorial****

 CRUD application that we are using Spring Boot to handle the backend part and Angular to handle the frontend part.
 
 ![Alt text](https://i.ibb.co/Cwm62f9/Copy-of-Spring-Boot-Angular-9-CRUD-Mongo-DB-Docker-Tutorial-1.png "Architecture of application")

##**What are going to implement?**
* Create a song
* Update a song
* List of songs
* Delete song
* View song details
* Plus Rating for Song :)

##**Working of Application**
* Once we deployed our application on the server,a view pop-up to add and view students at the web browser. 
* Once clicking add song link, the page redirects to create song via router we can add a song by filling the required details.
* At the main page, details of the existing song fetched from MongoDB and song also contains update and delete link.
* Note that I'm populating image from file system, just for simplicty :)


![Alt text](https://i.ibb.co/6PptTG2/Spring-Boot-Angular-9-CRUD-Mongo-DB-Docker-Tutorial-2-Song.png "Architecture of application")


**Backend endpoints:**

http://localhost:8080/songs/createSong \
http://localhost:8080/songs/updateSong/{id} \
http://localhost:8080/songs/deleteSong/{id} \
http://localhost:8080/songs/getSong/{id} \
http://localhost:8080/songs/getAllSongs

Sample JSON data:
```json

  {
    "id": "5fe491cee71c1c45b8b517d3",
    "title": "Highway to Hell",
    "artist": "AC/DC",
    "image": "./assets/images/acdc.png",
    "album": "Highway to Hell",
    "genre": "Rock, Heavy metal, Hard rock, Blues, Rock and roll, Blues rock, Boogie rock",
    "thumbRating": 5,
    "releaseDate": "2020-04-24"
  }

```

![Alt text](https://i.ibb.co/t2KZf17/Spring-Boot-Angular-9-CRUD-Mongo-DB-Docker-Tutorial-2-1.png "Angular side")

In order to setup MongoDB configuration, we relied on the defaults. Spring Data MongoDB configuration  we are editing the application.properties file present inside the src/main/resources folder. 
If its not created, you can create it manually and setup like this:

`spring.data.mongodb.uri=mongodb://localhost:27017/songdb`

**Front end side**

At the front end side, we have components for CRUD operations.
To start front-end side navigate the folder and start the application


`cd ui-angular `

Start to server, type following to terminal :\

`npm serve ` 


**Database**

For this project, I preffered to use MongoDB, here example of data in your db side.
```json

{
    "_id": {
        "$oid": "5fe49122e71c1c45b8b517d1"
    },
    "title": "My Baby",
    "artist": "Janis Joplin",
    "image": "./assets/images/jj.jpg",
    "album": "Pearl (Legacy Edition)",
    "genre": "Rock",
    "thumbRating": 5,
    "releaseDate": {
        "$date": "2020-12-24T13:01:22.640Z"
    },
    "_class": "com.spring.songapp.model.Song"
}
```

**Screenshot of project**

![Alt text](https://i.ibb.co/cgRgzzW/screenshot.png "Angular side")
