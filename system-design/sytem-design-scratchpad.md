# System Design Scratchpad

## Forward

The questions require the interviewees to design an architecture for a software system, which could be a news feed, Google search, chat system, etc. 

These questions are intimidating, and there is no certain pattern to follow.

An interviewee is evaluated based on how she analyzes a vague problem and how she solves the problem step by step.

The system design questions are open-ended. Just like in the real world, there are many differences and variations in the system. The desired outcome is to come up with an architecture to achieve system design goals. 

## CHAPTER 1: SCALE FROM ZERO TO MILLIONS OF USERS

### Single server setup

1. Users access websites through domain names, such as api.mysite.com. Usually, the Domain Name System (DNS) is a paid service provided by 3rd parties and not hosted by our servers.
2. Internet Protocol (IP) address is returned to the browser or mobile app. In the example, IP address 15.125.23.214 is returned.
3. Once the IP address is obtained, Hypertext Transfer Protocol (HTTP) requests are sent directly to your web server.
4. The web server returns HTML pages or JSON response for rendering.

The traffic to your web server comes from two sources: web application and mobile application.

- Web application: it uses a combination of server-side languages (Java, Python, etc.) to handle business logic, storage, etc., and client-side languages (HTML and JavaScript) for presentation.
- Mobile application: HTTP protocol is the communication protocol between the mobile app and the web server. JavaScript Object Notation (JSON) is commonly used API response format to transfer data due to its simplicity.

### Database

With the growth of the user base, one server is not enough, and we need multiple servers: one for web/mobile traffic, the other for the database. Separating web/mobile traffic (web tier) and database (data tier) servers allows them to be scaled independently.

Relational databases are also called a relational database management system (RDBMS) or SQL database.

Non-Relational databases are also called NoSQL databases.

These databases are grouped into four categories: key-value stores, graph stores, column stores, and document stores. Join operations are generally not supported in non-relational databases.

Non-relational databases might be the right choice if:
- Your application requires super-low latency.
- Your data are unstructured, or you do not have any relational data.
- You only need to serialize and deserialize data (JSON, XML, YAML, etc.). • You need to store a massive amount of data.

### Vertical Scaling vs Horizontal Scaling

**Vertical scaling**, referred to as “scale up”, means the process of adding more power (CPU, RAM, etc.) to your servers.

**Horizontal scaling**, referred to as “scale-out”, allows you to scale by adding more servers into your pool of resources. Horizontal scaling is more desirable for large scale applications due to the limitations of vertical scaling.

### Load Balancer

A load balancer evenly distributes incoming traffic among web servers that are defined in a load-balanced set.

The load balancer communicates with web servers through private IPs.

If a load balancer and a second web server are added, one successfully solves no failover issue and improved the availability of the web tier.
- If server 1 goes offline, all the traffic will be routed to server 2. This prevents the website from going offline. We will also add a new healthy web server to the server pool to balance the load.
- If the website traffic grows rapidly, and two servers are not enough to handle the traffic, the load balancer can handle this problem gracefully. You only need to add more servers to the web server pool, and the load balancer automatically starts to send requests to them.

### Database Replication

Database replication can be used in many database management systems, usually with a master/slave relationship between the original (master) and the copies (slaves).

A master database generally only supports write operations. A slave database gets copies of the data from the master database and only supports read operations.

All the data-modifying commands like insert, delete, or update must be sent to the master database.

*Most applications require a much higher ratio of reads to writes; thus, the number of slave databases in a system is usually larger than the number of master databases.*

What if one of the databases goes offline?
- If only one slave database is available and it goes offline, read operations will be directed to the master database temporarily.
- If the master database goes offline, a slave database will be promoted to be the new master.

### Cache

A cache is a temporary storage area that stores the result of expensive responses or frequently accessed data in memory so that subsequent requests are served more quickly.

#### Cache Tier

The cache tier is a temporary data store layer, much faster than the database.

After receiving a request, a web server first checks if the cache has the available response. If it has, it sends data back to the client. If not, it queries the database, stores the response in cache, and sends it back to the client. This caching strategy is called a **read-through cache**.

#### Considerations for using cache

Here are a few considerations for using a cache system:
- Decide when to use cache. Consider using cache when data is read frequently but modified infrequently.
- Expiration policy. It is a good practice to implement an expiration policy. Once cached data is expired, it is removed from the cache.
- Consistency: This involves keeping the data store and the cache in sync. Inconsistency can happen because data-modifying operations on the data store and cache are not in a single transaction.
- Mitigating failures: A single cache server represents a potential single point of failure (SPOF).
- Eviction Policy: Once the cache is full, any requests to add items to the cache might cause existing items to be removed. This is called cache eviction.

### Content Delivery Network (CDN)

A CDN is a network of geographically dispersed servers used to deliver static content. CDN servers cache static content like images, videos, CSS, JavaScript files, etc.

Here is how CDN works at the high-level: when a user visits a website, a CDN server closest to the user will deliver static content. Intuitively, the further users are from CDN servers, the slower the website loads.

#### Considerations of using a CDN

- Cost: CDNs are run by third-party providers, and you are charged for data transfers in and out of the CDN.
- Setting an appropriate cache expiry: For time-sensitive content, setting a cache expiry time is important.
- CDN fallback: You should consider how your website/application copes with CDN failure.

### Stateless Web Tier

Now it is time to consider scaling the web tier horizontally. For this, we need to move state (for instance user session data) out of the web tier. A good practice is to store session data in the persistent storage such as relational database or NoSQL. Each web server in the cluster can access state data from databases. This is called stateless web tier.

### Stateful Architecture

 A stateful server remembers client data (state) from one request to the next.

 