## Background:  ##

The United States Military Academy provides and manages a wireless network for its cadets and faculty. To provide this service and be permitted to do so, the DoD must be satisfied with the security of the network to support the continued provisioning of the WREN. To uphold this level of security, cadets, faculty, and other personnel using the WREN network must agree to the Acceptable Use Policy, a document that describes appropriate use within the network. A key task in defending a network against internal and external threats is identifying weaknesses, minimizing attack surfaces, limiting access by user needs, etc. After security measures are implemented, a series of monitoring devices and software can be used to monitor the network to detect and react to unusual traffic or undesired users. 

The greatest motivator for this project is to maintain a secure network outside of the security boundary within the Department of Defense Information Network (DoDIN). In the past, the United States Military Academy has used DoD regulated networks within this security boundary. While more than sufficient for DoD purposes, this network did not prove to be effective for cadets working towards a college degree. Enter the WREN network: an enterprise network at USMA, still within the DoDIN but outside of the internal security boundary. While much more usable for college work and research, the WREN sacrifices the security provided by the inner security boundary of most DoD networks, making it more susceptible to compromise and attack. This is the problem the Defensive Cyber Operations capstone team is attempting to solve.  

A successful implementation of this capstone will provide cadets, faculty, and authorized personnel at West Point a method to monitor the network they use every day. Those who use the DDS-M kit will be able to observe the WREN network traffic (with limitations) and make reports and/or send up questionable data relating to the network. Not only will these individuals feel more responsible for the security of a resource they require every day, but they will also learn the basics of network management. DDS-M users and those who actively monitor the network will learn to hold others accountable for their internet use and cyber footprint, as it directly affects the health of the WREN network. The finished product will include detailed documentation for setup and installations. It will be effective in returning the intended DDS-M user base with metadata pertaining to the network and allow them to report possibly malicious data if it is found on the network. The overall goal is to maintain security of the WREN network. Allowing more individuals at West Point to have this capability will educate users on proper network etiquette while extending their knowledge of the cyber domain. 

#### Deliverables:  #### 

1.  Hardware configurations that enable the DDS-M kit to effectively reach high traffic points on EECS NET for monitoring network data.  
    

2.  Software tools/configurations on the DDS-M kit laptop that provides network tracing and packet capturing capabilities. 
    

3.  Software tools on the DDS-M deployment laptop that presents network data (IPs, time/type of connection) gathered by the hardware in a manner that is easy to follow and categorize based on threat level to the network.  
    

4.  Scripts/Code on DDSM deployment laptop that creates a visible response to suspicious network traffic to notify the user. (Suspicious traffic will be defined more clearly once we are able to see what network traffic looks like) 
    

5.  An accurate and updated network diagram of EECSNET that we develop using a network mapping tool (nmap) to get a better understanding of the layout of the network.  
    

#### Constraints and Restriction on the Design:  ####

1.  DDS-M Kit hardware and software 
    

#### Principle of Operation: ####  

The final product is a method to view consolidated network traffic and packets to scan for any suspicious network usage such as accessing unauthorized sites with or without VPNs and information being discretely sent to IPs with malware. The user would access the toolkit using the deployment laptop after turning on all the hardware in the DDS-M toolkit and connecting it to the laptop. On the deployment laptop the user would sign in and access the user interface for Red Hat Enterprise to access the virtual machines and hardware of the DDS-M kit and ensure that the systems are turned on and working properly. Next, the user would access the SecurityOnion interface and access the command terminal to view both the inputs and outputs of the products. The inputs are the network traffic and packets that are being captured using software tools that are within SecurityOnion and outside of it. The outputs are the dashboards and parsed displays of texts that show what data is being tracked, how much data is coming through, who it is coming from, where it is going, and the types of protocols being used. Along with SecurityOnion, scripts and code that will be accessed on the terminal will also be used as the system between the inputs and outputs. 

#### User Interface:  ####

The user interface(s) for the DDS-M kit are operating systems built on the Linux platform. The first is Red Hat Enterprise, the OS for the deployment laptop that was provided to us as part of the kit. Red Hat Enterprise allows the user to connect directly to the hardware, view its status, and access virtual machines for the hardware in the DDS-M kit. The second user interface is SecurityOnion, also a Linux based OS. Within SecurityOnion the user has access to tools for monitoring the network traffic and health. These interfaces are mostly web based and in GUI form.  

#### Inputs: #### 

