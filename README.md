# NETWORKWALKS-B083-WK1-PM1-CYBERSECURITY-LAB-SETUP
Week 1 Cybersecurity Lab Environment Setup using VirtualBox and Kali Linux.



📌 Project Overview

This project focuses on setting up an isolated cybersecurity lab environment using Oracle VirtualBox and Kali Linux. The purpose of the lab is to create a safe and controlled environment for learning and practicing cybersecurity concepts, network security, and penetration testing techniques without affecting the host system or external networks.

The project documents the complete lab setup process, including virtual machine configuration, network configuration, Kali Linux installation, connectivity verification, and security considerations. Screenshots are included to provide evidence of each major setup step.

This Week 1 project establishes the foundation for further hands-on cybersecurity and ethical hacking activities in a controlled virtual environment.



🎯 Objectives

The main objectives of this project are:

1. Set up a virtual cybersecurity lab using Oracle VirtualBox.


2. Install and configure Kali Linux as the primary cybersecurity testing environment.


3. Configure the virtual network to enable safe and controlled communication within the lab.


4. Verify network connectivity and ensure the virtual environment is functioning correctly.


5. Understand basic virtualization and networking concepts used in cybersecurity labs.


6. Create a safe, isolated environment for future ethical hacking and penetration-testing exercises.


7. Document the complete setup process with screenshots and step-by-step explanations for future reference.

   


🛡️ Purpose of the Lab

The purpose of this lab is to create a safe, isolated, and controlled environment for cybersecurity learning and practical experimentation. Using Oracle VirtualBox and Kali Linux, the lab provides a platform to understand and practice cybersecurity concepts without directly affecting the host operating system or real-world systems.

The lab will be used to:

Practice network security and cybersecurity concepts.

Learn and explore Kali Linux security tools.

Understand virtual machines and network configurations.

Perform authorized security testing and penetration-testing exercises.

Develop practical, hands-on cybersecurity skills in an ethical and controlled environment.

Prepare the environment for future cybersecurity projects and labs.



🏗️ Lab Architecture
The cybersecurity lab is designed using Oracle VirtualBox to create an isolated virtual environment. Kali Linux runs as a virtual machine inside VirtualBox and is used as the primary cybersecurity testing and learning platform.
Architecture
                    HOST COMPUTER
                         │
                         │
                  Oracle VirtualBox
                         │
                         │
                  ┌──────▼──────┐
                  │  Kali Linux │
                  │ Virtual      │
                  │ Machine      │
                  └──────┬──────┘
                         │
                  Virtual Network
                         │
                  ┌──────▼──────┐
                  │  Controlled  │
                  │   Network    │
                  │ Environment  │
                  └──────────────┘
Components
Host Machine: Physical computer running the virtualization software.
Oracle VirtualBox: Used to create and manage the virtual cybersecurity lab.
Kali Linux VM: Provides cybersecurity and penetration-testing tools for authorized practice.
Virtual Network: Provides controlled network connectivity for communication and testing within the lab.
Isolation: The virtual environment helps keep testing activities separate from the host system and unauthorized external systems.
This architecture provides a controlled and safe foundation for future cybersecurity exercises.



Lab Configuration
| 🧩 Component | ⚙️ Configuration |
|---|---|
| 💻 Host OS | Windows 10 |
| 🧠 Host RAM | 16 GB |
| ⚡ Processor | Intel Core i5 |
| 🧰 Hypervisor | VirtualBox 7.2.16 r174877 |
| 🐉 Security OS | Kali Linux 2026.2 |
| 🧠 Kali RAM | 2048 MB |
| 🌐 Virtual Network | NAT Network |
| 📡 Network Address | 10.0.0.0/24 |
| 🐧 Kali IP Address | 10.0.0.4/24 |
| 🚪 Default Gateway | 10.0.0.1 |
| 🌐 DNS Server | 8.8.8.8 |
| 🔮 Future VM Range | 10.0.0.5 - 10.0.0.99 |



🛠️ Lab Setup Procedure

