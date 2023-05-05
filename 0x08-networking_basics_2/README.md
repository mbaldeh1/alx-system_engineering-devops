                        0x08. Networking basics #1
-------------------------------------------------------------------------------

0. Change your home IP


Log in to your router's settings page using your web browser and administrator login credentials.
Look for an option to change the WAN (Wide Area Network) IP address. This may be located under the "Internet" or "Network" settings.
Choose a new IP address that is within the range of your ISP's allocated IP addresses.
Save your changes and restart your router for the new IP address to take effect.
Please note that changing your home IP address may not always be possible or advisable, and it could also affect any devices or services that rely on a static IP address. Additionally, if you are looking to change your IP address for privacy or security reasons, using a Virtual Private Network (VPN) may be a better solution.


1. Show attached IPs


The exact steps to view attached IPs may vary depending on your router's make and model, but the process generally involves the following steps:

Open a web browser and enter your router's IP address into the address bar. This should be listed in the documentation provided with your router or on a label attached to the router itself.

Log in to the router's settings page using the administrator username and password. Again, these credentials should be listed in the documentation or on the router.

Navigate to the "Connected Devices" or "Device List" section. This may be located under the "Status" or "Network" section, depending on your router.

Look for a list of devices connected to your network. Each device should be listed along with its IP address, MAC address, and hostname.

Please note that the specific steps and options for viewing attached IPs may differ depending on your router's firmware and user interface.


2. Port listening on localhost



To check for open ports listening on localhost, you can use the command prompt or terminal and enter the following command:

netstat -an | grep LISTEN | grep :<port_number>



Replace <port_number> with the port number you want to check. This command will display a list of all open ports on your system, and the "grep" command will filter the output to show only the ports that are listening for incoming connections.

For example, if you want to check if port 8080 is open on localhost, you can run the following command:

netstat -an | grep LISTEN | grep :8080


If there is a process listening on that port, you should see an output line with the local address set to "localhost" or "127.0.0.1".

Alternatively, you can use a graphical tool to check for open ports on your system, such as "lsof" or "nmap". These tools may provide more detailed information about the processes using the open ports.
