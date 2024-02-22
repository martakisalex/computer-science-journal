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