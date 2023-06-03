Deploying Chrome's Dinosaur Game with Elastic Beanstalk
This repository contains the necessary files to deploy Chrome's Dinosaur Game using Docker and Elastic Beanstalk. By following the steps below, you can quickly get the game up and running on Elastic Beanstalk's free tier with default settings.

Prerequisites
Docker: Ensure that Docker is installed on your local machine.
Deployment Steps
Clone this repository to your local machine or download and extract the ZIP file.

Open a terminal and navigate to the project's root directory.

Make sure you are logged in to your Docker account by running the docker login command.

Build the Docker image by executing the following command:

bash
Copy code
docker build -t image_name .
Replace image_name with the desired name for your Docker image.

After the image is built, tag it using the following command:

bash
Copy code
docker tag image_name repository_name:tag
Replace image_name with the name of the image you created in the previous step, repository_name with the name of your Docker repository (e.g., username/repository_name), and tag with the desired tag for your image (e.g., v1.0).

Push the image to your Docker repository with the following command:

bash
Copy code
docker push repository_name:tag
Make sure to replace repository_name and tag with the values you specified in the previous step.

Log in to the AWS Management Console and navigate to Elastic Beanstalk.

Click "Create Application" and provide a name and description for your application.

Choose the "Docker" platform and select the "Upload your code" option.

Click "Choose file" and select the Docker image you pushed to the repository.

On the next page, leave the default settings as they are.

Finally, click "Create application" to initiate the deployment process.

Elastic Beanstalk will now create the necessary environment and deploy the Docker image, which will launch the Chrome's Dinosaur Game. You can access the game by visiting the environment's URL provided in the Elastic Beanstalk console.

Note: When using the free tier, please be aware of the limitations and consider upgrading your account if necessary.
