
# 2048


This is a recreation of the popular 2048 game by Gabriele Cirulli. The purpose of this Dockerfile is to create the docker images and containers necessary to deploy to AWS using Elastic Beanstalk


## Create image and container
1. Navigate to the folder containing the Dockerfile. 
2. Run the following command to create the docker image out of the Dockerfile, this will name the image 2048-game:  
    docker built -t 2048-game .
3. Run the following command to get the Image ID:
    docker images 
4. Run the following code to create a container from the image:
    docker run -d -p 80:80 <imageid>
5. Your application will be accessible at http://localhost:80 

## Host on AWS Cloud 
1. Open AWS Console 
2. Select Elastic Beanstalk 
3. Create Application
4. Name Application
5. Choose Docker Platform 
6. Under Application code, select upload your code. Select local file and upload Dockerfile
7. Configure Options according to personal preferencess 
8. Create app
    -This will take a few moments to load, but once you see the domain, your app is running on the cloud! 




