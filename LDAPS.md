#organizationsetup 
* Stands for LDAP Secure
* Secured, encrypted version of LDAP.
* Port: `636`

* How LDAPS works
	*  Client connects to LDAP server
	* Instead of sending info as plaintext, connection is encrypted using SSL/TLS.
	* Credentials, group info and directory queries are exchanged safely.

* Why use LDAPS?
	* To protect sensitive data, especially login credentials.
	* Required for compliance.
	* Prevents man-in-middle attacks during authentication.

* IT Support Example Using LDAPS
	* A company has enabled LDAPS for security. Now, an internal HR app is unable to authenticate users
		* What IT support might check
			* Is the app trying to connect to port `636`?
			* Does the LDAP server have a valid SSL certificate?
			* Is the app configured to trust the certificate authority (CA)?
			* `openssl s_client -connect ldap.company.com:636`
				* This checks if LDAP is working correctly.