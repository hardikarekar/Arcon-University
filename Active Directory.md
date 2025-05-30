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

## Active Directory Setup
### Part1: Install Active Directory on Windows Server 2019
* Prerequisites
	* Windows server 2019 installed on VMware
	* Internet Connection 
	* A static IP address is recommended
* Step by Step: Install AD DS Role
	* Open Server Manager
	* Click Manage > Add Roles and Features
	* Click next until you reach "Server Roles"
	* Click Active Directory Domain Services
		* Popup will appear. Click Add features
	* Click next until you reach "Confirmation"
	* Click Install
	* Wait for installation to complete
		* Don't restart yet
### Part2: Promote the Server to Domain Controller
* Steps
	* In Server Manager, click the flag icon (top-right).
	* Click "Promote this server to domain controller"
	* Now choose your scenario
		* If it's your first domain
			* Select add "New Forest"
			* Type a root domain name (e.g. `hardik.local`)
	* Domain Controller Options
		* Choose Forest Functional Level
		* Check 
			* DNS server
			* Global Catalog (default)
		* Set a directory service restore mode (DSRM) password
	* Click next through the rest of the wizard and click Install at the end
	* The server will restart automatically after promotion.
### Part3: Logging in as Domain Admin
* After reboot
	* On login screen, click "Other User"
	* Login with the domain admin
		* Username: `Administrator`
		* Domain: `hardik.local`
### Part4: Using Active Directory Tools
* Open AD Management Consoles:
	* Go to Server Manager > Tools
		* Active Directory Users and Computers (ADUC)
		* DNS
		* Group Policy Management
		* AD Domains and Trusts
### Part5: Common Tasks
* Create a new user
	* Open Active Directory Users and Computers
	* Right Click on the Users container > New > User
	* Enter
		* First name, username (e.g. `nichiket`)
		* Set password
	* Click finish
* Joint a Client Machine to Domain
* Create Organizational Units
	* Open Active Directory Users and Computers (ADUC)
	* Right click your domain `hardik.local` > New > Organizational Unit
	* Create the following OUs
		* `IT`
		* `HR`
		* `Finance`
	* Check "Protect Container from accidental deletion"
	* Create User inside OU
		* Expand the OU eg `IT` > Right click > New > User
		* Example
			* First Name: `pratik`
			* User Logon Name: `pratik.tare`
			* Password
		* Create at least 2 users per OU