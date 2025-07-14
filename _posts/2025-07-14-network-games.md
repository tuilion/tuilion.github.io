---
layout: post
title: "Network games."
date: 2025-07-14
excerpt: "The other day I was reading about _piping_ on Unix with `|`, and while creating a new
`.md` file for this blog post, I used `cp 2025-07-13-academia-goodbye.md 2025-07-14-network-games.md | subl 2025-07-14-network-games.md` in my Mac terminal"
---
 
The other day I was reading about _piping_ on Unix with `|`, and while creating a new `.md` file for this blog post, I used `cp 2025-07-13-academia-goodbye.md 2025-07-14-network-games.md | subl 2025-07-14-network-games.md` in my Mac terminal. Anyway, I was feeling so smart until ChatGPT informed me that actually this was not necessary because "`cp` carries nothing". Basically `|` does nothing, except enabling me to write the command in one line. Well... you learn...

#### Network curiosities
While learning networking on TryHackMe a few days ago, I learned about ARP packets and network scanning, MAC addresses, and of course I was curious to see what devices are currently attached to my home network, so I did a quick `sudo arp-scan`. What I found out was interesting. First of all, I had several `Unknown` devices on my network, and secondly, some of the devices appeared and disappeared when I scanned the network multiple times. Below is the image which illustrates this behaviour.

<p align="center">
  <img src="/_posts/assets/2025-07-14-network-scan.png" alt="ARP scan results" width="600"/>
  <br>
  <em>ARP-scan showing connected devices on my LAN</em>
</p>

We can see that there are multiple unknown devices on my network. So... what? 😄 Next, I used `nslookup` to actually find the names of the devices, and _voila_ all the locally administered unknowns are actually Android phones!

<p align="center">
  <img src="/_posts/assets/2025-07-14-network-android-devices.png" alt="nslookup results" width="600"/>
  <br>
  <em>nslookup results showing the names of "unknown" devices</em>
</p>

#### Lessons learned

1. Android phones show up as `unknown` when using `arp-scan`.
2. Android phones connect and disconnect from the network - probably to conserve battery power.
3. Piping with `|` is sometimes redundant. 😂

#### Next steps
I will continue learning about networks,. I want to deepen my knowledge to be able to use it in real-life, especially at home. Also, I plan to build a **network-scanner** with Python that will be able to:
1. Scan my network every 30 seconds.
2. Log the scans into a .txt file.
3. Report if there are any unusual devices connected to the network.

This will be an exercise in Python, in networking, and in cybersecurity.

---

**Until next time, happy network scanning.**
