#PAMTraining
* IP Address = logical address= denoted towards a system
* 2 parts
	* net id
	* host id
* `192.188.0.0` - net id
* `192.168.0.1` - Wi-Fi router/gateway


* `192.168.0.255` - broadcast id 

* 2 methods to assign IP
	* static 
		* manually assign to a machine
	* dynamic 
		* automatically assign via DHCP to a machine for a time

* port number - `0 - 65535`

* `192.168.0.10:3389` - rdp
* `192.168.0.10:8082` - ACMO
* `192.168.0.10:8443` - APIs

* security
	* data
		* access rights
		* encryption -> base46, AES 256, DES, SHA-256
		* authorization -> ARCOSDB -- arcossqladmin
	* server/machine
		* firewalls
		* access rights 
		* security (asymmetric cryptography)
			* public key and private key
		* authorization
		* authentication / MFA / 2FA  -> OTP, SMS, Email OTP, Biometric, Access Cards
			* based on their provided data 
				* username and password
		* IDS (Intrusion Detection System) and IPS (Intrusion Prevention System)
			* detect attack 
			* prevent
		* Port
			* hide close

* windows 10
	* local admin
		* privileges
			* open registry
			* open cmd
			* open task manager
	* local user 
		* privileges
			* open chrome.exe  
		* `hardik.arekar` -> created local -> at machine

* AD 
	* Arcon Domain
		* `hardik.arekar`

* PAM - U16 Hotfix-2
	* Builds on zero trust privileged access security framework
	* Major Products
		* PAM (Privileged Access Management)
		* UBA -> EPM (Endpoint Privileged Access Management)
		* SCM (Security Compliance Management)

* PAM 
	* Single Sign On
	* Group On Boarding
		* Mapping
	* Password Vault
		* Manage authentication (username, password)
		* Encryption
			* data -> AES 256 -> Arcon Proprietary Encryption (SSL) -> db
			* data <- AES 256 <- Arcon Proprietary Encryption (SSL) <- db
			* done with the help of APIs (400+ well documented APIs)
		* Database
			* MS SQL 2014
				* **OLTP Daily**
				* ARCOSDB (Main Database) -> `.mdf` & `.ldf`
				* ARCOSRDPDB (Video Log Information) -> `.mdf` & `.ldf`
					* capture image -> binary format
					* logmanagerservice -> binary to image `.jpeg` / `.jpeg.e`
					* `.jpeg.` in sequence -> video
					* logarchivalservice -> convert `.jpeg` -> `.avi` / `.mp4`
				* **OLAP DW**
				* Dwh_Raw (Data Warehousing)
				* ReportingDB (Data Warehousing)
	* Smart Audit Trails
	* Virtual Grouping

