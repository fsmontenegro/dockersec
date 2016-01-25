---
title: "Docker Security"
author: "Fernando Montenegro & Ricardo Gerardi"
date: "January 24, 2016"
---







## Docker Introduction

### What is Docker? <!-- .element: class="fragment" data-fragment-index="1" -->

Docker is a container based platform used to package and run applications in a variety of systems <!-- .element: class="fragment" data-fragment-index="2" style="color: blue"-->

### What problem does it solve? <!-- .element: class="fragment" data-fragment-index="3" -->

Eliminates the existing chasm between Dev and Sys Admins <!-- .element: class="fragment" data-fragment-index="4" style="color: blue"-->



## Software package and distribution challenge



## Docker architecture in a nutshell

![Alt text](images/what-is-vm-diagram.png) <!-- .element: style="border:1px grey" -->

<small>Source: <a href="https://www.docker.com/what-docker">https://www.docker.com/what-docker</a></small>


![Alt text](images/architecture.svg) <!-- .element: style="border:1px grey" -->

<small>Source: <a href="https://docs.docker.com/engine/introduction/understanding-docker/">https://docs.docker.com/engine/introduction/understanding-docker/</a></small>



# Docker Security

## Securing the Host itself
* Harden OS
* Harden kernel?
      https://grsecurity.net/compare.php
      http://mjg59.dreamwidth.org/38158.html
* Dedicated OS?
      Atomic
      CoreOS

## Securing Containers from Malicious App
    read-only FS
      came in Docker 1.5
      specify logs in another volume or remote
    seccomp
      secure computing mode
      filter system calls
      example
        tcp.json

## Securing Docker daemon and running Containers
    secure Docker API and socket
      access control
        root user, Docker group only on /var/run/docker.sock
      de-containerized aspects
        -net = host, -pid = host
      consider TLS authentication
        --tlsverify
      proper location for certs
        /etc/default/docker

## Securing the Hosts from Docker
    User-namespaces
      root in container is mapped to non-root user
      (experimental)
      more features coming
    SELinux/AppArmor Profiles
      Jessie Frazelle - bane

## Security for Docker Images

    Registry Access
      make sure regular and mirror access via https
        no --insecure-registry
    Getting trustworthy images
      trusted sources - docker hub, private registry
      building secure - See docker site TBD
      Docker Content Trust
        docker 1.8
        requires signed images
          root@debian-jessie:~# export DOCKER_CONTENT_TRUST=1
        "only signed content in production"
  #### Project Nautilus
      Docker securing images on DockerHub
      Image security
      Component inventory/license management
      Image optimization
      Basic functional testing
  #### Clair by CoreOS
      Security scanning of images
        https://coreos.com/blog/vulnerability-analysis-for-containers/
      Available on Quay
        Security Scanning Beta
          https://blog.quay.io/security-scanning-beta/
      https://github.com/coreos/clair

## Other
    DockerBench
      script for best practices



## Operations and Ecosystem (RG)



## Looking at the Future

* Unikernels
  + one degree further
  + compile kernel for application
  + potentially bad idea?

* Serverless Architecture
  + AWS Lambda
  + Microsoft Batch Services



## Wrapping up

* Docker Security "Anti-Patterns"
  + free-for-all (unrestricted containers in Prod)
  + treating containers as servers

* Recommendations
  + **Don't try to stop it!!!**
  + no agents on containers
  + watch for outbound traffic
  + keep up to date (news!)

* People and Resources of Note

On Twitter:
    @mattnowina
    @diogomonica
    @nigelpoulton
    @dockercon
    @kubecon
    @jaybeale
    @mierdin

Websites:
    http://thenewstack.io/
    http://packetpushers.net/datanauts-podcast/

Others:
  RunC
