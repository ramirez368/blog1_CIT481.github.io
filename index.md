---
layout: default
---


## [The Wide World of Internet of Things](https://www.youtube.com/watch?v=LlhmzVL5bm8)

[//]: #  There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

## About iptables
iptables is a command-line firewall utility that uses policy chains to allow or block traffic. When a connection tries to establish itself on your system, iptables looks for a rule in its list to match it to. If it doesn’t find one, it resorts to the default action.

iptables almost always comes pre-installed on any Linux distribution. To update/install it, just retrieve the iptables package:


## Types of Chains
iptables uses three different chains: input, forward, and output.

Input – This chain is used to control the behavior for incoming connections. For example, if a user attempts to SSH into your PC/server, iptables will attempt to match the IP address and port to a rule in the input chain.

Forward – This chain is used for incoming connections that aren’t actually being delivered locally. Think of a router – data is always being sent to it but rarely actually destined for the router itself; the data is just forwarded to its target. Unless you’re doing some kind of routing, NATing, or something else on your system that requires forwarding, you won’t even use this chain.

![](https://www.howtogeek.com/wp-content/uploads/2013/12/2-packets-processed.jpg?trim=1,1&bg-color=000&pad=1,1) 

## Output 
This chain is used for outgoing connections. For example, if you try to ping howtogeek.com, iptables will check its output chain to see what the rules are regarding ping and howtogeek.com before making a decision to allow or deny the connection attempt.


![ ](https://dl.cdn-anritsu.com/images/tm/solutions/mt1000a-05/mt1000a-5g-ecpri-01e.jpg?la=en-us) 

## 




### 


```
Thank you readers, and wait for next week blog
For Contact e-mail me at ramirez368@hotmail.com

```
