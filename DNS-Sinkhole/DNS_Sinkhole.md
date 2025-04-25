# DNS Sinkhole

Created by: Shadi A
Created time: April 25, 2025 5:29 PM
Category: Networking

# What is a DNS Sinkhole?

In simple terms a DNS Sinkhole is a way of blocking traffic coming from a specific domain.

# How does it work?

A DNS sinkhole functions as the DNS server for your network. When a device attempts to access a domain (like [https://www.google.com](https://www.google.com/search?q=google.com)), it sends a DNS query to the sinkhole. The sinkhole then checks if the requested domain name is on its blacklist. If it is, instead of providing the actual IP address of the target server, the sinkhole might return a non-routable IP address or just refuse to resolve the domain. This prevents your network from connecting to the blacklisted domain.

# How does it block ads?

When you access a webpage, the page often pulls ads from separate servers (different domains). Your browser makes DNS requests to retrieve the IP addresses of these servers. A DNS sinkhole intercepts these DNS queries. If the domain name of an ad server is on the sinkhole's blacklist, it will block the DNS resolution, preventing your browser from connecting to that ad server, blocking the ads from loading. The sinkhole identifies these ad domains based on a blocklists, that is regularly update.

# Implement it

If you're looking for a free solution, I recommend Pi-Hole. It's an open source DNS Sinkhole solution with plenty of documentation online, meaning you won't have much trouble setting it up. It also serves as a great project to get a better grasp of DNS systems and how they work.
