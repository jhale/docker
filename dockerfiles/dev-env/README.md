# FEniCS development environment image

This image provides a development environment for building the FEniCS
libraries.  It does not provide an installation of FEniCS. It is intended for
users who want to build their own version of FEniCS. It also serves as a base
image for <https://registry.hub.docker.com/u/fenicsproject/dev>, which does
provide the development version of FEniCS.

To launch the container:

    docker run -t -i fenicsproject/dev-env:latest

We do provide a helper script (fenics.conf) in this container to compile FEniCS
automatically:

    update_fenics

If you want to have access to the source code and build files in the container
on the host machine then run:

    docker run -v $(pwd)/build:/home/fenics/build -t -i fenicsproject/dev-env:latest
    
If you would like to have another directory on the host shared into the
container then run:

    docker run -v $(pwd)/shared:/home/fenics/shared -t -i fenicsproject/dev-env:latest
