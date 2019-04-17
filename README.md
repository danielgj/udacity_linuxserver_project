# Full Stack Development Nanodegree - Project Linux Server Configuration

## Introduction

This final project aims to demonstrate the knowledge acquired during the Full Stack Development Nanodegree on Linux Server configuration. The main steps to complete the project are:

* Create a Linux server instance using AWS Lightsail
* Configure users and SSH access
* Configure firewall rules
* Install apache and all the software to be able to run catalog app using PostgreSQL as database
* Deploy and publish transformed catalog app

## Access Details

Instance of Linux server has this public IP: **54.246.181.23**

SSH port is **2200** 

To connect as grader user, a provided SSH key must be used. The script to connect is the following:

`ssh grader@54.246.181.23 -i SSH_KEY_HERE -p 2200`


Catalog web application is accesible in following URL: <http://54.246.181.23.xip.io/>

## Configuration Steps

Several steps has been performed to configure the server:

1. Setup Lightsail instance as described by AWS documentation (see rerefences)
2. Update all installed packages: `sudo apt-get update; sudo apt-get upgrade`
3. Change the SSH port from 22 to 2200 and configure the Lightsail firewall to allow it.
4. Configure the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).
5. Create a new user account named grader.
6. Give grader the permission to sudo.
7. Create an SSH key pair for grader using the ssh-keygen tool.
8. Configure the local timezone to UTC.
9. Install and configure Apache to serve a Python mod_wsgi application.
10. Install and configure PostgreSQL creating a database called *catalog*
11. Create default categories in catalog database
12. Install git
13. Clone catalog app
14. Configure default site in apache to serve the catalog app
15. Adapt catalog app code to connect to Postgres DB
16. Setup access to the server for Oauth with Google
17. Install all python dependencies


## Resources

Following third party resources have been checked to complete the project:

* AWS Lightsail documentation: <https://aws.amazon.com/es/lightsail/faq/>
* Ubuntu PostgreSQL configuration: <https://help.ubuntu.com/lts/serverguide/postgresql.html.en>
* JungleBadger support tutorial on GitHub: <https://github.com/jungleBadger/-nanodegree-linux-server-troubleshoot/blob/master/python3+venv+wsgi/README.md>
