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



## Security for Docker Images

    Registry Access
      make sure regular and mirror access via https
        no --insecure-registry
    **Getting trustworthy images**
      trusted sources - docker hub, private registry
      building secure - See docker site TBD
      Docker Content Trust (1.8)
          root@debian:~# export DOCKER_CONTENT_TRUST=1
        "only signed content in production"



## Project Nautilus
      Docker securing images on DockerHub
      Image security
      Component inventory/license management
      Image optimization
      Basic functional testing



## Clair by CoreOS
      Security scanning of images
        https://coreos.com/blog/vulnerability-analysis-for-containers/
      Available on Quay
        Security Scanning Beta
          https://blog.quay.io/security-scanning-beta/
      https://github.com/coreos/clair

## Other
    DockerBench
      script for best practices
