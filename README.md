# Docker
A repository for developing, maintaining, and distributing a consistent programming environment.

## How To Guide

1. Download Docker from https://www.docker.com/
2. Install Docker and run it
3. Clone the Git repository anywhere on your local system.
4. Navigate to the repository (i.e., have it as your working directory)
5. Run the following command on the shell
```
docker-compose -f docker-compose.yml up -d container_name
```
To start the RStudio, Jupyter Lab, and VS Code all together omit the container_name argument.

## Containers

### RStudio

RStudio will be accessible at http://localhost:8787/

This container includes R v3.6.1 and many R packages.

### Jupyter Lab

Jupyter Lab will be accessible at http://localhost:8888/lab

When prompted for a password, the password is: *jupyter*.

The available kernels include R v3.6.1, Python v3.7.6, and Julia v1.3.1.

For Julia, run the following lines before installing packages to use the user library.
```
empty!(DEPOT_PATH)
push!(DEPOT_PATH, joinpath(homedir(), ".julia"))
```

### VS Code

Visual Studio Code with Julia is accesible at http://localhost:8080/

This container includes Julia v1.3.1.

## Volumes

R packages are installed to `docker/R/user-library`

Julia packages are installed at `docker/julia/.julia`
