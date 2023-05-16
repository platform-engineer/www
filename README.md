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


#### Multipass

Multipass is the recommended method to create Ubuntu VMs on workstations. It is designed for developers who want to quickly set up a fresh Ubuntu environment with just a single command. Multipass installs on Linux, Windows and macOS, and supports leading hypervisors, including KVM.


#### Kernel-based Virtual Machine [KVM hypervisor: a beginners’ guide - Ubuntu](https://ubuntu.com/blog/kvm-hyphervisor)

KVM (Kernel-based Virtual Machine) is the leading open source virtualisation technology for Linux. It installs natively on all Linux distributions and turns underlying physical servers into hypervisors so that they can host multiple, isolated virtual machines (VMs). KVM comes with no licenses, type-1 hypervisor capabilities and a variety of performance extensions which makes it an ideal candidate for virtualisation and cloud infrastructure implementation. But what are the benefits of KVM hypervisor and how do you get started?

How does KVM work?
+ [What is KVM?](https://www.redhat.com/en/topics/virtualization/what-is-KVM)

KVM converts Linux into a type-1 (bare-metal) hypervisor. All hypervisors need some operating system-level components—such as a memory manager, process scheduler, input/output (I/O) stack, device drivers, security manager, a network stack, and more—to run VMs. KVM has all these components because it’s part of the Linux kernel. Every VM is implemented as a regular Linux process, scheduled by the standard Linux scheduler, with dedicated virtual hardware like a network card, graphics adapter, CPU(s), memory, and disks.

It’s possible to manually manage a handful of VM fired up on a single workstation without a management tool. Large enterprises use virtualization management software that interfaces with virtual environments and the underlying physical hardware to simplify resource administration, enhance data analyses, and streamline operations. Red Hat created Red Hat Virtualization for exactly this purpose.

KVM uses a combination of security-enhanced Linux (SELinux) and secure virtualization (sVirt) for enhanced VM security and isolation. SELinux establishes security boundaries around VMs. sVirt extends SELinux’s capabilities, allowing Mandatory Access Control (MAC) security to be applied to guest VMs and preventing manual labeling errors.

SELinux was originally a development project from the National Security Agency (NSA )[18] and others. It is an implementation of the Flask operating system security architecture.[19]The NSA integrated SELinux into the Linux kernel using the Linux Security Modules (LSM ) framework. SELinux motivated the creation of LSM, at the suggestion of Linus Torvalds, who wanted a modular approach to security instead of just accepting SELinux into the kernel. 





#### [Virtual Machine Manager](https://virt-manager.org/)

Virtual Machine Manager is a desktop user interface for managing KVM VMs. It presents a summary view of running guest instances, their live performance and resource utilisation statistics. Virtual Machine Manager comes with wizards that enable the creation of new VMs and the configuration of their resource allocation and virtual hardware.
The virt-manager application is a desktop user interface for managing virtual machines through libvirt. It primarily targets KVM VMs, but also manages Xen and LXC (linux containers). It presents a summary view of running domains, their live performance & resource utilization statistics. Wizards enable the creation of new domains, and configuration & adjustment of a domain’s resource allocation & virtual hardware. An embedded VNC and SPICE client viewer presents a full graphical console to the guest domain.

**install**
```
yum install virt-manager (Fedora)
apt-get install virt-manager (Debian)
emerge virt-manager (Gentoo)
pkg_add virt-manager (OpenBSD)
```

+ virt-install is a command line tool which provides an easy way to provision operating systems into virtual machines.
+ virt-viewer is a lightweight UI interface for interacting with the graphical display of virtualized guest OS. It can display VNC or SPICE, and uses libvirt to lookup the graphical connection details.
+ virt-clone is a command line tool for cloning existing inactive guests. It copies the disk images, and defines a config with new name, UUID and MAC address pointing to the copied disks.
+ virt-xml is a command line tool for easily editing libvirt domain XML using virt-install’s command line options.
+ virt-bootstrap is a command line tool providing an easy way to setup the root file system for libvirt-based containers.


**KVM hypervisor benefits**

The main benefit of the KVM hypervisor is its native availability on Linux. Since KVM is part of Linux, it installs natively, enabling straightforward user experience and smooth integration. But KVM brings more benefits compared to other virtualisation technologies. Those include:
 
-   **Performance** – One of the main drawbacks of traditional virtualisation technologies is performance degradation compared to physical machines. Since KVM is the type-1 hypervisor, it outperforms all type-2 hypervisors, ensuring near-metal performance. With KVM hypervisor VMs boot fast and achieve desired performance results.
-   **Scalability** – As a Linux kernel module, the KVM hypervisor automatically scales to respond to heavy loads once the number of VMs increases. The KVM hypervisor also enables clustering for thousands of nodes, laying the foundations for cloud infrastructure implementation.
-   **Security** – Since KVM is part of the Linux kernel source code, it benefits from the world’s biggest open source community collaboration, rigorous development and testing process as well as continuous security patching.
-   **Maturity** – KVM was first created in 2006 and has continued to be actively developed since then. It is a 15-year old project, presenting a high level of maturity. More than 1,000 developers around the world have contributed to KVM code.
-   **Cost-efficiency** – Last but not least, the cost is a driving factor for many organisations. Since KVM is open source and available as a Linux kernel module, it comes at zero cost out of the box. Businesses can optionally subscribe to various commercial programmes, such as [UA-I (Ubuntu Advantage for Infrastructure)](https://ubuntu.com/advantage) to receive enterprise support for their KVM-based virtualisation or cloud infrastructure.




#### OpenStack

OpenStack is an open-source cloud platform that manages distributed compute, network and storage resources, aggregates them into pools, and allows on-demand provisioning of virtual resources through a self-service portal. 
OpenStack is the most popular open source cloud computing platform that enables the management of distributed compute, network and storage resources in the data centre. It wraps around the KVM hypervisor providing virtualisation capabilities and enables fully automated provisioning of VMs through a self-service portal.
OpenStack is a cost-effective extension of the existing public cloud infrastructure and a reasonable alternative to proprietary virtualisation solutions. It enables organisations to optimise their cloud costs and service providers to build an infrastructure competitive to hyperscalers.

+ [What is OpenStack - Ubuntu](https://ubuntu.com/openstack/what-is-openstack)


#### LXC

+ [lxc/lxc: LXC - Linux Containers](https://github.com/lxc/lxc)

LXC is the well-known and heavily tested low-level Linux container runtime. It is in active development since 2008 and has proven itself in critical production environments world-wide. Some of its core contributors are the same people that helped to implement various well-known containerization features inside the Linux kernel.

Unprivileged containers are containers that are run without any privilege. This requires support for user namespaces in the kernel that the container is run on. LXC was the first runtime to support unprivileged containers after user namespaces were merged into the mainline kernel.

In essence, user namespaces isolate given sets of UIDs and GIDs. This is achieved by establishing a mapping between a range of UIDs and GIDs on the host to a different (unprivileged) range of UIDs and GIDs in the container. The kernel will translate this mapping in such a way that inside the container all UIDs and GIDs appear as you would expect from the host whereas on the host these UIDs and GIDs are in fact unprivileged. For example, a process running as UID and GID 0 inside the container might appear as UID and GID 100000 on the host. The implementation and working details can be gathered from the corresponding user namespace man page.



#### LXD


LXD system containers run a complete filesystem with background processes. This allows you to run any workload, or containerise your traditional systems and apps without modifying the apps or your operations. LXD containers offer the density and efficiency of containers with a VM-like experience.

Fast, dense, and secure container and VM management at any scale

LXD provides a unified user experience for managing system containers and virtual machines. For more demanding workloads, LXD can be set up in a cluster environment to run containers, VMs, or a combination of the two on a set of machines. 
LXD has direct hardware access, minimising overhead and matching the density and efficiency of containers.




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


#### [Bhyve - FreeBSD Wiki](https://wiki.freebsd.org/bhyve)

bhyve, pronounced "beehive" is a hypervisor/virtual machine manager for FreeBSD that supports most Intel and AMD processors that report the "POPCNT" (POPulation Count) processor feature in dmesg(8).

Most Intel Atom C2000, Celeron, Core i3, i5, i7 and related Xeon processors support bhyve but early "Core" processors may only support one virtual machine.

Most "Barcelona" class and newer AMD processors support bhyve but some, notably the "Kuma" core processors include POPCNT but lack the required "NRIPS" (Next RIP Save) feature. 


#### Code Analysis

[Ghidra Debugger with QEMU Emulated ARM Binary - YouTube](https://www.youtube.com/watch?v=muj9Nfk-YPY)

Ghidra is a software reverse engineering (SRE) framework created and maintained by the National Security Agency Research Directorate. This framework includes a suite of full-featured, high-end software analysis tools that enable users to analyze compiled code on a variety of platforms including Windows, macOS, and Linux. Capabilities include disassembly, assembly, decompilation, graphing, and scripting, along with hundreds of other features. Ghidra supports a wide variety of processor instruction sets and executable formats and can be run in both user-interactive and automated modes. Users may also develop their own Ghidra extension components and/or scripts using Java or Python.
+ [Ghidra](https://ghidra-sre.org/)
+ 
+ [NationalSecurityAgency/ghidra: Ghidra is a software reverse engineering (SRE) framework](https://github.com/NationalSecurityAgency/ghidra)
+ [Releases · NationalSecurityAgency/ghidra](https://github.com/NationalSecurityAgency/ghidra/releases)
+ [Issues · NationalSecurityAgency/ghidra](https://github.com/NationalSecurityAgency/ghidra/issues)

+ [Code Analysis With Ghidra: An Introduction](https://blogs.blackberry.com/en/2019/07/an-introduction-to-code-analysis-with-ghidra)


#### Multics

+ [Multics wikipedia](https://en.wikipedia.org/wiki/Multics)
+ [Multics History](https://www.multicians.org/history.html)

Multics (Multiplexed Information and Computing Service) is a time-sharing operating system begun in 1965 and used until 2000. The system was started as a joint project by MIT's Project MAC, Bell Telephone Laboratories, and General Electric Company's Large Computer Products Division. Professor Fernando J. Corbató of MIT led the project. Bell Labs withdrew from the development effort in 1969, and in 1970 GE sold its computer business to Honeywell, which offered Multics as a commercial product and sold dozens of systems, until its cancellation in 1985.

Multics included

    a supervisor program that managed all hardware resources, using symmetric multiprocessing, multiprogramming, and paging
    an innovative segmented memory addressing system supported by hardware
    a tree structured file system
    device support for peripherals and terminals
    hundreds of command programs, including language compilers and tools
    hundreds of user-callable library routines
    operational and support tools
    user and system documentation


![image](https://github.com/platform-engineer/www/assets/5669657/a6388062-9e09-4bf1-a591-544dffada733)



#### PRIMOS

+ [PRIMOS - Wikipedia](https://en.wikipedia.org/wiki/PRIMOS)

PRIMOS is a discontinued operating system developed during the 1970s by Prime Computer for its minicomputer systems. It rapidly gained popularity and by the mid-1980s was a serious contender as a mainline minicomputer operating system.
With the advent of PCs and the decline of the minicomputer industry, Prime was forced out of the market in the early 1990s, and by the end of 2010 the trademarks for both PRIME[1] and PRIMOS[2] no longer existed.[3]
Prime had also offered a customizable real-time OS called RTOS.




### What is a Mainframe?

+ [What is a Mainframe?](https://www.microfocus.com/en-us/what-is/mainframe)

Mainframes were the large cabinets housing the central processing unit (CPU) and main memory of early computers. The term persists to describe and differentiate these larger computers, known for their considerable size and amount of storage, processing power, and reliability, from smaller counterparts such as servers, minicomputers, workstations, and personal computers (PCs). While mainframe is a generic term, most people instantly associate these computing workhorses with IBM and their System Z, the most popular and widely used models. The Z15 is the latest model.



### Illumos

+ [illumos - Wikipedia](https://en.wikipedia.org/wiki/Illumos)

Illumos (stylized as illumos) is a partly[3] free and open-source Unix operating system. It is based on OpenSolaris, which was based on System V Release 4 (SVR4) and the Berkeley Software Distribution (BSD). Illumos comprises a kernel, device drivers, system libraries, and utility software for system administration. This core is now the base for many different open-sourced illumos distributions,[4] in a similar way in which the Linux kernel is used in different Linux distributions.[5]

The maintainers write illumos in lowercase[6] since some computer fonts do not clearly distinguish a lowercase L from an uppercase i: Il (see homoglyph).[7] The project name is a combination of words illuminare from Latin for to light and OS for Operating System.[8] 


#### Features

+ **ZFS**, a combined file system and logical volume manager providing a high level of data integrity for very large storage capacities.
+ **Solaris Containers** (or Zones), a low overhead implementation of operating-system-level virtualization technology for x86 and SPARC systems.
+ **DTrace, a comprehensive dynamic tracing framework for troubleshooting kernel and application problems on production systems in real time.
+ **Kernel-based Virtual Machine (KVM)**, a virtualization infrastructure. KVM supports native virtualization on processors with hardware virtualization extensions.
+ **OpenSolaris Network Virtualization and Resource Control (or Crossbow)**, a set of features that provides an internal network virtualization and quality of service including: virtual NIC (VNIC) pseudo-network interface technology, exclusive ip zones, bandwidth management, and flow control on a per interface and per VNIC basis.



---

+ [edit](https://github.com/platform-engineer/www/edit/main/README.md)
