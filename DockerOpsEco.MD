# Operations and Ecosystem



## Where to deploy Docker?

### On premises

- Baremetal (on Linux)
- Virtual Machines
- IaaS, OpenStack, etc


### Public Cloud Providers

- AWS
- Microsoft Azure
- Digital Ocean
- Google Container engine


### PaaS Providers

- RedHat OpenShift
- Heroku
- Cloud Foundry
- IBM Bluemix

Note: Usually supporting their own security features:
  - Certificate Based Authentication
  - Multiple identity Providers
  - Roles
  - etc



## Orchestration / Scheduling

- Kubernetes
- Docker Swarm
- Apache Mesos



## Networking

### Basic Networking

![](http://fsmontenegro.github.io/dockersec/images/docker-net-bridge.png) <!-- .element: style="border:1px grey" -->

Note: L2/Bridge
  - No outbound filtering
  - Inter host comm depends on NAT


### Overlay Networking

![](http://fsmontenegro.github.io/dockersec/images/docker-net-overlay.png) <!-- .element: style="border:1px grey" -->

Note: Overlay networks
  - Provided by Orchestration engines
  - VxLAN (encapsulates L2 frames in IP packets, "emulates bridge over ip")
  - KV Stores
  - DNS



## Monitoring

### Challenges
- Scalability (100s of containers in a single host)
- Host Monitoring x Container Monitoring
- Container instrumentation (1 process/container philosophy)
- API instability


### Container monitoring solutions
- [Google cAdvisor](http://192.168.56.102:8080/containers/)
- Sysdig Cloud
- Weaveworks
- New relic


### Container Log Management
- ELK Stack
- Splunk
