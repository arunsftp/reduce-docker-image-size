                        ** How to Reduce Docker Image Size: 6 Optimization Methods**

If you want to reduce docker image size, you need to use the standard best practices in building a Docker Image.

This blog talks about different optimization techniques that you can quickly implement to make the smallest and minimal docker image. We will also look at some of the best tools for Docker Image Optimization.

Docker as a container engine makes it easy to take a piece of code & run it inside a container. It enables engineers to collect all the code dependencies and files into a single location which can be run anywhere, quite quickly & easily.

The whole concept of “run anywhere” images starts from a simple configuration file called Dockerfile. First, we add all the build instructions, such as the code dependencies, commands, and base image details, in Dockerfile.

                        ** Need for Docker Image Optimization**
Even though the Docker build process is easy, many organizations make the mistake of building bloated Docker images without optimizing the container images.

In typical software development, each service will have multiple versions/releases, and each version requires more dependencies, commands, and configs. This introduces a challenge in Docker image build, as now – the same code requires more time & resources to be built before it can be shipped as a container.

I have seen cases where the initial application image started with 350MB, and over time it grew to more than 1.5 GB.

Also, by installing unwanted libraries, we increase the chance of a potential security risk by increasing the attack surface.

Therefore, DevOps engineers must optimize the docker images to ensure that the docker image is not getting bloated after application builds or future releases. Not just for production environments, at every stage in the CI/CD process, you should optimize your docker images.

Also, with container orchestration tools like Kubernetes, it is best to have small-sized images to reduce the image transfer and deploy time.

How to Reduce Docker Image Size?
If we take a container image of a typical application, it contains a base image, Dependencies/Files/Configs, and cruft (unwanted software).

Docker application image components.
So it all boils down to how efficiently we can manage these resources inside the container image.

Let’s look at different established methods of optimizing Docker images. Additionally, we have given practical examples to understand docker image optimization in real time.

Either you use the examples given in the article or try the optimization techniques on existing Dockerfiles.

The following are the methods by which we can achieve docker image optimization.

Using distroless/minimal base images
Multistage builds
Minimizing the number of layers
Understanding caching
Using Dockerignore
Keeping application data elsewhere
Docker Excercise Files: All the application code, Dockerfiles, and configs used in this article are hosted this Github repository. You can clone it and follow along the tutorial.
