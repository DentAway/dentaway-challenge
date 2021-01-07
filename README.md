# DentAway Tech challenge

Aim: create a sample application where you can showcase back and front end skills. 

## Technical requirements 
- Front end: React
- Back end: PHP Laravel - create back end API to serve front end
- Database: MySQL or PostgreSQL 
- Deployment: Docker and docker-compose 
- Use version control of preference with the necessary documentation (overview, setup, run etc.), [atomic commits](https://dev.to/cbillowes/why-i-create-atomic-commits-in-git-kfi) and tags. You need to use a few tags and / or releases from 0.1 to 1.0.0 -  You can decide how you want to split the project, but these need to make sense. Tag 1.0.0 will be the final version with front and back end and all dependencies packaged in Docker images. 


## The challenge
Given a csv file containing a job url and a few other attributes (extracted from the description), you need to load this in the database at the run time in table table_processed. The table will have all the schema needed from the csv columns.  

- On the left hand side of the app, display the content of the url as you see it on the webpage. This is meant to look like a user sees it on the browser.   
- On the right hand side of the app, you need to display the other attributes found in the csv file in a box element. These are meant to be visually checked on the left hand side by the user and validated if the values are correct. The user can edit the field values and on the click of it, the text inside the box will be highlighted on the left hand side (similar to as words are highlighted when you search in the browser). When the user clicks outside the box, text on the left will not be highlighted anymore.    
- Once the edits are done, the user can save the edits by clicking on a save button.  In the back end, the data will be saved in table_validated with the same attributes / schema but new values if edited and a timestamp. 
- The job url load/selection can be random by the click of a button or use a filter to select which job url was not written back to the new table.

## Other things to consider 
- Editing criteria: jobs in London cannot be edited, but viewed only. 
- Intermediate saving / auto-save
- Logs: success, error and consider email notification on error (e.g. SendGrid)
- Authentication: admin account to create users with two roles: admin / view 
- Microservices 
- The code needs to be reusable 
- Performance 


The app should be able to run locally, with all dependencies already tested and ready to be installed in Docker images (Dockerfile and / or Docker Compose needs to be in repo) . The end user should clone the repo and run the Docker images via docker run or docker-compose up commands, as specified in the documentation without worrying about package dependencies or installation steps. This is a highly recommended step and will have the least focus in the evaluation process. It’s just nice to pull and see the app instantly. 

**Docker Resources**
- Docker Laravel image: https://hub.docker.com/r/kamerk22/laravel-alpine/
- Docker PostgreSQL image: https://hub.docker.com/_/postgres 
- Docker compose: https://github.com/thayronarrais/docker-laravel-postgres-nginx 
- https://mherman.org/blog/dockerizing-a-react-app/ 

