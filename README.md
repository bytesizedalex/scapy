# Docker Container for Scapy

This Docker container build is based on [Alpine Linux](https://alpinelinux.org/) and runs Scapy

# What is Alpine Linux?

*
Alpine Linux is an independent, non-commercial, general purpose Linux distribution designed for power users who appreciate security, simplicity and resource efficiency.

*SMALL
Alpine Linux is built around musl libc and busybox. This makes it smaller and more resource efficient than traditional GNU/Linux distributions. A container requires no more than 8 MB and a minimal installation to disk requires around 130 MB of storage. Not only do you get a fully-fledged Linux environment but a large selection of packages from the repository.

*Binary packages are thinned out and split, giving you even more control over what you install, which in turn keeps your environment as small and efficient as possible.

*SIMPLE
Alpine Linux is a very simple distribution that will try to stay out of your way. It uses its own package manager called apk, the OpenRC init system, script driven set-ups and that’s it! This provides you with a simple, crystal-clear Linux environment without all the noise. You can then add on top of that just the packages you need for your project, so whether it’s building a home PVR, or an iSCSI storage controller, a wafer-thin mail server container, or a rock-solid embedded switch, nothing else will get in the way.

*SECURE
Alpine Linux was designed with security in mind. The kernel is patched with an unofficial port of grsecurity/PaX, and all userland binaries are compiled as Position Independent Executables (PIE) with stack smashing protection. These proactive security features prevent exploitation of entire classes of zero-day and other vulnerabilities.
*
# What is Scapy?

*Scapy is a powerful interactive packet manipulation program. It is able to forge or decode packets of a wide number of protocols, send them on the wire, capture them, match requests and replies, and much more. It can easily handle most classical tasks like scanning, tracerouting, probing, unit tests, attacks or network discovery (it can replace hping, 85% of nmap, arpspoof, arp-sk, arping, tcpdump, tethereal, p0f, etc.). It also performs very well at a lot of other specific tasks that most other tools can't handle, like sending invalid frames, injecting your own 802.11 frames, combining technics (VLAN hopping+ARP cache poisoning, VOIP decoding on WEP encrypted channel, ...), etc. See interactive tutorial and the quick demo: an interactive session (some examples may be outdated).
What makes scapy different from most other networking tools

*First, with most other tools, you won't build someting the author did not imagine. These tools have been built for a specific goal and can't deviate much from it. For example, an ARP cache poisoning program won't let you use double 802.1q encapsulation. Or try to find a program that can send, say, an ICMP packet with padding (I said padding, not payload, see?). In fact, each time you have a new need, you have to build a new tool.
Second, they usually confuse decoding and interpreting. Machines are good at decoding and can help human beings with that. Interpretation is reserved to human beings. Some programs try to mimic this behaviour. For instance they say "this port is open" instead of "I received a SYN-ACK". Sometimes they are right. Sometimes not. It's easier for beginners, but when you know what you're doing, you keep on trying to deduce what really happened from the program's interpretation to make your own, which is hard because you lost a big amount of information. And you often end up using tcpdump -xX to decode and interpret what the tool missed.

*Third, even programs which only decode do not give you all the information they received. The network's vision they give you is the one their author thought was sufficient. But it is not complete, and you have a bias. For instance, do you know a tool that reports the padding ?

*Scapy tries to overcome those problems. It enables you to build exactly the packets you want. Even if I think stacking a 802.1q layer on top of TCP has no sense, it may have some for somebody else working on some product I don't know. Scapy has a flexible model that tries to avoid such arbitrary limits. You're free to put any value you want in any field you want, and stack them like you want. You're an adult after all.

*In fact, it's like building a new tool each time, but instead of dealing with a hundred line C program, you only write 2 lines of Scapy.

*After a probe (scan, traceroute, etc.) Scapy always gives you the full decoded packets from the probe, before any interpretation. That means that you can probe once and interpret many times, ask for a traceroute and look at the padding for instance.*
