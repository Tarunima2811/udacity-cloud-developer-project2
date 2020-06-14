# Udagram Image Filtering Microservice

Udagram is a simple cloud application developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.

The project is split into three parts:
1. [The Simple Frontend](https://github.com/udacity/cloud-developer/tree/master/course-02/exercises/udacity-c2-frontend)
A basic Ionic client web application which consumes the RestAPI Backend. [Covered in the course]
2. [The RestAPI Backend](https://github.com/udacity/cloud-developer/tree/master/course-02/exercises/udacity-c2-restapi), a Node-Express server which can be deployed to a cloud service. [Covered in the course]
3. [The Image Filtering Microservice](https://github.com/udacity/cloud-developer/tree/master/course-02/project/image-filter-starter-code), the final project for the course. It is a Node-Express application which runs a simple script to process images. [This assignment]

## Tasks done as part of this project

### Setup Node Environment

Created a new node server. Open a new terminal within the project directory and run:

1. Initialize a new project: `npm i`
2. run the development server with `npm run dev`

### Created a new endpoint in the server.ts file

Completed an endpoint in `./src/server.ts` which uses query parameter to download an image from a public URL, filter the image, and return the result.

Used the helper functions to handle some of these concepts and those are imported at the top of the `./src/server.ts`  file.

```typescript
import {filterImageFromURL, deleteLocalFiles} from './util/util';
```

### Deploying the system

Follow the process described in the course to `eb init` a new application and `eb create` a new environment to deploy your image-filter service! Don't forget you can use `eb deploy` to push changes.


<b>Link to access:</b> 

http://udacity-cloud-developer-project2-dev.ap-south-1.elasticbeanstalk.com/filteredimage?image_url=https://www.cleverfiles.com/howto/wp-content/uploads/2018/03/minion.jpg

API Response of deployed app:

![Alt text](/deployment_screenshots/deployment-response.PNG "AWS deployed response")