The cybersecurity laboratory environment was set up using Oracle VirtualBox and Kali Linux. The following steps were performed to create a controlled environment for cybersecurity learning and authorized security testing.

Step 1 — Install 7-Zip

7-Zip was installed to extract and manage compressed files required during the laboratory setup.

Step 2 — Install Oracle VirtualBox

Oracle VirtualBox was installed on the host computer. VirtualBox was used as the hypervisor for creating, configuring, and managing the Kali Linux virtual machine.

Step 3 — Create the NAT Network

A dedicated NAT Network was configured in VirtualBox to provide controlled communication between virtual machines while maintaining Internet connectivity.

The required network settings were configured according to the laboratory requirements.

Step 4 — Import Kali Linux

The Kali Linux virtual machine was obtained from the official Kali Linux source and imported into Oracle VirtualBox.

The virtual machine was then configured with the required hardware resources, including RAM, storage, and network adapter settings.

Step 5 — Configure the Virtual Machine Network

The Kali Linux virtual machine's network adapter was configured to connect to the dedicated NAT Network.

This configuration allows the virtual machine to communicate within the controlled laboratory network while providing the required external connectivity.

Step 6 — Configure Kali Linux Network Settings

After starting Kali Linux, the network interface and IPv4 configuration were checked.

The IP address, subnet mask, default gateway, and DNS configuration were verified to ensure that the system could communicate correctly within the laboratory environment.

Step 7 — Verify Network Connectivity

Network connectivity was tested using basic networking commands.

The following checks were performed:

- Verified the assigned IP address.
- Tested connectivity to the default gateway.
- Tested Internet connectivity.
- Verified DNS resolution.

Step 8 — Create a Clean Virtual Machine Snapshot

After successfully completing the initial configuration and connectivity tests, a clean snapshot of the Kali Linux virtual machine was created.

The snapshot provides a recovery point that can be restored before future cybersecurity experiments.

Step 9 — Document the Laboratory Setup

Screenshots were captured during the important stages of the setup, including the VirtualBox configuration, Kali Linux environment, network configuration, and verification results.

The documentation was organized and uploaded to the GitHub repository as part of the Week 1 project submission.

Result

The cybersecurity laboratory environment was successfully prepared using Oracle VirtualBox and Kali Linux. The environment provides a controlled platform for future cybersecurity learning, network-security exercises, and authorized penetration-testing activities.




🔎 Lab Verification

After completing the cybersecurity lab setup, the following checks were performed to verify that the Kali Linux virtual machine and network configuration were functioning correctly.

Verification Check	Method / Command	Expected Result

IP Address	ip a	Kali Linux displays a valid IP address.
Network Interface	ip link	The configured network interface is active.
Default Gateway	ip route	A default route/gateway is displayed.
Gateway Connectivity	ping -c 4 <gateway-ip>	Successful replies are received from the gateway.
Internet Connectivity	ping -c 4 8.8.8.8	Successful replies confirm Internet connectivity.
DNS Resolution	ping -c 4 google.com	Domain name resolves and replies are received.
Virtual Machine Status	Oracle VirtualBox	Kali Linux VM runs without configuration errors.
Snapshot	VirtualBox Snapshot Manager	A clean recovery snapshot is available.


✅ Verification Result

The lab environment was verified successfully by checking the network interface, IP configuration, default gateway, Internet connectivity, and DNS resolution. The Kali Linux virtual machine was confirmed to be operating within the configured virtual network.




🐞 Problems Encountered & Solutions

No major problems were encountered during the initial laboratory setup.

However, during network configuration, assigning a specific static IP address may result in connectivity issues if the address is not compatible with the configured NAT Network.

Problem 1 — Internet Connectivity Issue

Problem:
A manually assigned IP address may prevent Kali Linux from accessing the Internet if the IP configuration does not match the configured virtual network.

Solution:
The IP configuration was checked against the NAT Network settings. A valid IP address within the configured network range was selected, and the gateway and DNS settings were verified.

Problem 2 — Kali Linux NetworkManager IPv4 Timeout

Problem:
Kali Linux may occasionally experience an IPv4 configuration timeout while establishing the network connection.

