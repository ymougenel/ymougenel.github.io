---
layout: default
title: Reference Collector 
excerpt_separator: <!--more-->
tags: [kotlin, spring-boot, thymeleaf, ansible, docker]
---

A website that helps you gather, store and share references

Switching between computers and browsers made my history bookmarks quite messy. 

Reference Collector is designed to keep track of the articles I read, and share those easily.
![screenshot](../assets/reference_collector.png)
<!--more-->

I decided to make the project public: the 1.0.0 release add a Keycloak authentication feature.

## Technical environment
* Dev: Kotlin, Springboot 2 & thymeleaf
* CI/CD: Docker, jenkins & ansible
* Server: Centos7, Ha-proxy & let's encrypt
