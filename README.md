# AzureDevops-CICD-pipeline
BoardgameListingWebApp
Description
Board Game Database Full-Stack Web Application. This web application displays lists of board games and their reviews. While anyone can view the board game lists and reviews, they are required to log in to add/ edit the board games and their reviews. The 'users' have the authority to add board games to the list and add reviews, and the 'managers' have the authority to edit/ delete the reviews on top of the authorities of users.

Technologies:
Java
Spring Boot
Amazon Web Services(AWS) EC2
Thymeleaf
Thymeleaf Fragments
HTML5
CSS
JavaScript
Spring MVC
JDBC
H2 Database Engine (In-memory)
JUnit test framework
Spring Security
Twitter Bootstrap
Maven


PROCEDURE: PROJECT STEPS

STEP 1: SETTING UP THE INFRASTRUCTURE
> 1. Create a Virtual Machine
> Connect to it via SSH and Set up Infrastructure  JAVA , MAVEN , DOCKER
> We use this Virtual Machine as a SELF-HOSTED Agent  Beacause I use Free Trail account which does not support built in Azureagentpool like AzurePipeline
> 2. Create an Azure Kubernetes cluster

STEP 2: PREPARE SOURCE CODE REPOSITORY (FORK THE REPOSITORY)
> Navigate to the repository you want to fork, Locate the fork button, choose the destination and wait for the fork to complete
> Navigate to AzureDevops go to the Repos Tab and Import the Repository

STEP 3. CREATE BUILD PIPELINE
> Navigate through the Pipeline tab then click on Create pipeline for this project I'm using the Classic Editor for creating the pipeline
> Add task to the Agent job like MAVEN TEST, MAVEN PACKAGE, SONARQUBE PREPARE CONFIGURATION, RUN CODE ANALYSIS, DOCKER BUILD AND PUSH and provide the Required information.
> Copy the jar files to COPY.jar, Manifest files to COPY MANIFEST and Publish Artifact to the Drop location
 
STEP 4. CREATE RELEASE PIPELINE
> Navigate through the Pipeline tab under click on Release Pipeline
> Create new Release Pipeline and Add Artifact from the drop location and in the task section search for the kubectl installer and kubectl apply and add those tasks

STEP 5. ENABLE CI/CD
> Enable Continous integration and continous deployment triggers

STEP 6. RUN THE PIPELINE

STEP 7. VERIFY THE DEPLOYMENT
