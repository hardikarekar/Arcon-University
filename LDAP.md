#organizationsetup 
* Used to access and manage directory information.
* Used in IT systems to lookup, read and write data in a directory service.
* Acts like a bride between applications (like login screen) and the directory service (like AD).
* Common Uses
	* Login Authentication
		* When a user logs in LDAP checks if username and password are correct.
	* Search Users
		* Email apps or internal systems search LDAP to autofill user names.
	* Access Control
		* Systems check group membership to allow or deny access.

* LDAP structure like a tree
```markdown
Root
 └── dc=example,dc=com
     ├── ou=Users
     │    └── cn=John Doe
     └── ou=Computers
          └── cn=PC01
```
* dc
	* Domain component (like `example.com`)
* ou
	* Organizational Unit (like users or computers)
* cn
	* Common Name (like the username or device name)

* How LDAP works
* Step1: User enters his username and password
```plaintext
Username: hardik.arekar
password: ********
```
* Step2: Windows sends a request to the domain controller
```bash
LDAP Query → "Is there a user called hardik.arekar, and does this password match?"
```
	* LDAP request checks directory for
		* Username: cn=hardik.arekar
		* Matching password (via secure authentication)
		* Account status (is it locked, exoired, etc.)
* Step3: AD/LDAP responds
	* If credentials are correct LDAP says `Yes,allow login`
	* If not LDAP says `Invalid username or password`
* Step 4: IT Support troubleshoots

| Check                                       | Why                                         |
| ------------------------------------------- | ------------------------------------------- |
| Is the user account disabled or locked      | Too many failed logins can lock the account |
| Is the password expired                     | LDAP can show the `pwdLastSet` attribute    |
| Is `hardik` part of the correct group or OU | LDAP can show his group memberships         |
| Can you search the user in LDAP?            | To ensure `hardik` account still exists     |

Example LDAP Query (Using command line)
```bash
ldapsearch -x -b "dc=company,dc=com" "(sAMAccountName=hardik.arekar)"
```
* This fetches details like
	* Hardik's email
	* Group he belongs to 
	* Account status

