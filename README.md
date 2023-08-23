## Table of Contents
1. [Prerequisites](#1-Prerequisites)
1. [How to Use](#2-How-to-Use)
1. [PostgreSQL Versions](#3-PostgreSQL-Versions)

## 1. Prerequisites
You will need to ensure that the following has been installed on the machine where the docker container is to be hosted:
- git (to clone this repo)
- docker
- docker-compose

## 2. How to Use
Follow these steps to get the PostgreSQL docker container running with the help of this repository:
1. Clone this repository to the machine.
1. Edit the `env-template` file and enter the username and password to be used to create the primary super-user role for this PostgreSQL server (these credentials may never be stored in the public online repo!).
1. Rename `env-template` to `.env`.
1. From a terminal with the working directory set to the location of these files, run `docker-compose up -d`.
    - You can also run this from a nother working directory if you specify the path the the `docker-compose.yml` file, please refer to the docker-compose documentation for how to do this.
1. Once the server is up and running, you may confirm that you are able to connect, and then start using it (create additional roles, create and restore databases, etc.).

## 3. PostgreSQL Versions
This repository is currently to be used to start up a PostgreSQL 13 container. For now, this is the only version supported.

In future, we plan to update the files in the main branch to support newer PostgreSQL versions. With each version bump, the plan is to first make a branch with the files for the current version - e.g. when moving to PostgreSQL 15 or 16, we will first make a branch to keep the files for PostgreSQL 13, so they remain accessible.