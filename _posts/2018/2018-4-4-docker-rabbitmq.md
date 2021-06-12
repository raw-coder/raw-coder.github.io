---
layout: post
current: post
thumbnail: assets/img/javascript.png
navigation: True
title: rabbitMQ docker로 실행하기
date: 2018-4-4
tags: [story]
class: post-template
subclass: 'post tag-translation'
author: raw-coder
published: true
---

### rabbitMQ docker로 실행하기 ###

> docker 설치

기존 버전의 docker 설치되어 있는 경우 우선 삭제합니다.

``` bash
sudo apt-get remove docker docker-engine docker.io
```

sudo 명령으로 실행하지 않기 위해 권한 등록 후 docker를 실행합니다.

``` bash
sudo usermod -aG docker username
sudo service docker restart
```
> rabbitMQ 설치

rabitmq docker image 를 검색합니다.

``` bash
sudo docker search rabbitmq
```

``` bash
NAME                                           DESCRIPTION                                     STARS               OFFICIAL            AUTOMATED
rabbitmq                                       RabbitMQ is an open source multi-protocol me…   1855                [OK]
tutum/rabbitmq                                 Base docker image to run a RabbitMQ server      15
frodenas/rabbitmq                              A Docker Image for RabbitMQ                     12                                      [OK]
bitnami/rabbitmq                               Bitnami Docker Image for RabbitMQ               9                                       [OK]
sysrun/rpi-rabbitmq                            RabbitMQ Container for the Raspberry Pi 2 (b…   6
kbudde/rabbitmq-exporter                       rabbitmq_exporter for prometheus                6                                       [OK]
gonkulatorlabs/rabbitmq                        DEPRECATED: See maryville/rabbitmq              5                                       [OK]
aweber/rabbitmq-autocluster                    RabbitMQ with the Autocluster Plugin            5
arm32v7/rabbitmq                               RabbitMQ is an open source multi-protocol me…   4
cyrilix/rabbitmq-mqtt                          RabbitMQ MQTT Adapter                           4                                       [OK]
mikaelhg/docker-rabbitmq                       RabbitMQ in Docker.                             3                                       [OK]
gavinmroy/alpine-rabbitmq-autocluster          Minimal RabbitMQ image with the autocluster …   2
pivotalrabbitmq/rabbitmq-autocluster           RabbitMQ with the rabbitmq-autocluster plugi…   2
luiscoms/openshift-rabbitmq                    RabbitMQ docker image to use on Openshift ba…   2                                       [OK]
smebberson/alpine-rabbitmq                     A Docker image for running RabbitMQ on Alpin…   2                                       [OK]
henrylv206/rabbitmq-autocluster                RabbitMQ Cluster                                1                                       [OK]
authentise/rabbitmq                            A RabbitMQ image that will run a bash script…   1                                       [OK]
cvtjnii/rabbitmq                                                                               1
pdffiller/rabbitmq                             Rabbitmq 3.7.3 with delayed_message plugin,c…   0
ekesken/rabbitmq                               docker image for rabbitmq that is configurab…   0                                       [OK]
pivotalrabbitmq/rabbitmq-server-buildenv       Image used to build and test RabbitMQ server…   0
hoist/rabbitmq-cluster                         Hoist's RabbitMQ Cluster Image                  0                                       [OK]
cflondonservices/london-services-ci-rabbitmq                                                   0
callforamerica/rabbitmq                        RabbitMQ (stable) w/ Kubernetes fixes & mani…   0                                       [OK]
newsdev/rabbitmq                               rabbitmq:olympics Extends official rabbitmq …   0                                       [OK]
```

간단한 설정과 함께 rabbitmq 를 실행합니다.
username, password, port 등을 설정합니다. management 페이지의  port는 8088로 설정하였습니다.

``` bash
docker run -d --name rabbitmq -p 5672:5672 -p 8088:15672 --restart=unless-stopped -e RABBITMQ_DEFAULT_USER=guest -e RABBITMQ_DEFAULT_PASS=guest rabbitmq:management
```

![rabbitMQ_management_page](/assets/img/rabbitMQ_management.png)

