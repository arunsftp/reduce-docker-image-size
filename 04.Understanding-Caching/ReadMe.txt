Often, the same image has to be rebuilt again & again with slight modifications in code.

As Docker uses layered filesystem, each instruction creates a layer. Due to which, Docker caches the layer and can reuse it if it hasn’t changed.

Due to this concept, it’s recommended to add the lines which are used for installing dependencies & packages earlier inside the Dockerfile – before the COPY commands.

The reason behind this is that docker would be able to cache the image with the required dependencies, and this cache can then be used in the following builds when the code gets modified.

Also, COPY and ADD instructions in a Dockerfile invalidate the cache for subsequent layers. Which means, Docker will rebuild all the layers after COPY and ADD.

This means, it is recomended to add instructions that are less likely to change earlier in the Dockerfile.

For example, let’s take a look at the following two Dockerfiles.