![image](https://github.com/user-attachments/assets/565eac1c-a6ae-494e-b881-b5d988ecf8e9)

1. # **SYSADM1 – Capacity Management & Planning**

## **Part 1\. A Simulated Dataset for Capacity Planning Exercise**

**Scenario:** A mid-sized e-commerce website is expecting a significant surge in traffic due to an upcoming holiday sale.

![image](https://github.com/user-attachments/assets/9da63f68-a152-4101-852b-fabfe107d305)

### Projected Traffic Increase

* **Expected Peak Traffic:** 5x the normal peak traffic  
* **Peak Time:** 12:00 PM \- 3:00 PM on the sale day

  ### System Specifications
  
* **Server Count:** 5  
* **CPU Cores per Server:** 8  
* **RAM per Server:** 32GB  
* **Network Bandwidth per Server:** 1Gbps

  ### Additional Considerations

* **New Product Launch:** A highly anticipated product will be released during the sale.  
* **Marketing Campaign:** A major marketing campaign will be launched to promote the sale.  
* **Potential Cyber Threats:** Increased traffic can attract malicious actors.

Tasks:

1. **Review the provided server performance data and identify potential bottlenecks**

   The potential bottlenecks are the following:

   

A. **CPU Utilization Bottleneck**  
   

   According to the existing server configuration, CPU consumption rises noticeably at times of increased demand, suggesting that the servers' processing capacity is almost at its limit. This implies that complicated processes like processing user queries, handling database requests, and managing background functions concurrently under a large traffic surge may be beyond the capabilities of the CPU. Particularly during high-concurrency events like a flash sale, the servers may encounter throttling if the load increases dramatically, which could lead to slower request handling and even crashes.

     
B. **Memory Utilization Issue**  
   

   Potential inefficiencies in the system's management of memory-based operations, including caching or database query handling, are indicated by the rising memory usage during peak periods. This can indicate a lack of efficient caching techniques or poorly optimized queries. Memory saturation brought on by increased traffic may force the system to use disk-based storage, which is slower and might result in lag in user experience and delays in data retrieval.

     
C. **Network Bandwidth Limitations**  
   

   The servers appear to be getting close to their bandwidth capacity during periods of high demand, based on the present network activity. A spike in traffic would probably overload the network, leading to slower data transfer speeds and interrupted service, especially when activities like streaming product photos or videos are involved. Additionally, this might affect server-to-server communication, which could negatively impact the functionality of distributed systems like databases or APIs that are essential for transactions and real-time data updates.

     
D. **Response Time Degradation**   
   

   A combination of CPU, memory, and network resource congestion is shown in the increased response times during periods of high activity. This suggests that the system has trouble effectively managing multiple requests at once, most often as a result of queue backlogs or conflict over shared resources like databases. Response delays may get worse with a large spike in traffic, which could result in timeout errors, abandoned transactions, and a general decline in client satisfaction. This emphasizes that in order to lower latency, both capacity increase and system optimization are required.

2. **Brainstorm possible solutions to address the identified bottlenecks. Propose potential solutions considering hardware and software-based solutions.**

   Our solutions to address the identified problems are the following:

   

A. **Horizontal Scaling, Code Optimization, and Auto-Scaling (Solution for CPU Utilization Bottleneck)**  
   

   To spread the load over an additional set of resources, use horizontal scaling by adding extra servers. Optimize database queries and application code to lessen the processing load on each server. As traffic spikes, more resources will be dynamically allocated if auto-scaling based on CPU thresholds is enabled.  
     
   Justification: By distributing the workload across several servers, the burden on individual CPUs is lessened. Code optimization increases efficiency by ensuring that each operation consumes the least amount of processing power required. Auto-scaling guarantees sufficient resources during periods of high demand while avoiding overprovisioning during off-peak hours.

     
B. **Caching Mechanisms and Upgrading Server RAM (Solution for Memory Utilization Issue)**  
   

   Programs like Redis or Memcached can store frequently requested data in memory to optimize caching methods. Review and improve database queries as well to cut down on memory usage. Upgrade server RAM or use memory-efficient programming techniques for long-term scalability.  
     
   Justification: Caching speeds up response times and saves memory by reducing the need to frequently query the database. Optimized queries lower the amount of RAM needed to analyze data. Upgrading hardware guarantees that the system can manage heavy loads in extreme situations without depending on slower disk-based storage.

     
C. **Improving APIs and Enhancing Network Bandwidth (Solution for Network Bandwidth Limitations)**  
   

   Improve APIs to minimize payload size and compress data to reduce bandwidth requirements. Additionally, enhance the network bandwidth capacity to handle the projected peak load.  
     
   Justification: Optimized APIs and data compression reduce bandwidth usage. By expanding network bandwidth, the system can handle spikes in traffic without experiencing bottlenecks.

     
D. **Load Balancing, Asynchronous Processing, and Stress Testing (Solution for Response Time Degradation)**  
   

   A load balancer can prioritize important tasks during periods of high traffic and divide traffic evenly among servers. Utilize asynchronous processing for non-essential operations to free up resources for user requests in real time. Furthermore, conduct stress testing to find and address system bottlenecks prior to the sale.  
     
   Justification: By preventing any server from becoming overloaded, load balancing enhances response speeds in general. The system can prioritize urgent tasks while postponing less critical ones due to asynchronous processing. Stress testing finds and fixes weak points in the system in advance, preparing it to withstand anticipated demands.

3. **Discuss the pros and cons of each proposed solution by filling out the table below. **

| Proposed Solution | Pros | Cons | Cost | Complexity | Potential Impact on System Performance |
| ----- | ----- | ----- | ----- | ----- | ----- |
| Horizontal scaling, code optimization, and enabling auto-scaling  | Distributes load evenly across multiple servers. Prevents single server overload. Auto-scaling dynamically adjusts resources based on traffic. Improves system reliability and availability. | Requires additional servers, increasing operational costs. Auto-scaling needs cloud infrastructure and configuration. Code optimization requires development effort and time. | Horizontal scaling: Ranges from $100 \- $1000 per month depending on the cloud provider (AWS, Azure, Google Cloud) and the number of additional servers required. Code optimization: Typically $500 \- $5000 depending on the complexity of the code and developer rates. Auto-scaling: $200 \- $2000 per month depending on the cloud infrastructure's resources and scaling requirements | Moderate to High, as implementing auto-scaling and optimizing code can be technically complex. | This solution significantly improves system performance by reducing the risk of CPU bottlenecks, maintaining responsiveness even under high traffic, and ensuring high availability. |
| Implement caching, optimize database queries, and upgrade RAM  | Caching reduces memory usage by storing frequently accessed data. Optimized queries reduce memory needed for processing data. RAM upgrades provide more resources for handling traffic. | Caching requires setup, configuration, and maintenance. RAM upgrades are hardware-dependent and can be costly. Database query optimization requires expertise and time. | Database query optimization: $1000 \- $5000 for consulting or development work to optimize queries. RAM upgrades: For 32GB of RAM per server, $100 \- $500 per server. For 5 servers, this can range from $500 \- $2500 depending on server specs and hardware providers.  | Moderate for caching; High for RAM upgrades and database optimization. | This solution improves response times by reducing memory-related issues, ensuring smoother application performance, and enhancing user experience. |
| Compress data, optimize APIs, and upgrade bandwidth. | Data compression minimizes bandwidth usage. API optimization reduces data transfer, improving efficiency. Upgrading bandwidth supports higher traffic loads. | Compression and API optimization require development time. | Data compression: $500 \- $3000 in initial development and integration costs. API optimization: $500 \- $3000 for development time to optimize API calls. Bandwidth upgrade: For upgrading to 1Gbps or higher bandwidth, monthly costs could range from $1000 \- $5000 per month depending on the service provider and location. | Moderate for compression, High for API optimization.  | This solution greatly improves data transfer speeds, reduces latency, and ensures the system can handle increased traffic without network congestion. |
| Implement load balancing, use asynchronous processing, and conduct stress testing. | Load balancing distributes traffic evenly, avoiding server overload. Asynchronous processing frees up resources for real-time requests. Stress testing identifies system weaknesses before traffic peaks. | Load balancing requires configuration and monitoring. Asynchronous processing complicates code and system design. Stress testing requires dedicated resources, time, and tools.  | Load balancers: Cost: For a cloud-based load balancing service (e.g., AWS ELB), it can cost $20 \- $500 per month, depending on the traffic and resources. Asynchronous processing: Development and setup could cost between $1000 \- $5000 depending on the complexity and integration needs. Stress testing: For using tools like LoadRunner or JMeter, stress testing can range from $500 \- $2000 per month for cloud-based testing environments. | Moderate to High, depending on the configurations and the system's current architecture. | This solution enhances system resilience by reducing latency and ensuring smooth handling of concurrent user requests, leading to better performance under high traffic conditions. |

Grading Rubric:

| Criteria | Excellent | 10pts | Good | 7pts | Needs Improvement | 4pts |
| ----- | :---- | :---- | :---- |
| **Problem Identification**  | Accurately identifies the primary problem and provides a detailed explanation. | Identifies the main problem and provides a basic explanation. | Identifies a problem but lacks clarity or accuracy. |
| **Solution Proposal**  | Proposes multiple relevant solutions and provides detailed explanations, including potential drawbacks and benefits. | Proposes one or two relevant solutions but lacks detailed explanation. | Proposes a solution but lacks feasibility or relevance. |
| **Evaluation of Solutions**  | Provides a thorough evaluation of the proposed solutions, considering factors like cost, complexity, and potential impact. | Provides a basic evaluation of the proposed solutions, but lacks depth. | Does not evaluate the proposed solutions or provides a superficial evaluation. |
| Score: |  |  |      /30 |

