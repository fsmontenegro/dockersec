# Docker Security

<small>

Fernando Montenegro, CISSP - [@fsmontenegro](https://twitter.com/fsmontenegro)

Ricardo Gerardi - [@ricardogerardi](https://twitter.com/ricardogerardi)

TASK Jan 27, 2016
</small>



### Why are we here?

Google Trends: "Microservices"

![](http://fsmontenegro.github.io/dockersec/images/microservicesGT.png)


Google Trends:  "Docker"

![](http://fsmontenegro.github.io/dockersec/images/DockerGT.png)


Google Trends: "Kubernetes"

![](http://fsmontenegro.github.io/dockersec/images/kubernetesGT.png)



### Microservices?
![](http://fsmontenegro.github.io/dockersec/images/microservicesF5.png)
<small>
(Source: F5)
</small>


### Microservices
*"Many development teams have found the microservices architectural style to be a* **superior** *approach to a monolithic architecture. But other teams have found them to be a productivity-sapping* **burden**. *Like any architectural style, microservices bring costs and benefits. To make a sensible choice you have to understand these and apply them to your specific context.""*

<small>
Martin Fowler (http://martinfowler.com/articles/microservice-trade-offs.html)
</small>


### Significant benefits
* Support CI/CD practices
* Easier to achieve scale
* Operational benefits of "DevOps"



### DataDog Container Survey

(https://www.datadoghq.com/docker-adoption/)

Two schools of thought:
* Containers as up&down microservices
* Containers as "lightweight servers" that stay up


![](http://fsmontenegro.github.io/dockersec/images/ddContainerTypes.png)


![](http://fsmontenegro.github.io/dockersec/images/ddContainerLife.png)



### What we found

<img src="http://fsmontenegro.github.io/dockersec/images/Dwarrowdelf_LoTR.png">


<img src="http://fsmontenegro.github.io/dockersec/images/DockerIceberg.jpg"  height="700" alt="Iceberg">



### About us - Fernando
[@fsmontenegro](https://twitter.com/fsmontenegro)

<table>
<tr>
<td style="vertical-align: top;">
<ul>
<li>Sales Engineer
<ul>
<li>Network Security (Micro-segmentation)
</ul>
<li>CompSci ’94
<li>Greying hair
</ul>

<ul>
<li>Curious
<ul>
<li>Finance (DIY)
<li>Economics (EMH, Behaviour)
<li>Data Science (Coursera)
</ul>
</td>

<td style="vertical-align: top;">
<img src="http://fsmontenegro.github.io/dockersec/images/fmcat.png" height="400">
</td>
</tr>
</table>



## About us - Ricardo

[@ricardogerardi](https://twitter.com/ricardogerardi)

<table>
<tr>
<td style="vertical-align: top;">
<ul>
<li>Senior IT Consultant
<ul>
<li>Network Management/Monitoring
</ul>
<li>IBM Netcool Certified
<li>Uncertified father (2x)
</ul>

<ul>
<li>Interests
<ul>
<li>Linux/UNIX
<li>Emerging technologies
<li>Data Science
</ul>
</td>

<td style="vertical-align: top;">
<img src="http://fsmontenegro.github.io/dockersec/images/tux_darkvador.png" height="400">
</td>
</tr>
</table>
