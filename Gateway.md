* Is a network device/software that acts as bridge between two different networks, especially when they use different protocols
* Exit point for network traffic.

* Example
	* You open a browser and visit `www.google.com`. Here's what happens
		* Your computer sends the request
		* It passes through the default gateway (usually your router)
		* Gateway sends it to the internet
		* Google replies back --> gateway passes it back to your computer

* Common Types of Gateways

| Type            | What it does                                                          |
| --------------- | --------------------------------------------------------------------- |
| Default Gateway | Connects internal network to external (e.g. router in a home network) |
| Email Gateway   | Filters and routes email between networks<br>                         |
| VoIP Gateway    | Converts voice calls between telephone and IP networks                |
| Cloud Gateway   | Connects on-premise systems to cloud services (e.g. AWS, Azure)       |

* In IT Support Teams
	* Default gateway IP like `192.168.1.1` is what devices use to access the internet.
	* If users cant access the internet IT support often checks
		* Is the gateway reachable?
		* Is the gateway IP set correctly?
		* Is the router/firewall (acting as the gateway) functioning?

* Command to check gateway (windows)
	* `ipconfig`
* Look for
	* `Default Gateway . . . . . . . . . : 192.168.1.1`

