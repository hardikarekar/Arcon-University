#organizationsetup 
* Database server stores, manages and provides access to structured data.
* Applications connect to it to read, write or update information.
* Where it fits in a system (3 Tier Architecture)
```css
[Client (Browser)] → [Application Server] → [Database Server]
```
	* Client: Requests something
	* App server: Processes the logic
	* Database server: Stores and gives back the data (e.g. user info, orders, etc.)

* Key Responsibilities of a Database Server

| Function            | Description                                                                 |
| ------------------- | --------------------------------------------------------------------------- |
| Store Data          | Structured tables of information (e.g. users, products)                     |
| Process Queries     | Respond to SQL commands like `SELECT`, `INSERT`, `UPDATE`, `DELETE`         |
| Ensure Security     | User access control, encryption and data privacy                            |
| Manage Transactions | Handles operations that must succeed or fail together (e.g. bank transfers) |
| Backup and Recovery | Protects data in case of failure or corruption.                             |

* Popular database servers

| Server Software      | Description                                   |
| -------------------- | --------------------------------------------- |
| MySQL                | Open source, very popular for web apps        |
| PostgreSQL           | Advanced, open-source, enterprise-grade       |
| Microsoft SQL Server | Common in enterprise and Windows environments |
| Oracle DB            | Enterprise level, feature rich                |
| MongoDB              | NoSQL DB, good for document-style data        |

* IT Support Example
	* Scenario
		* A company's sales app cant show customer records.
	* You might check
		* Is the database server online?
		* Is the DB service (like MySQL) running?
		* Are connections from app server being blocked?
		* Are there errors in the logs?
		* Has the database crashed or become full?