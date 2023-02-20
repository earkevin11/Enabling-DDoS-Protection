# Enabling-DDoS-Protection

# Differences between DDoS and DoS
- Distributed Denial of Service (DDoS) is if the attack comes from many networks and systems.
- Denial of Service (DoS) is if the attack comes from one location.


# What are Botnets?
- Botnets are collections of internet-connected systems that an individual controls. Attackers often times will use them without their owners’ knowledge. 
- Botnet owners use them to perform various actions like spamming, DDoS.
- In the past, Botnets were made of up compromised computers. Now they are made of IoT devices.

# What are the goal of DDoS?
- The malicious hacker’s goal is to overwhelm system resources on targeted servers making the system inaccessible.



# Best Practices for building DDoS resilient services in Azure

# Best Practice 1: Understand Application Architecture
- Solution: Ensure that security is a priority throughout the entire lifecycle of an application, from design and implementation to deployment and operations. Applications might have bugs that allow a relatively low volume of requests to use a lot of resources, resulting in a service outage.
- Solution below:
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/220011367-92666de6-d056-469a-8dbd-97792611b658.png" height="100%" width="100%" alt="SPF"/>
  
<p/>

# Best Practice 2: Eliminate single point of failure (SPF)
- Solution: Design your application handle increased loads by provisioning multiple instances makeing your system more resilient and more scalable.
- - 1. For Azure App Service, select an App Service plan that offers multiple instances.
- - 2. For Azure Cloud Services, configure each of your roles to use multiple instances.
- - 3. For Azure Virtual Machines, ensure that your VM architecture includes more than one VM and that each VM is included in an availability set. We recommend using virtual machine scale sets for autoscaling capabilities.

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/220010998-dcc25857-e496-4608-b634-8be86b0ed344.png" height="100%" width="100%" alt="SPF"/>
  
<p/>


# Best Practice 3: Implement defense in depth and layer security defenses in an application to reduce the chance of a successful attack
- Solution: Reduce the surface area by using IP allowlists to close down the exposed IP address space and listening ports that aren’t needed on the load balancers (for Azure Load Balancer and Azure Application Gateway).
- Use Network Security Groups (NSGs) to reduce the attack surface. 
- You can use service tags and application security groups (ASGs) as a natural extension of an application’s structure to minimize complexity for creating security rules and configuring network security.
