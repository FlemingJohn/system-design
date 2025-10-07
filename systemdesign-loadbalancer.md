# Traffic Tamer: Mastering Load Balancing

## Module 1: Introduction to Load Balancers

### 1.1 What is a Load Balancer?
- Definition, purpose, and role in distributed systems
- Motivation: scalability, high availability, fault tolerance

### 1.2 The Need for Load Balancing
- Handling increased traffic, preventing single points of failure
- Distributing workloads efficiently

### 1.3 Basic Concepts
- Upstream servers (backend servers), Virtual IP (VIP), Real IP (RIP)
- Client-Server interaction flow with a load balancer

## Module 2: Types of Load Balancers

### 2.1 Hardware vs. Software Load Balancers
- Pros and cons of each
- Examples: `F5 BIG-IP` (hardware), `HAProxy`, `NGINX` (software)

### 2.2 Layer 4 vs. Layer 7 Load Balancers
- L4 (Transport Layer): TCP/UDP based, faster, simpler
- L7 (Application Layer): HTTP/HTTPS based, content-aware routing, SSL termination, more complex
- Use cases and differences in functionality

### 2.3 Internal vs. External Load Balancers
- Use cases within a private network vs. public internet facing

## Module 3: Load Balancing Algorithms

### 3.1 Basic Algorithms
- Round Robin: Simple, sequential distribution
- Weighted Round Robin: Prioritizing servers based on capacity
- Least Connections: Directing traffic to the server with fewest active connections
- Weighted Least Connections: Combining weighting with least connections

### 3.2 Advanced Algorithms
- IP Hash: Client IP mapped to a specific server (session persistence)
- URL/Header Hash: Content-based routing
- Least Response Time: Directing traffic to the server with the quickest response
- Source IP Affinity (Sticky Sessions)

## Module 4: Key Features and Concepts

### 4.1 Health Checks
- How load balancers monitor backend server health (ping, TCP, HTTP)
- Passive vs. Active health checks
- Configuring thresholds and actions for unhealthy servers

### 4.2 Session Persistence (Sticky Sessions)
- Maintaining client-server affinity for a session
- Methods: Cookie-based, IP-hash, SSL session ID

### 4.3 SSL Termination/Offloading
- Decrypting SSL traffic at the load balancer to offload backend servers
- Re-encrypting (re-encryption) vs. plain HTTP to backend

### 4.4 Connection Draining
- Gracefully removing a server from the load balancer pool without dropping active connections

### 4.5 Rate Limiting and Throttling
- Protecting backend servers from excessive requests

### 4.6 Content-Based Routing
- Directing requests based on URL path, host header, or other HTTP attributes

## Module 5: Deployment Strategies and Architectures

### 5.1 Active-Passive (Failover) Configuration
- Primary and secondary load balancers
- Heartbeat and failover mechanisms

### 5.2 Active-Active Configuration
- Distributing load across multiple active load balancers

### 5.3 Standalone Deployment
- Single load balancer instance

### 5.4 High Availability for Load Balancers Themselves
- `VRRP`, `CARP`, `Keepalived`

## Module 6: Global Server Load Balancing (GSLB)

### 6.1 Introduction to GSLB
- Distributing traffic across geographically dispersed data centers

### 6.2 DNS-Based Load Balancing
- Using DNS records (A, CNAME) to direct traffic
- Limitations of DNS caching

### 6.3 Advanced GSLB Techniques
- Proximity-based routing, latency-based routing, capacity-based routing

## Module 7: Cloud Load Balancers

### 7.1 AWS Elastic Load Balancing (ELB)
- Application Load Balancer (`ALB`): L7 features, path/host-based routing
- Network Load Balancer (`NLB`): High performance, L4, static IP support
- Classic Load Balancer (`CLB`): Legacy, L4/L7

### 7.2 Azure Load Balancer and Application Gateway
- Azure Load Balancer: L4, internal/external
- Azure Application Gateway: L7, WAF, SSL termination

### 7.3 Google Cloud Load Balancing
- Global External HTTP(S) Load Balancing, Internal Load Balancing, Network Load Balancing

## Module 8: Monitoring, Troubleshooting, and Best Practices

### 8.1 Key Metrics to Monitor
- Connection rates, error rates, backend server health, latency
- CPU/memory usage of load balancer itself

### 8.2 Common Troubleshooting Scenarios
- Backend server issues, misconfigured health checks, session persistence problems

### 8.3 Security Considerations
- DDoS protection, WAF integration, secure configurations

### 8.4 Capacity Planning
- Estimating required load balancer capacity based on traffic predictions

## Module 9: Load Balancers in Modern Architectures

### 9.1 Microservices and API Gateways
- Load balancing within a microservices ecosystem
- Role of API Gateways as advanced L7 load balancers

### 9.2 Service Mesh (e.g., Istio, Linkerd)
- Sidecar proxies providing advanced traffic management, load balancing, and observability at the service level

### 9.3 Serverless Architectures
- How load balancing concepts apply to serverless functions and API Gateways