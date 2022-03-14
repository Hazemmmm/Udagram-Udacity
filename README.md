# Udagram

This application is provided to you as an alternative starter project if you do not wish to host your own code done in the previous courses of this nanodegree. The udagram application is a fairly simple application that includes all the major components of a Full-Stack web application.

## Getting Started

1. Clone this repo locally into the location of your choice.
1. Move the content of the udagram folder at the root of the repository as this will become the main content of the project.
1. Open a terminal and navigate to the root of the repo
1. follow the instructions in the installation step

The project can run but is missing some information to connect to the database and storage service. These will be setup during the course of the project

### Steps for Running Project Locally:
1- Upload that code after clonning to your github repo.
2- Add .env file in root folder 
 -- udapgram-api 
   -- src
   -- .env
3- This .env file must contain the following keys:
   - POSTGRES_HOST= **********
   - PORT=********
   - POSTGRES_USERNAME=********
   - POSTGRES_PASSWORD=********
   - POSTGRES_DB=********
   - DB_PORT=********
   - RDS_DIALECT=********
   - AWS_REGION=********
   - URL=********
   - JWT_SECRET=********
   - EB_APP=********
   - EB_ENV=********
   - AWS_BUCKET=********

4- Run this script first `npm install` for both front & back end folders.
5- Run the server and the client side using `npm run start`
backend should route to `localhost:${your port}` and Frontend should route to `localhost:4200`

### In order to view your deployment on S3 [Front End Environment]

    S3 Bucket: `my-bucket-udagram`
    S3 URL: `http://my-bucket-udagram.s3-website-us-east-1.amazonaws.com/`

![Alt text](https://github.com/Hazemmmm/Udagram-Udacity/blob/main/Docs/S3/Screenshot%202022-03-11%20172507.jpg "Frontend Environment")

### In order to view your deployment on Elastic Beanstalk [Back End Environment]
    Application Name: `udagram`  
    Enviroment Name: `Udagram-env`
    URL: `http://udagram-env.eba-jxzps8vm.us-east-1.elasticbeanstalk.com`

![Alt text](https://github.com/Hazemmmm/Udagram-Udacity/blob/main/Docs/EB/Screenshot%202022-03-14%20010317.jpg "BackEnd Environment")

### In order to view your deployment on RDS Database [Datbase Environment]

    DB URL: `database-1.c2deshkx6ptb.us-east-1.rds.amazonaws.com`

![Alt text](https://github.com/Hazemmmm/Udagram-Udacity/blob/main/Docs/RDS/RDS_DB.jpg "DB Environment")


### Deployment Process In CircleCi:
![Alt text](https://github.com/Hazemmmm/Udagram-Udacity/blob/main/Docs/CircleCi/Screenshot%202022-03-14%20011859.jpg "CircleCi Passed")


### Explaining The App Structure Diagram:

![Alt text](https://github.com/Hazemmmm/Udagram-Udacity/blob/main/Docs/Diagram/Screenshot%202022-03-14%20013026.jpg "App Structure Diagram")


### Explaining The CircleCi PipeLine: 
![Alt text](https://github.com/Hazemmmm/Udagram-Udacity/blob/main/Docs/Diagram/CircleCi%20.jpg "CircleCi PipeLine")
### Package.json SCRIPTS:

      "backend:install": "cd udagram-api && npm install",
      "frontend:install": "cd udagram-frontend && npm install",
      "backend:build": "cd udagram-api && npm run build",
      "frontend:build": "cd udagram-frontend && npm run build",
      "backend:test": "cd udagram-api && npm run test",
      "frontend:test": "cd udagram-frontend && npm run test",
      "backend:deploy": "cd udagram-api && npm run deploy",
      "frontend:deploy": "cd udagram-frontend && npm run deploy"


### Dependencies

```
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

```

### Installation

Provision the necessary AWS services needed for running the application:

1. In AWS, provision a publicly available RDS database running Postgres. <Place holder for link to classroom article>
1. In AWS, provision a s3 bucket for hosting the uploaded files. <Place holder for tlink to classroom article>
1. Export the ENV variables needed or use a package like [dotnev](https://www.npmjs.com/package/dotenv)/.
1. From the root of the repo, navigate udagram-api folder `cd starter/udagram-api` to install the node_modules `npm install`. After installation is done start the api in dev mode with `npm run dev`.
1. Without closing the terminal in step 1, navigate to the udagram-frontend `cd starter/udagram-frontend` to intall the node_modules `npm install`. After installation is done start the api in dev mode with `npm run start`.

## Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd starter/udagram-frontend`
1. `npm run test`
1. `npm run e2e`

There are no Unit test on the back-end

### Unit Tests:

Unit tests are using the Jasmine Framework.

### End to End Tests:

The e2e tests are using Protractor and Jasmine.

## Built With

- [Angular](https://angular.io/) - Single Page Application Framework
- [Node](https://nodejs.org) - Javascript Runtime
- [Express](https://expressjs.com/) - Javascript API Framework

## License

[License](LICENSE.txt)
