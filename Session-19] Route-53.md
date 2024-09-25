# Route 53-
- Route 53 provides highly available and scalable Domain Name System (DNS), domain name registration, and health-checking cloud services.
- The Domain Name System (DNS) is the phonebook of the Internet.
- Humans access information online through domain names, like facebook.com or espn.com. Web browsers interact through Internet Protocol (IP) addresses.
- DNS translates domain names to IP addresses so browsers can load Internet resources.

# Domain Name System-
- **Domain Name:** A domain name is the human-readable address used to access websites on the internet. It translates to an IP address that computers use to identify each other.
- Key Components of a Domain Name:
  - **Second-Level Domain (SLD):** The part of the domain name that comes before the top-level     domain (TLD). In "example.com," "example" is the SLD.
  - **Top-Level Domain (TLD):** The suffix that follows the SLD, such as ".com," ".org," or ".net." There are also country-code TLDs (like ".uk" for the United Kingdom).
  - **Subdomain:** An optional prefix added to a domain name, such as "blog.example.com." This can help organize different sections of a website.


# Working-

![image](https://github.com/user-attachments/assets/cd551155-e835-4993-98c6-e96b4dd1c956)

- Step 1: User Request
  - Entering a Domain Name: When you type a web address (like www.example.com) into your browser   and hit enter, your computer needs to find out the corresponding IP address to connect to that website.
- Step 2: DNS Resolver Query
  - Query the DNS Resolver: Your device sends a request to a DNS resolver, typically provided by your Internet Service Provider (ISP) or a public DNS service (like Google DNS).
- Step 3: Check Cache
  - Cache Check: The DNS resolver first checks its cache to see if it has the IP address for that domain stored.
  - If it finds it, it returns the IP address immediately, and the process ends here.
- Step 4: Recursive Query (If Not Cached)
  - Root Server Query: If the IP address is not cached, the resolver sends a query to a root DNS server.
  - The root server doesn’t know the specific IP address but can direct the resolver to the appropriate TLD (Top-Level Domain) server (like .com or .org).
- Step 5: TLD Server Query
  - TLD Server Query: The resolver then queries the TLD server based on the domain’s extension. The TLD server responds with the address of the authoritative DNS server for the specific domain.
- Step 6: Authoritative Server Query
  - Authoritative Server Query: The resolver sends a query to the authoritative DNS server.
  - This server contains the actual DNS records for the domain, including the IP address.
- Step 7: Return the IP Address
  - IP Address Response: The authoritative server responds with the IP address of the requested domain (for example, 192.0.2.1).
- Step 8: Return to User
  - Send Back to User: The resolver sends the IP address back to your device.
- Step 9: Connect to the Website
  - Connect to the Server: With the IP address, your device can now establish a connection to the website's server and load the webpage.
 
# Routing Policy-
- **Simple routing policy –** Use for a single resource that performs a given function for your domain, for example, a web server that serves content for the example.com website. You can use simple routing to create records in a private hosted zone.

- **Failover routing policy –** Use when you want to configure active-passive failover. You can use failover routing to create records in a private hosted zone.

- **Geolocation routing policy –** Use when you want to route traffic based on the location of your users. You can use geolocation routing to create records in a private hosted zone.

- **Geoproximity routing policy –** Use when you want to route traffic based on the location of your resources and, optionally, shift traffic from resources in one location to resources in another location. You can use geoproximity routing to create records in a private hosted zone.

- **Latency routing policy –** Use when you have resources in multiple AWS Regions and you want to route traffic to the Region that provides the best latency. You can use latency routing to create records in a private hosted zone.

- **IP-based routing policy –** Use when you want to route traffic based on the location of your users, and have the IP addresses that the traffic originates from.

- **Multivalue answer routing policy –** Use when you want Route 53 to respond to DNS queries with up to eight healthy records selected at random. You can use multivalue answer routing to create records in a private hosted zone.

- **Weighted routing policy –** Use to route traffic to multiple resources in proportions that you specify. You can use weighted routing to create records in a private hosted zone.
