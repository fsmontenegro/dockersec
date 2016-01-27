# Docker Intro



## What is Docker?

### Docker, the platform <!-- .element: class="fragment" data-fragment-index="1" -->

Docker is a container based platform used to package and run applications in a variety of systems <!-- .element: class="fragment" data-fragment-index="2" style="color: blue"-->

### Docker, the company <!-- .element: class="fragment" data-fragment-index="3" -->

[Docker Inc. (https://www.docker.com/company)](https://www.docker.com/company)  <!-- .element: class="fragment" data-fragment-index="4" style="color: blue"-->

Note: 1 min 8.5-9.5



## Software package and distribution challenge

### Old Way - Hosted applications

![](http://fsmontenegro.github.io/dockersec/images/old_way_hosted.png) <!-- .element: style="border:1px grey" -->

Note: 3 min 9.5-12.5
  - No isolation
    + Isolation only by segregating servers - Inefficient
  - Common libraries/dependencies
  - Highly coupled with OS


### Virtual machines

![](http://fsmontenegro.github.io/dockersec/images/vms.png) <!-- .element: style="border:1px grey" -->

Note: Speaker notes
  - Isolation
    + Duplication / Inefficient
  - Highly coupled with Guest OS


### Enter the container

![](http://fsmontenegro.github.io/dockersec/images/containers.png) <!-- .element: style="border:1px grey" -->

Note: Speaker notes
  - Some isolation
  - Independent libs - avoid dependency hell
  - Loosely coupled with OS



## Why Docker?

- Linux containers
  + Around for a *long* time (Open VZ, LXC, etc)
  + Not very "friendly"
- Docker streamlines the process and makes it very easy to create and use containers
  + Speed (Development/Scalability)
  + Portability
  + Driver to DevOps and Microservices

Note: 1.5 min 12.5-14



## What do you need to run Docker?

- Recent Linux Kernel (3.8+)
  + Namespaces
  + cGroups
- Network connection

Note: 0.5 min 14-14.5



## Docker architecture in a nutshell

![](http://fsmontenegro.github.io/dockersec/images/what-is-vm-diagram.png) <!-- .element: style="border:1px grey" -->

<small>Source: <a href="https://www.docker.com/what-docker">https://www.docker.com/what-docker</a></small>

Note: 5 min 14.5-19.5


![](http://fsmontenegro.github.io/dockersec/images/architecture.svg) <!-- .element: style="border:1px grey" -->

<small>Source: <a href="https://docs.docker.com/engine/introduction/understanding-docker/">https://docs.docker.com/engine/introduction/understanding-docker/</a></small>



## Docker demo

Note: 10 min 19.5-29.5
