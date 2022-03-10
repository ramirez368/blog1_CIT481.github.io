---
layout: default
---


## [Comparing the 2 Cloud Giants: AWS vs Azure](https://www.youtube.com/watch?v=xCabPpcq8Ac)

[//]: #  There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

## Azure vs. AWS: What is the Difference Between AWS and Azure
iptables is a command-line firewall utility that uses policy chains to allow or block traffic. When a connection tries to establish itself on your system, iptables looks for a rule in its list to match it to. If it doesn’t find one, it resorts to the default action.

iptables almost always comes pre-installed on any Linux distribution. To update/install it, just retrieve the iptables package:


## Types of Chains
iptables uses three different chains: input, forward, and output.

## Input:
This chain is used to control the behavior for incoming connections. For example, if a user attempts to SSH into your PC/server, iptables will attempt to match the IP address and port to a rule in the input chain.

## Forward:
This chain is used for incoming connections that aren’t actually being delivered locally. Think of a router – data is always being sent to it but rarely actually destined for the router itself; the data is just forwarded to its target. Unless you’re doing some kind of routing, NATing, or something else on your system that requires forwarding, you won’t even use this chain.

![](https://www.howtogeek.com/wp-content/uploads/2013/12/2-packets-processed.jpg?trim=1,1&bg-color=000&pad=1,1) 

## Output:
This chain is used for outgoing connections. For example, if you try to ping howtogeek.com, iptables will check its output chain to see what the rules are regarding ping and howtogeek.com before making a decision to allow or deny the connection attempt.

## Policy Chain Default Behavior
Before going in and configuring specific rules, you’ll want to decide what you want the default behavior of the three chains to be. In other words, what do you want iptables to do if the connection doesn’t match any existing rules?
To see what your policy chains are currently configured to do with unmatched traffic, run the iptables -L command.

![](https://www.howtogeek.com/wp-content/uploads/2013/12/3-policy-setting.jpg?trim=1,1&bg-color=000&pad=1,1)

As you can see, we also used the grep command to give us cleaner output. In that screenshot, our chains are currently figured to accept traffic.

More times than not, you’ll want your system to accept connections by default. Unless you’ve changed the policy chain rules previously, this setting should already be configured. Either way, here’s the command to accept connections by default:

## Connection-specific Responses
With your default chain policies configured, you can start adding rules to iptables so it knows what to do when it encounters a connection from or to a particular IP address or port. In this guide, we’re going to go over the three most basic and commonly used “responses”.

Accept – Allow the connection.

Drop – Drop the connection, act like it never happened. This is best if you don’t want the source to realize your system exists.

Reject – Don’t allow the connection, but send back an error. This is best if you don’t want a particular source to connect to your system, but you want them to know that your firewall blocked them.

The best way to show the difference between these three rules is to show what it looks like when a PC tries to ping a Linux machine with iptables configured for each one of these settings.

Allowing the connection:

![](https://www.howtogeek.com/wp-content/uploads/2013/12/4-accept.jpg?trim=1,1&bg-color=000&pad=1,1)

Dropping the connection:
![](https://www.howtogeek.com/wp-content/uploads/2013/12/5-drop.jpg?trim=1,1&bg-color=000&pad=1,1)

Rejecting the connection:
![](https://www.howtogeek.com/wp-content/uploads/2013/12/6-reject.jpg?trim=1,1&bg-color=000&pad=1,1)

## Connection States
As we mentioned earlier, a lot of protocols are going to require two-way communication. For example, if you want to allow SSH connections to your system, the input and output chains are going to need a rule added to them. But, what if you only want SSH coming into your system to be allowed? Won’t adding a rule to the output chain also allow outgoing SSH attempts?

That’s where connection states come in, which give you the capability you’d need to allow two way communication but only allow one way connections to be established. Take a look at this example, where SSH connections FROM 10.10.10.10 are permitted, but SSH connections TO 10.10.10.10 are not. However, the system is permitted to send back information over SSH as long as the session has already been established, which makes SSH communication possible between these two hosts.

![image](https://user-images.githubusercontent.com/89552767/155385833-6b36a57a-820f-47a4-8810-34755f13e681.png)


```
Thank you readers, and wait for next week blog
For Contact e-mail me at ramirez368@hotmail.com

```
