# www.platformengineer.net 

<iframe width="450" height="450" src="https://meeting.zoho.eu/meeting/login/embedmeeting.jsp?meetingKey=1242554154&newWindow=true&t=3c55bd981e4b5714deea68031769e8a199fb6ccbd01af66a9f8f959031b7ccf5" frameborder="0"> </iframe>


+ [platform engineer](https://www.platformengineer.net/)
+ [Folge 133 - Wie Software-Architekt:innen ausbilden?](https://software-architektur.tv/2022/09/09/folge133.html)
+ [Azul - The Java Platform for the Modern Cloud Enterprise](https://www.azul.com/) Continuously detect known vulnerabilities in your Java applications in production


In platform engineering are a few areas you should focus on:


## Resource management

This includes more than just billing and budgets; it also involves your organizational structure. Project liens are an important resource management tool. A project lien blocks projects from being deleted without approval.


## Access management

Choose components that allow you to create and manage identity groups, use IAM service accounts, and securely work with external identity providers.


## Networking

Your developers should be able to benefit from your network without having to interact with it directly or frequently. 



## ChatGPT for platform engineering

ChatGPT and other AI tools will be a game changer for debugging and troubleshooting infrastructure.

Take k8sgpt, for example. 
It advertises itself as a tool that diagnoses and triages your K8s clusters in simple English. 

AI can fix problems in real time, reducing the need for engineers to be on-call.

AI is not human, and it won’t be anywhere near sentient for a long time. 

In the meantime, we can leverage machines to lift repetitive work and toil off our shoulders. 
ChatGPT isn’t creative, it just formulated solutions based on existing information it can find. 

Examples:

+ Templates based on your requirements. (No more looking for YAML online)
+ Templates based on another service.
+ Recommendations to upsize or downsize infrastructure based on traffic.
+ Cost recommendations for your cloud providers based on your usage.

Simulations, Testing, DigitalTwins


## Languages

+ [Java Tutorial](https://jenkov.com/tutorials/java/index.html)



## Cloud

+ [Oracle ERP vs. SAP](https://www.oracle.com/erp/oracle-vs-sap/)
+ [10 Differences between Oracle and SAP](https://www.oracle.com/erp/oracle-vs-sap/differentiators/)

### [Kata Containers - Open Source Container Runtime Software | Kata Containers](https://katacontainers.io/)

> ## About Kata Containers
> 
> Kata Containers is an open source community working to build a secure container runtime with lightweight virtual machines that feel and perform like containers, but provide stronger workload isolation using hardware virtualization technology as a second layer of defense.

+ [Kata Containers](https://github.com/kata-containers)
Kata Containers is an open source project and community working to build a standard implementation of lightweight Virtual Machines (VMs) that feel and perform like containers, but provide the workload isolation and security advantages of VMs.

## Infra

+ [Join The Open Infrastructure Foundation - Open Infrastructure Foundation (OpenInfra Foundation)](https://openinfra.dev/join/individual)

> OpenInfra Foundation Individual MemberJoin over 110,000 community members from 187 countries to advance the future of open source. Everyone is welcome—the Open Infrastructure community is inclusive and diverse, and all members agree to the Open Infrastructure [Community Code of Conduct](https://openinfra.dev/legal/code-of-conduct). There are two types of accounts: Individual Member accounts, which include certain rights and responsibilities, and Community accounts, which are more limited.


## operating systems

During a conversation with Olek Suchdolski, we got some view of interesting opensource ecosystem in direction virtaulisation.
I prepared the list of interesting links with a descriptions


#### 




#### 





#### 



#### [Xen Virtualization Takes On Automotive - Linux.com](https://www.linux.com/news/xen-virtualization-takes-automotive/)

+ [Xen Project](https://xenproject.org/)

The Xen Project is focused on advancing virtualization in a number of different commercial and open source applications, including server virtualization, Infrastructure as a Services (IaaS), desktop virtualization, security applications, embedded and hardware appliances, and automotive/aviation.
+ [Downloads - Xen Project](https://xenproject.org/downloads/)


#### Xen Project Benefits
 
![image](https://github.com/platform-engineer/www/assets/5669657/cb2d648b-800a-433d-8308-560b12dc44c8)

The upstream contributions should enable enhancements to the next two Xen Project releases. These include improvements to the Xen Project Hypervisor on ARM, real-time scheduling enhancements, as well as improved security, boot time, stability, and reliability. The new technology was made possible by last year’s completion of the Xen port to ARM in the 10th year of the project’s existence.

Over the last two years, several other developments were said to have set the groundwork for the initiative, including:

    Experimental PV (paravirtualization) ARM support on Nvidia by Samsung (2013)
    Interrupts and IOMEM mapping to DomU to support driver domains by GlobalLogic (2014)
    Development of rich PV drivers for HID, Audio, GPU, framebuffer, etc. by GlobalLogic (2013-14)
    Ongoing improvements to real-time scheduling by DornerWorks and the University of Washington
    Ongoing developments of a QNX baseport by GlobalLogic and a FreeRTOS baseport by Galois.



#### Automotive Virtualization by Xen

CREATING NEX T-GEN DIGITAL COCKPIT SOLUTIONS WITH MIXED SAFET Y FUNCTIONS
Xen Hypervisor enables OEMs and Tier 1 suppliers to design mixed safety automotive systems. EPAM, the global leader
of the Xen Hypervisor for embedded and automotive, drives the innovation and delivery of this solution.
Uniquely positioned to support a new range of use cases in automotive, Xen Hypervisor’s isolation, security features,
flexible virtualization modes, driver disaggregation and ARM support make it a perfect fit for mixed safety systems and embedded applications. EPAM also supports Xen open source safety certification.
In Xen Embedded & Automotive, we use the R-Car Gen 3 processor as reference hardware for integrating Xen Hypervisor with vehicle infotainment systems:
![image](https://github.com/platform-engineer/www/assets/5669657/cd761dc1-a6a1-45f5-9df7-7818f8dfc6b0)




#### [Linux-VServer](http://linux-vserver.org/Welcome_to_Linux-VServer.org)

Linux-VServer provides virtualization for GNU/Linux systems. This is accomplished by kernel level isolation. It allows to run multiple virtual units at once. Those units are sufficiently isolated to guarantee the required security, but utilize available resources efficiently, as they run on the same kernel.

This site contains information relating to the use and development of virtual servers based on Linux-VServer. This particular virtual server model is implemented through a combination of "security contexts", segmented routing, chroot, extended quotas and some other standard tools.

Note: If this isn't what you are looking for, maybe Linux Virtual Server is. 


#### [bhyve - FreeBSD Wiki](https://wiki.freebsd.org/bhyve)

bhyve, pronounced "beehive" is a hypervisor/virtual machine manager for FreeBSD that supports most Intel and AMD processors that report the "POPCNT" (POPulation Count) processor feature in dmesg(8).

Most Intel Atom C2000, Celeron, Core i3, i5, i7 and related Xeon processors support bhyve but early "Core" processors may only support one virtual machine.

Most "Barcelona" class and newer AMD processors support bhyve but some, notably the "Kuma" core processors include POPCNT but lack the required "NRIPS" (Next RIP Save) feature. 


#### Code Analysis

Ghidra is a software reverse engineering (SRE) framework created and maintained by the National Security Agency Research Directorate. This framework includes a suite of full-featured, high-end software analysis tools that enable users to analyze compiled code on a variety of platforms including Windows, macOS, and Linux. Capabilities include disassembly, assembly, decompilation, graphing, and scripting, along with hundreds of other features. Ghidra supports a wide variety of processor instruction sets and executable formats and can be run in both user-interactive and automated modes. Users may also develop their own Ghidra extension components and/or scripts using Java or Python.
+ [Ghidra](https://ghidra-sre.org/)
+ 
+ [NationalSecurityAgency/ghidra: Ghidra is a software reverse engineering (SRE) framework](https://github.com/NationalSecurityAgency/ghidra)
+ [Releases · NationalSecurityAgency/ghidra](https://github.com/NationalSecurityAgency/ghidra/releases)
+ [Issues · NationalSecurityAgency/ghidra](https://github.com/NationalSecurityAgency/ghidra/issues)

+ [Code Analysis With Ghidra: An Introduction](https://blogs.blackberry.com/en/2019/07/an-introduction-to-code-analysis-with-ghidra)

---

+ [edit](https://github.com/platform-engineer/www/edit/main/README.md)
