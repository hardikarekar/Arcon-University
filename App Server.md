* Application Server hosts and runs apps --> processes business logic, connects to databases, sends the result to the user.

* Typical role in a 3 tier architecture
```css
[Client (Browser/App)] → [Application Server] → [Database Server]
```
	* Client Tier: UI (e.g. browser/mobile app)
	* Application Tier: Business Logic (app server)
	* Database Tier: Stores data (DB server)

* Responsibilities of an Application Server

| Task               | Example                                       |
| ------------------ | --------------------------------------------- |
| Run business logic | Validating login, processing transactions     |
| Manage connections | Talking to databases, APIs and other services |
| Handle Sessions    | Remembering user login, tracking actions      |
| Load Balancing     | Distribute requests across multiple servers   |
| Security           | Authentication, encryption, access control    |

* Examples of Application Server

| Platform       | Description                             |
| -------------- | --------------------------------------- |
| Apache Tomcat  | For Java based apps                     |
| Microsoft IIS  | Can host ASP.NET apps                   |
| JBoss/WildFly  | Enterprise Java EE apps                 |
| Node.js Server | JavaScript runtime acting as app server |
| GlassFish      | Another Java EE server                  |

* App Server vs Web Server

| Feature | Web Server                         | App Server                                      |
| ------- | ---------------------------------- | ----------------------------------------------- |
| Purpose | Servers static context (HTML, CSS) | Runs dynamic apps (processes code, talks to DB) |
| Example | Apache HTTP Server                 | Tomcat, JBoss, Node.js                          |
| Content | Static                             | Dynamic                                         |
