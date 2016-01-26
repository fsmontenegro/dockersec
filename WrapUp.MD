### Looking at the Future

* Containers exist in a continuum of options.

* Unikernels
  + one degree further
  + compile kernel for application
  + [potentially bad idea?](https://www.joyent.com/blog/unikernels-are-unfit-for-production)

* Serverless Architecture?
  + AWS Lambda
  + Microsoft Batch Services



### Wrapping up

* Docker Security "Anti-Patterns"
  + free-for-all (unrestricted containers in Prod)
  + treating containers as servers

* Recommendations for Security
  + **Don't try to stop it!!!**
  + no agents on containers
  + watch for outbound traffic
  + keep up to date (news!)
  + rethink approach ("cattle, not pets")



### Resources!
* [@mattnowina](https://twitter.com/mattnowina) - AWS architect, tons of great Docker links
* [@diogomonica](https://twitter.com/diogomonica) - Docker Security
* [@nigelpoulton](https://twitter.com/nigelpoulton) - Pluralsight course
* [@mierdin](https://twitter.com/mierdin) - KeepingItClassless, TechFieldDay
* [@jaybeale](https://twitter.com/jaybeale) - BSidesNYC 2016 preso

Also
* [@dockercon](https://twitter.com/dockercon) and [@kubeconio](https://twitter.com/kubeconio)

Websites:
*  [TheNewStack](http://thenewstack.io/)
*  [Packet Pushers](http://packetpushers.net/datanauts-podcast/)

Others:
  [RunC](https://runc.io/)
