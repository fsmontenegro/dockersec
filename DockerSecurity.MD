# Docker Security



##  First things first...
* Containers vs. VMs?
  + Containers not as isolated as VMs.
  + but much more isolated than processes...
  + cgroups & namespaces
* Containers are OS-dependant.

* Containers for multi-tenancy? Not so fast...
  + Containers & VMs :-)



## Security *FOR* Docker

How to secure the Docker "pipeline"

How to secure Docker containers themselves


### Security for Docker Images

* Secure Registry/Mirror Access
* **Getting trustworthy images**
  + trusted sources - docker hub, private registry
  + building secure
  + Docker Content Trust (1.8) [Notary]
    + "only signed content in production"
    + Yubico Keys


### Docker's Project Nautilus
* Docker securing images on DockerHub
* Image security
* Component inventory/license management
* Image optimization
* Basic functional testing


### Clair by CoreOS
* Security scanning of images - https://coreos.com/blog/vulnerability-analysis-for-containers/
* Available on Quay
* Security Scanning Beta - https://blog.quay.io/security-scanning-beta/


### Other Considerations
* Containers are stateless
  + Can mount additional volumes
* How to do Secrets Management?
  + ENV variables - not recommended
  + Key/Value Pair solutions
    + [Vault & Keywhiz](https://www.vaultproject.io/intro/vs/keywhiz.html)
  + Embedded in orchestration ([Kubernetes](http://kubernetes.io/v1.1/docs/user-guide/secrets.html))
  + [Custom solutions](https://engineering.shopify.com/79963908-secrets-at-shopify-introducing-ejson)



## Security *FROM* Docker

How to contain Docker & containers?


### Securing the Host itself
* Dedicated OS
  + Atomic
  + CoreOS
* Harden OS
* Harden kernel ([grsecurity](https://grsecurity.net/compare.php))
* Linux Security Modules
  + AppArmor and SELinux
  + Of note: [Bane](https://github.com/jfrazelle/bane)


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


### Leveraging Docker for Security
* microservice -> reduced attack surface
* r/o FileSystems
* reduced capabilities
* seccomp - filtering system calls
* journaled changes
