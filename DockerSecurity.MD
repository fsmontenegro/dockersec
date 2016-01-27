# Docker Security



##  First things first...
* Containers vs. VMs?
  + Containers not as isolated as VMs.
  + but much more isolated than processes...
  + cgroups & namespaces
* Containers are OS-dependant.

* Containers for multi-tenancy? Not so fast...



## Security FOR Docker

How to "secure" the Docker pipeline

How to "secure" Docker containers themselves


### Security for Docker Images

* Secure Registry/Mirror Access
* **Getting trustworthy images**
  + trusted sources - docker hub, private registry
  + building secure
  + Docker Content Trust (1.8)
    "only signed content in production"


### Docker's Project Nautilus
    * Docker securing images on DockerHub
    * Image security
    * Component inventory/license management
    * Image optimization
    * Basic functional testing


### Other Considerations
* Containers are stateless
  + Can mount additional volumes
* How to do Secrets Management?
  + ENV variables - not recommended
  + Key/Value Pair solutions - Hashicorp et al.
  + Embedded in orchestration (Kubernetes)
  + Custom solutions



## Security FROM Docker

How does Docker protect containers & hosts?


### Securing the Host itself
* Dedicated OS
  + Atomic
  + CoreOS
* Harden OS
* Harden kernel
      https://grsecurity.net/compare.php
      http://mjg59.dreamwidth.org/38158.html


### Namespaces & Cgroups
* PID – process isolation
* Network – NICs, IPs, routing tabes et al.
* UTS – hostnames
* Mount – filesystem layouts/ properties
* IPC – interprocess communication
* User – users ("root" != **root**)

* Control groups: resource utilization (RAM, swap, CPU, IO, controls)




## Security BY Docker

Leveraging Docker features for security



## TEMP - To Move


## Securing Containers
    read-only FileSystems
      came in Docker 1.5
      specify logs in another volume or remote
    seccomp
      secure computing mode
      filter system calls
      VERY nice!


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


### Clair by CoreOS
* Security scanning of images - https://coreos.com/blog/vulnerability-analysis-for-containers/
* Available on Quay
* Security Scanning Beta - https://blog.quay.io/security-scanning-beta/


## Other
DockerBench
script for best practices
