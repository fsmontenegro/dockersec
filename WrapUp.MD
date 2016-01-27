# Wrapping Up



### Looking at the Future

* Containers exist in a continuum of options.

* Unikernels
  + one degree further
  + compile kernel for application
  + [potentially bad idea?](https://www.joyent.com/blog/unikernels-are-unfit-for-production)
    + Undebuggable?

* Serverless Architecture?
  + AWS Lambda
  + Azure Service Fabric


  ![](http://fsmontenegro.github.io/dockersec/images/unikernels.png)




### Wrapping up

* Docker Security "Anti-Patterns" <!-- .element: class="fragment" data-fragment-index="1" -->
  + free-for-all (unrestricted containers in Prod) <!-- .element: class="fragment" data-fragment-index="1" -->
  + treating containers as servers <!-- .element: class="fragment" data-fragment-index="1" -->

* Recommendations for Security <!-- .element: class="fragment" data-fragment-index="2" -->
  + Don't try to stop it!!! <!-- .element: class="fragment" data-fragment-index="2" style="font-weight: bold"-->
  + recognize massive potential for disruption <!-- .element: class="fragment" data-fragment-index="2" -->
  + no agents on containers <!-- .element: class="fragment" data-fragment-index="3" -->
  + watch for outbound traffic <!-- .element: class="fragment" data-fragment-index="3" -->
  + keep up to date (news!) <!-- .element: class="fragment" data-fragment-index="3" -->
  + rethink approach ("cattle, not pets") <!-- .element: class="fragment" data-fragment-index="3" -->


### Docker all over
Last few weeks of news:

* [Docker buys Unikernel](http://techcrunch.com/2016/01/21/docker-acquires-unikernel-systems-as-it-looks-beyond-containers/)
* [Arista announces Container support in EOS](https://www.sdxcentral.com/articles/news/arista-outfits-eos-for-containers-hybrid-clouds/2016/01/)
* [Citrix supports NetScaler as Container](https://www.citrix.com/blogs/2015/12/15/early-christmas-present-a-big-surprise-in-a-small-container/)
* [Amazon announces Docker 1.9 support](https://aws.amazon.com/about-aws/whats-new/2016/01/amazon-ec2-container-service-supports-docker-1-9/)



### Resources!

<small>
Twitterfolk:

<table>
<tr>
<td>
<ul>
<li>[@mattnowina](https://twitter.com/mattnowina) - AWS architect, tons of Docker links

<li>[@diogomonica](https://twitter.com/diogomonica) - Docker Security

<li>[@frazelledazzell](https://twitter.com/frazelledazzell) - Tons of Container work

<li>[@nigelpoulton](https://twitter.com/nigelpoulton) - Pluralsight course

<li>[@mierdin](https://twitter.com/mierdin) - KeepingItClassless, TechFieldDay
</ul>
</td>
<td>
[@blinken_lichten](https://twitter.com/blinken_lichten) - DevOps

[@jaybeale](https://twitter.com/jaybeale) - Shmoocon 2016 preso

[@docker](https://twitter.com/docker) and [@dockercon](https://twitter.com/dockercon) - Company & Conference

[@kubeconio](https://twitter.com/kubeconio) - Kubernetes confab
</td>
</tr>
</table>

Websites:
  * [TheNewStack](http://thenewstack.io/) - portal of all things "modern" stacks
  * [Packet Pushers](http://packetpushers.net/datanauts-podcast/) - Network-focused approach
  * [RunC](https://runc.io/) - Open Container Initiative

</small>
