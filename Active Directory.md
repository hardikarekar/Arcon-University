#organizationsetup
* Directory service developed by Microsoft for Windows Domain Networks.
* Used to manage and organize IT resources e.g. users, computers, printers and more in a centralized and secure way.

* What AD does
	* Authentication and Authorization
		* Verifies who a user is (Authentication)
		* Determines what a user is allowed to access (Authorization)
	* Centralized Management
		* Admins can manage all computers, users and policies from one place.
	* Group Policy
		* Used to enforce rules like password policies, software restrictions and desktop configurations on multiple computers at once.
	* Security
		* AD allows for role based access control using permissions and group memberships.

* Key Components

| Component                   | Description                                                              |
| --------------------------- | ------------------------------------------------------------------------ |
| Domain                      | Group of objects (users, computers) sharing same database.               |
| Domain Controller (DC)      | Server that runs AD services and manages domain.                         |
| Organizational Units (OU)   | Container to group objects for easier management and policy application. |
| Users & Groups              | Individuals or collection of users given access to resources.            |
| Group Policy Objects (GPOs) | Set of rules applied to users and computers.                             |

* Tech used with AD
	* LDAP
		* Lightweight directory access protocol
		* Used to interact with AD.
	* Kerberos
		* Authentication protocol used by AD
	* DNS
		* Crucial for locating services with AD