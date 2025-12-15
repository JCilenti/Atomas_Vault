#### NMAP Commands
- ```nmap -sC``` --> is used to obtain more detailed information
- ```nmap -sV``` --> used to fingerprint the services running on a system and provide their versions
- Adding the ```-p-``` parameter tells nmap to scan all 65,535 ports
- If you need to run nmap with a specific script, you can use the command format ```nmap --script <script name> -p<port> <host>``` 
- To get a banner with nmap, we can use ```nmap -sV --script=banner <target>```
- To do it with a specific port, like FTP, we can use ```nmap -sV --script=banner -p21 10.10.10.0/24```
- To scan SMB with nmap, we can use ```nmap --script smb-os-discovery.nse -p445 <ipaddress>``` 
- To enable OS detection, version detection, script scanning, and traceroute, use the command ```nmap -A -p445 <ipaddress>``` which enables version detection over SMB port 445
- 