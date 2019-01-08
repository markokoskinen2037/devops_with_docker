### When to use Docker and what are the benefits?

In the beginning of this course I had heard of Docker. I was under the impression that it makes deployment and installation  a lot simpler and faster. Those are indeed, in my opinion the, fundamental features of Docker that make it so great. I think there is no excuse not to use Docker.

Lets have a look at an example. Say you want to test out an open source project, available in GitHub. Lets also assume that this project is quite complicated and requires a lot of libraries and dependencies to be installed in order to work. Docker image for the project is available in DockerHub.

#### *You now have two options:*

**(1)** Clone the project and install all of the required libraries and dependencies on your local machine.
This can be complicated, especially, if the installation instructions are not well made.

**(2)** Install docker and use the pre-made Dockerfile to build and run the image.
Testing the project using docker is really simple. First you need to Install docker and then run the command provided in the project DockerHub page to download and run the pre-made image.


If the installation instructions are well made, then **(option 1)** can be rather straightforward. However, if one of the required dependencies encounters an error while installing – you might be in for a debugging session that lasts for hours. Your local machine gets filled with libraries and dependencies that you wont need once you are done testing the project – causing your machine to lose precious disk-space.

With Docker **(option 2)** there is very little that can go wrong, because the image published on DockerHub is basically guaranteed to work. Also, Docker does not install any of the projects dependencies/libraries on your local machine. So when you are done with the project, you can get all your disk-space back with a single command. ```docker stop $(docker ps -aq) && docker system prune –force```