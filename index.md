---
layout: default
---


## [The Concept of a Linux Firewall: IPtables](https://www.youtube.com/watch?v=eC8scXX1_1M)

[//]: #  There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

## About iptables
iptables is a command-line firewall utility that uses policy chains to allow or block traffic. When a connection tries to establish itself on your system, iptables looks for a rule in its list to match it to. If it doesn’t find one, it resorts to the default action.

iptables almost always comes pre-installed on any Linux distribution. To update/install it, just retrieve the iptables package:


## Types of Chains
iptables uses three different chains: input, forward, and output.

## Input:
This chain is used to control the behavior for incoming connections. For example, if a user attempts to SSH into your PC/server, iptables will attempt to match the IP address and port to a rule in the input chain.

## Forward
This chain is used for incoming connections that aren’t actually being delivered locally. Think of a router – data is always being sent to it but rarely actually destined for the router itself; the data is just forwarded to its target. Unless you’re doing some kind of routing, NATing, or something else on your system that requires forwarding, you won’t even use this chain.

![](https://www.howtogeek.com/wp-content/uploads/2013/12/2-packets-processed.jpg?trim=1,1&bg-color=000&pad=1,1) 

## Output 
This chain is used for outgoing connections. For example, if you try to ping howtogeek.com, iptables will check its output chain to see what the rules are regarding ping and howtogeek.com before making a decision to allow or deny the connection attempt.

## Policy Chain Default Behavior
Before going in and configuring specific rules, you’ll want to decide what you want the default behavior of the three chains to be. In other words, what do you want iptables to do if the connection doesn’t match any existing rules?
To see what your policy chains are currently configured to do with unmatched traffic, run the iptables -L command.

![](https://www.howtogeek.com/wp-content/uploads/2013/12/3-policy-setting.jpg?trim=1,1&bg-color=000&pad=1,1)

As you can see, we also used the grep command to give us cleaner output. In that screenshot, our chains are currently figured to accept traffic.

More times than not, you’ll want your system to accept connections by default. Unless you’ve changed the policy chain rules previously, this setting should already be configured. Either way, here’s the command to accept connections by default:


### 


```
Thank you readers, and wait for next week blog
For Contact e-mail me at ramirez368@hotmail.com

```
