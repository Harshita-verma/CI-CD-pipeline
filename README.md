# CI-CD-pipeline
Jenkins is a open source to automate entire software development lifecycle
Stages of ci cd pipleine:
source code--> Build stage-->tesing stage-->Deploy stage.
In this project i am using the tools for setup the ci cd pipeline:-
Git , Jenkins,Ansible, Kubernetes cluster.
Steps to follow as:
I am using AWS cloud to implement this ci cd pipeline.
Create 3 instance first for ansible second for jenkins and third one for webserver
also establish connection over them using ssh.
First developer Push their code into github(version control system) after that webhook(automatically trigger jenkins to build) trigger to jenkins to start build that code.
Jenkins establish ssh connection with Ansible and push the dockerfile to ansible for building the image ansible push that image to registery(dockerhub).
Ansible run playbook which has ip of weberver and run kubectl command.asnible establish ssh connection with webserver. webserver pulling the image from doockerhub and start run container after that it deploy  webapplication on the kubernetes cluster.



