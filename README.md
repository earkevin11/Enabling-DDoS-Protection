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

# Best Practice 1
-

# Best Practice 2: Eliminate single point of failure 
- Solution: Design your application handle increased loads by provisioning multiple instances makeing your system more resilient and more scalable.
- - 1. For Azure App Service, select an App Service plan that offers multiple instances.
- - 2. For Azure Cloud Services, configure each of your roles to use multiple instances.
- - 3. For Azure Virtual Machines, ensure that your VM architecture includes more than one VM and that each VM is included in an availability set. We recommend using virtual machine scale sets for autoscaling capabilities.