The inputs for our delivered product will be the network traffic and packets that are going in and out of EECS NET and devices on the network.  All the data that is related to the traffic that is flowing in the network are the inputs that our product takes in. The details of these inputs are: 

The amount of traffic that is flowing in messages between devices that are communicating either within the network or outside the network is to be taken in by the system. Specifically, the amount of bits or Bytes being used to quantify the amount of data in a message. 

The IP and MAC addresses of the devices involved in the back-and-forth messages. These are also inputs that will go into the system and eventually become an output for the user. 

The protocols used on all layers of the OSI model in the traffic between devices on the network. Factors such as whether a message used TCP or UDP and HTTP and DNS and other potential protocols are inputs that will be taken in by our system. 

The date and time that messages were made, encoding method, and data size of the messages themselves are all inputs that the system will take in. 

#### Outputs:  ####

The outputs for our delivered product will be organized network traffic and metadata in an easy to view format that allows the user to make a sound judgment as to whether the data contains possibly malicious content or not. Although many tools within our stated user interfaces provide the user with this ability, we would like all outputs to be in one place, making it easily accessible and viewable. The different outputs in our user interfaces are included below along with an explanation.  

First, the user will need to see source and destination IP and MAC addresses. IP addresses allow for pinpointing the device, initiating the connection and the device or service accepting that connection. An IP address can tell the user a lot about where and what the user could be doing on the network. It also allows the user to compare the discovered IP addresses against those commonly accessed from West Point or allowed through our DNS servers and firewall. If the IP addresses of either party are out of the ordinary, it could be malicious and therefore reported. MAC addresses are also necessary, as they provide the exact address for the machines or systems involved in the connection. MAC addresses allow the user to verify the legitimacy of the IP addresses used. IP addresses can also come from the hops the involved devices take to make the final connection. Intermediate addresses come from devices such as routers and DNS servers.  

Next is the time of the connection made and frequency. When did the parties involved begin the connection, end the connection, and what was the connection’s total length? Also, how often do the parties involved make this connection? These pieces of data will reveal such things as crypto mining or consistent use of unapproved sources (per AUP). If this is a consistent event on the network, researchers at West Point can dig deeper to discover exactly what is being shared across the network. Additional to the time of the connection is the type of the connection, such as ports and protocols used. This gives the user further insight into what was going on during the connection and whether it is done securely.  

A description of the data shared, such as encoding, and data size and format will be another key output for this project. This enables the user to see how the data was sent between involved parties and if the data is important, based on the encoding scheme. Data that is important, such as usernames and passwords would not be in plain text s compared to html data from a website. Age of the data is another key piece, allowing the user to determine of the data is relevant to the situation or if it is no longer worth exploring (due to older age). Overall, the description of the data in brief terms enables the user to make a call as to whether it should be reported for suspicious content.  

#### User Instructions:  ####

-   Turn on DDS-M Kit (Turn on every hardware component) 
    
-   Ensure Deployment laptop is connected to DDS-M kit. 
    
-   Sign into deployment laptop 
    
-   Open a web browser and access Red Hat Enterprise Site 
    
-   Sign in with provided credentials 
    

-   Look through the status of all virtual machines and hardware that appears and ensure that they are all turned on and working  
    
-   Open the SecurityOnion application and open the command terminal 
    
-   Begin network traffic and packet capturing on both SecurityOnion and the terminal (To be defined more clearly once we create the code/scripts and get SecurityOnion installed) 
    
-   Look for unique changes in either the overall traffic on the network or the traffic on a specific device 
    

#### Acceptance Tests: #### 

Dashboards provide necessary information in real-time: Running test, conducted throughout all other tests and maintained use of our network. Looking for information regarding network stress, unusual activity (protocols on incorrect ports, transmissions at unusual times), and external to internal packet transmissions.  

DDSM Layers 2 and 3 are connected physically and logically: Conduct a series of pings between the components of our network to determine that they have network connectivity. After physically connecting every component do a ping test. 

Network Tap is providing a stream of information of all packets sent over it (Placed at perimeter of the network to ensure all traffic passes through it): Viewed in the workstation, SNORT is used to filter this traffic down into discernable, relevant information that can be used to identify anomalous network behavior and transmissions. The inputs would be the network traffic that flows through the location of the network that we place the network tap in and we would expect to see different forms of packets but mostly DNS packets. 

External IPs cannot Spoof Internal IP addresses to bypass firewall: Set ACL to prevent incoming traffic from outside our network from IPs within our address space. Use one of our personal laptop to attempt to gain access to our network while spoofing an Internal IP address.