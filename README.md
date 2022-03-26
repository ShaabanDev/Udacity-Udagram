# Udagram

This application is a simple application that is used to apply hosting principals using AWS services along with CI/CD principals using circleci integeration. 
The udagram application is a fairly simple application that includes all the major components of a Full-Stack web application.

## Getting Started

In order to test deployment on CircleCI 

1 - Upload code on your github repository.

2 - In the environment variables of your project in circleCi add the following variables.

    -   POSTGRES_USERNAME = *******
    -   POSTGRES_PASSWORD = *******
    -   POSTGRES_DB = *******
    -   PORT = *******
    -   POSTGRES_HOST = ****************************
    -   AWS_REGION = *******
    -   AWS_DEFAULT_REGION = *******
    -   URL = ******************************************
    -   JWT_SECRET = *******
    -   EB_APP = *******
    -   EB_ENV = *******
    -   AWS_BUCKET = *******
    -   AWS_ACCESS_KEY_ID - IAM user access key for AWScli and elastic beanstalk deployment
    -   AWS_SECRET_ACCESS_KEY - Secret for IAM user

3 - Start the deployment process.

In order to view current deployment on S3 

Frontend Environment:
        S3 bucket: udagram-new-bucket
        S3 URL: http://my-01033674227-bucket.s3-website-us-east-1.amazonaws.com/

![Alt text](https://github.com/mosh3ban/Udacity-Udagram/blob/master/documentation/screen_shots/s3.JPG "Frontend Environment")


In order to view current deployment on Elastic beanstalk

Backend Environment:
        URL: http://udagram-api-dev.eba-igpzdpsh.us-east-1.elasticbeanstalk.com/

![Alt text](https://github.com/mosh3ban/Udacity-Udagram/blob/master/documentation/screen_shots/eb.JPG "Backend Environment")

        Database endpoint: database-1.c6lozgwarpkj.us-east-1.rds.amazonaws.com

![Alt text](https://github.com/mosh3ban/Udacity-Udagram/blob/master/documentation/screen_shots/rds.JPG "Database endpoint")

        Application name: udagram-api
        Environment name: udagram-api-env

Deployment Pipeline:
        CircleCI 
        GitHub project - https://github.com/mosh3ban/Udacity-Udagram

![Alt text](https://github.com/mosh3ban/Udacity-Udagram/blob/master/documentation/screen_shots/circleci.JPG "Deployment Pipeline")

### Illustration Diagram

- Infrastructure of the application

![Alt text](https://github.com/mosh3ban/Udacity-Udagram/blob/master/documentation/screen_shots/sss.png "Infrastructure of the application")

- Piplining

![Alt text](https://github.com/mosh3ban/Udacity-Udagram/blob/master/documentation/screen_shots/ss.png "Piplining")

### Dependencies

```
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

- An Elastic Beanstalk for hosting backend and APIs

- CircleCI Integrated with github to run the deployment process
```

### Package.json script

  "backend:install": "cd udagram-api && npm install",
        "frontend:install": "cd udagram-frontend && npm install",
        "backend:build": "cd udagram-api && npm run build",
        "frontend:build": "cd udagram-frontend && npm run build",
        "backend:test": "cd udagram-api && npm run test",
        "frontend:test": "cd udagram-frontend && npm run test",
        "backend:deploy": "cd udagram-api && npm run deploy",
        "frontend:deploy": "cd udagram-frontend && npm run deploy"

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


