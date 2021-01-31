# interview-challenge-cloudfront-s3
Interview Challenge repository for cloudfront S3 Bucket setup

## Pre Requisites
- Personal AWS Account (You can use AWS free tier for this exercise , so you should not get charges on your card)
- Fork this repository to your personal github repo.  You will be submitting a PR to this repository to submit your response.


## Goals of the exercise
- The goal is to understand how you handle things outside your comfort zone
- Ability to demonstrate technical skills with cloudformation
- Ability to demonstrate DevOps skills on how you setup and automate a project.   This project uses React App,   but as a DevOps Lead/Architect/Engineer,  we might have to deal with changing technologies like NodeJS, Java, .Net, GoLang, Ruby, Python etc.  I do not expect candidate to have knowledge on all languages,  but using your expertise in one technology and ability to quickly learn and adapt to other tech stack. 
- **Feel free to ask questions,  negotiate scope** .  Happy to have a call as well for any clarifications. 
- **Timing**:  Feel free to negotiate the scope and timebox the excercise to a maximum of 3 days.  

## Problem
I have a react application that I need to host it using AWS.   Since I am just launching the application,  I do not expect a lot requests hitting the site,  but as the customer base for my site increases,  I expect the solution to scale automatically with the demand.  For the scope of this exercise, we will focus only on the web aspect of the site.  The security is a big concern for this application. 

- Site needs to be deployed on S3.  S3 needs to be completely locked down , with no direct public access.
- Site is accessed publicly using cloudfront .  But cannot be accessed directly using S3 URL (without authentication). 
- The site will be accessed using https.  For this exercise we can use default cloudfront domain, so you do not need to use your custom domain.
- Infrastructure needs to be deployed using cloudformation (Use YAML) . Since my stack will grow and we have to add other tiers in the stack,  we need a modular approach to organize the stack. 
- - Parent Stack :  Place holder for the complete application.
  - Webapp Stack:  Hosts infrastructure components for my web application.  

## Technical Guidance
-	We do not need any fancy site as it is not testing your web skills.  Out of the box site works.
  - You can setup a quick site using:   https://reactjs.org/docs/create-a-new-react-app.html#create-react-app
  - After you have created the starter app,  you can run command  npm run build  to build static assets.  You can publish those assets to S3 bucket
  - You can add the generated site as part of this repository itself.  You can come up with your structure on how you want to organize the folders
-	Before we have a call to go over the solution,  ensure that you have submitted PR to this repository.
- Infrastructure (Cloudformation files) can be added in a suitable folder in same repo. 
- For deploying content to S3,  you can write a shell script or AWS Commands that copies the build assets to S3 bucket.  (You can use any approach,  one of the approach is to use ```aws sync``` command

## Hints
-	**Google/StackOverflow/AWS Forums/Internet** is your best Friend! As long as you have understanding of solution and are able to demostrate,  it does not matter how you come up with the solution. You can take help from anyone.
-	https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html
- It is ok not to automate everything using cloudformation for this excercise. As long as cloudfront distribution and S3 bucket for hosting content can be added,  it is a good enough demonstration of your cloudformation skills.

*All the best!*



