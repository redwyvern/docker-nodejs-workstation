![](https://img.shields.io/docker/stars/redwyvern/nodejs-workstation.svg)
![](https://img.shields.io/docker/pulls/redwyvern/nodejs-workstation.svg)
![](https://img.shields.io/docker/automated/redwyvern/nodejs-workstation.svg)
[![](https://images.microbadger.com/badges/image/redwyvern/nodejs-workstation.svg)](https://microbadger.com/images/redwyvern/nodejs-workstation "Get your own image badge on microbadger.com")

Redwyvern NodeJs Development Workstation 
========================================

This is image can be used as a general NodeJS development environment.

This image contains software to build the following type of projects:
* NodeJs

Example YAML file:
```
version: '3'
services:

  nodejs-workstation:
    image: docker.artifactory.weedon.org.au/redwyvern/nodejs-workstation
    hostname: nodejs-workstation
    ports:
      - "2222:22"
      - "3000:3000"
    volumes:
      - "/opt/docker-containers/nodejs-workstation/home:/home"
    dns: 192.168.1.50
    networks:
      - dev_nw

networks:
  dev_nw:
```