Solution:
The NetworkManager connection can be configured to disable Duplicate Address Detection timeout using:

sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0

After applying the configuration, the network connection can be restarted and connectivity verified again.

Problem 3 — Network Configuration Verification

Problem:
Incorrect IP address, gateway, or DNS settings can result in unsuccessful connectivity tests.

Solution:
The following commands can be used to verify the configuration:

ip addr
ip route
ping -c 4 8.8.8.8
nslookup networkwalks.com

These checks help confirm that the network interface, default gateway, Internet connectivity, and DNS resolution are working correctly.

Conclusion

The network configuration was reviewed and verified to ensure that the Kali Linux virtual machine could communicate correctly within the controlled laboratory environment.




💡 Lessons Learned

Through this Week 1 project, I gained practical knowledge of setting up and configuring a cybersecurity laboratory using Oracle VirtualBox and Kali Linux.

Learned how to create and configure a virtual machine using Oracle VirtualBox.

Understood the basics of virtual networking and NAT Network configuration.

Learned how to configure and verify IP addresses, gateways, and DNS settings in Kali Linux.

Gained experience using basic Linux networking commands such as ip a, ip route, and ping.

Understood the importance of maintaining an isolated and controlled environment for cybersecurity testing.

Learned how snapshots can be used to create a recovery point before performing security experiments.

Improved my ability to troubleshoot basic network connectivity issues.

Learned the importance of documenting technical work with screenshots and clear explanations.

Understood that cybersecurity testing should always be performed ethically and only on authorized systems.


📌 Key Takeaway

This project provided a strong practical foundation in virtualization, Linux networking, and cybersecurity lab setup, which will be useful for future hands-on cybersecurity exercises.




🔐 Security & Ethical Use

This cybersecurity laboratory is intended strictly for educational purposes and authorized security testing.

All cybersecurity activities performed using this laboratory should be conducted only on:

- Systems owned by me.
- Virtual machines created specifically for testing.
- Systems for which explicit permission has been provided.
- Controlled laboratory environments.

The tools and techniques available in Kali Linux must not be used to access, scan, exploit, or attack unauthorized systems.

The lab provides a safe environment to learn cybersecurity concepts while following responsible and ethical security practices.




🔗 Tools & Resources

Tool / Resource| Purpose
7-Zip| Extracting and managing compressed files used during the lab setup.
Oracle VirtualBox| Creating and managing the cybersecurity virtual machine environment.
Kali Linux| Cybersecurity-focused operating system used for security learning and authorized testing.
GitHub| Hosting and documenting the Week 1 cybersecurity project.
NetworkWalks Training| Cybersecurity training and practical learning reference.

Official Resources

- 7-Zip — https://7-zip.org/
- Oracle VirtualBox — https://www.virtualbox.org/
- Kali Linux — https://www.kali.org/
- GitHub — https://github.com/



👤 Author

Rutuja Medhekar

This cybersecurity lab was created and documented as part of the NetworkWalks Cybersecurity Training – Week 1 Project.

The laboratory setup, configuration, testing, screenshots, and documentation were completed as part of my hands-on cybersecurity learning.



🙏 Credits

The cybersecurity concepts, laboratory setup guidance, and practical learning were completed as part of the NetworkWalks Cybersecurity Training Program.

Waqas Karim — Cybersecurity Professional, CCIE

The training and laboratory concepts provided guidance for understanding VirtualBox, Kali Linux, networking, and cybersecurity lab setup.

All laboratory configuration, testing, documentation, and practical experimentation documented in this repository were performed by me in my own virtual laboratory environment.



📌 Project Information

Information| Details
Program Name| Cybersecurity at NetworkWalks
Week| 01
Project| Cybersecurity & Penetration Testing Lab Setup
Author| Rutuja Medhekar
Repository| GitHub
Primary Platform| Oracle VirtualBox
Security OS| Kali Linux
Purpose| Cybersecurity learning and authorized security testing
Documentation| GitHub README

Project Repository

NETWORKWALKS-B083-WK1-PM1-CYBERSECURITY-LAB-SETUP










