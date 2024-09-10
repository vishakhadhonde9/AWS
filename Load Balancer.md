# Elastic Load Balancer-
- ELB automatically distributes incoming application traffic across multiple targets or servers.
- Traffic Distribution:
    - The primary role of a load balancer is to evenly distribute incoming traffic among multiple servers to ensure no single server becomes overwhelmed.
    - This helps maintain the performance and reliability of applications.
- Health Monitoring:
    - Load balancers regularly check the health of servers to ensure they can handle requests.
    - If a server is detected as unhealthy or down, the load balancer will stop sending traffic to it until it is back online.
- Scalability:
    - Load balancers support horizontal scaling by allowing the addition or removal of servers without disrupting the overall service.
    - This makes it easier to handle varying traffic loads.
### Target Group- 
- A target group is a set of resources(servers) that a load balancer routes traffic towards them.
- It’s a way to group resources together so that the load balancer can manage and distribute traffic efficiently among them.

# Types of Load Balancer-
#### 1] Application Load Balance(ALB)-
- ALB operates at 7th layer of OSI model.
- ALB suppoerts HTTP and HTTPs protocols for routing.

#### 2] Network Load Balancer(NLB)-
 -  NLB is a type of load balancer designed to handle high-throughput, low-latency network traffic.
 -  Operates at the transport layer (Layer 4) of the OSI model.
 -  Support TCP and UDP protocols for routing.

#### 3] Gateway Load Balancer-
- Operates at Layer 3 (Network Layer) and Layer 4 (Transport Layer) of the OSI model.
- Gateway Load Balancer helps you easily deploy, scale, and manage your third-party virtual appliances like firewall.
