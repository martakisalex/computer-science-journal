# Domain Name System Scratch Pad

## [DNS Explained in 100 Seconds](https://youtu.be/UVR9lhUGAyU?si=K95Jo_bQDbQAk_FU)

It is like the phone book of the internet.

<img src="https://moz-static.moz.com/learn/seo/Domains-page/_large/domain-description-image.png?mtime=20170320080539" height="100">

It links human readable urls/host names to the unique ip address of a server that hosts that site.

When you type a url into the browser, it makes a DNS query to figure out which unique ip address is associated with that hostname.

However, the browser will first check the browser or local operating system cache. If the cache is empty, the browser must then use the "phone book". The job of this server is known as a DNS Recursive Resolver.

It is recursive because it needs to make calls to multiple servers starting with the root name server.

The Root Name Servers store the IP addresses of the Top Level Domain (TLD) Nameservers.

The TLD Nameservers store the IP addresses of the authoritative Nameservers for all the domains under them.