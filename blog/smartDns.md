# SmartDNS: SmartDNS setup in NPCI.

In the fast-evolving realm of financial technology, maintaining a robust and reliable infrastructure is paramount. At the National Payments Corporation of India (NPCI), where we operate a private datacenter housing thousands of virtual machines (VMs), the imperative for seamless interaction with banks has led to the development of an innovative solution - SmartDNS.

![DNS](https://cf-assets.www.cloudflare.com/slt3lc6tev37/5exJlPlwAT2kQCITQhrIi9/1f771294e218b64c0490e83968075766/what_is_dns.png)

## **The Challenge: Ensuring Uninterrupted Connectivity with Banks**

In the direct interface with banks, providing a consistent and reliable IP address is critical. Swift restoration in the event of downtime is imperative. To tackle this challenge, we conceived and implemented SmartDNS, a dynamic DNS solution designed for load balancing and automated IP assignment based on hostnames.

## **Technologies at the Core:**

### **PowerDNS:**
PowerDNS, a leading provider of secure open-source and commercial DNS software, stands at the core of our SmartDNS solution. Tailored for large-scale DNS service providers, PowerDNS ensures an exceptional user experience, provides DDoS protection, and delivers efficient internet performance for Hosters and ISPs.

### **MariaDB:**
To store DNS entries and ensure high availability through replication, we turned to MariaDB Server. As one of the most popular open-source relational databases, MariaDB is renowned for its performance, reliability, and unwavering commitment to open source principles.

### **Docker:**
Our SmartDNS implementation embraces a container-based setup using Docker, providing flexibility, scalability, and streamlined management for our dynamic DNS infrastructure.

### **PowerDNS DNSdist:**
DNSdist, a unique DNS proxy and load balancer, optimizes DNS traffic in front of the PowerDNS Recursor. Deployed alongside PowerDNS Recursor, it delivers unparalleled performance and features for our DNS services.

### **PowerDNS Recursor:**
As a highly efficient, low-latency DNS caching server, PowerDNS Recursor ensures rapid responses to DNS requests. Focused on faster, safer, and more secure internet performance, it plays a pivotal role in enhancing user experience.

### **PowerDNS-Admin:**
To streamline interactions with PowerDNS, we integrated PowerDNS-Admin as a user interface. Leveraging the PowerDNS API, PowerDNS-Admin offers an intuitive and reliable platform for managing DNS operations seamlessly.

### **SmartDNS Architecture:**
We have the master slave architecture where master is the one for the new DNS entry and slave act as DNS to resolve the hostname.
![smartDNS Architecture](../static/img/dnsArch.png)