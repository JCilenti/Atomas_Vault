
Using nmap
- `nmap -sV 10.129.49.105` will give you service versions and OS type
- use `nmap -sT <ip addr>` to scan only TCP ports

- `nmap -p- <ip addr>` scans all 65,535 ports
	- DO NOT EVER DO THIS ^^^ can take 18+ hours
- use `nmap -p- <ip addr> --min-rate 5000` instead, this will scan all ports and faster
- If it appears the IP you are scanning is blocking your ping probe, use `nmap -Pn <ip addr>` The `-Pn` allows you to Disable host discovery. Port scan only.
- 