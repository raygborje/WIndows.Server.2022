<h1>Windows Server 2022 - Setting Up Active Directory</h1>

<h2>Table of Contents</h2>
1. <a href="https://github.com/raygborje/Windows.Server.2022/blob/main/README.md#description"> Description </a> <br />
2. <a href="https://github.com/raygborje/Windows.Server.2022/blob/main/README.md#minimum-hardware-requirements"> Minimum Hardware Requirements </a> <br />
3. <a href="https://github.com/raygborje/Windows.Server.2022/blob/main/README.md#preparing-a-bootable-usb-drive-using-rufus"> Preparing a Bootable USB Drive using Rufus </a> <br />

<h2>Description</h2>
Embarking on the journey toward becoming a proficient Azure Administrator and aspiring Cyber Security Professional necessitates hands-on experience in crafting resilient infrastructures from the ground up. Establishing an Active Directory (AD) environment with Windows Server 2022 within a home lab serves as an invaluable stepping stone, providing a practical playground for honing skills, experimenting with configurations, and deepening understanding of core concepts.
<br /> <br />

The process commences with the procurement of hardware resources conducive to hosting virtualized environments. Leveraging virtualization platforms such as Hyper-V or VMware, a Windows Server 2022 instance is provisioned, serving as the cornerstone of the AD deployment. This exercise not only familiarizes oneself with server deployment procedures but also instills proficiency in managing virtualized environments—an essential skill set in contemporary IT landscapes.

With the server infrastructure in place, the installation and configuration of Windows Server 2022 are meticulously undertaken, following prescribed installation procedures and adhering to security best practices. This foundational step lays the groundwork for hosting Active Directory Domain Services (AD DS) roles, pivotal in facilitating centralized identity and access management within the lab environment.

Guided by a zeal for learning and a thirst for knowledge, the aspiring Cyber Security Professional delves into the intricacies of AD DS configuration, meticulously crafting domain structures, organizational units (OUs), and user accounts reflective of real-world scenarios. This hands-on experience not only solidifies comprehension of AD fundamentals but also cultivates problem-solving skills essential in addressing diverse challenges encountered in cyber security landscapes.

Furthermore, the integration of additional Windows Server roles and features, such as DNS and DHCP services, further enriches the lab environment, mirroring the complexities of enterprise-grade infrastructures. This holistic approach to infrastructure deployment fosters a comprehensive understanding of interdependencies and the interconnected nature of IT systems—a cornerstone of effective cyber security strategies.

As the lab environment matures, the aspiring professional explores advanced AD functionalities, such as Group Policy Objects (GPOs), fine-tuning security policies, and implementing access controls. Moreover, the integration with cloud services, including Azure Active Directory (Azure AD), offers a glimpse into hybrid cloud architectures, preparing individuals for the evolving paradigms of modern IT environments.

Throughout this journey, the home lab serves as a crucible for experimentation, innovation, and growth—a safe haven where mistakes are valued as opportunities for learning, and triumphs serve as catalysts for advancement. Armed with newfound knowledge and practical experience, the aspiring Cyber Security Professional emerges equipped with the skills and confidence to navigate the complexities of cyber security landscapes with poise and proficiency.

The project involves the following steps:

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

- Preparing a Bootable USB Drive using Rufus. 
- Install Windows Server on at least one machine to act as the domain controller for Active Directory.
- Install Active Directory Domain Services (AD DS) on the designated server.
- Promote the server to a domain controller by running the Active Directory Domain Services Configuration Wizard.
- Configure the domain name and forest settings.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

<h3>Minimum Hardware Requirements</h3>

- <b>USB Drive: A minimum of 10 GB will be needed to store Windows Server 2022. </b>
- <b>Processor: It is recommened to have at least 1 64bit Processor with 1.4 GHz that is Hyper -V Compatible (Intel VT or AMD -V). 64 Processors is the maximum effective limit.</b> 
- <b>RAM: At least 512 MB of RAM is required to host a Windows Server 2022. 4 TB RAM would be the maximum effective limit.</b>
- <b>Storage: A minimum of 32 GB of free disk space is required to install Windows Server 2022. However, it is advisable to allocate more space (at least 80 GB or higher) to accommodate additional software packages, tools, and data.</b>
- <b>Graphics: Any graphics card that supports the host operating system is sufficient for running Windows Server 2022.</b>
- <b>Network: A network adapter capable of at least 1 Gbps throughput.</b>

<i>It is important to note that the above specifications represent the minimum requirements, and for a better experience, it is recommended to have higher specifications, especially when working with resource-intensive tasks or running multiple virtual machines simultaneously. </i>

<h3>Languages and Utilities Used</h3>

- <b>Rufus 4.4</b> (Windows hosts)
- <b>Windows Command Line</b> (Windows hosts)
- <b>Powershell</b> (Windows hosts)
- <b>BIOS</b>

<h3>Environments Used </h3>

- <b>Windows Server 2022</b>
- <b>Windows 11</b>


<h2>Preparing a Bootable USB Drive using Rufus:</h2>
Download Windows Server 2022 ISO <a href=https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022>here</a><br />
Download Rufus <a href= https://rufus.ie/en/>here</a>

Have the Bootable USB Device plugged in. <br /><br />
	1. Launch Rufus from .exe file <br />
	2. Select the bootable USB Drive as the Device. <br />
	3. Under "Boot Selection", press "Select" and select the Windows Server 2022 ISO. <br />
	4. Leave the default settings that are pre-selected by Rufus. <br />
	5. Under "Volume Label", you can place a custom name for the Bootable USB Drive. Press Start. <br />
	6. Leave the selected settings and press OK. **WARNING**Data remaining on the USB will be destroyed at this point. <br />
	7. Wait for Status to read as READY. You should see the following files/folders in the Bootable USB Device. <br />
	&emsp;a. Boot (Folder)<br />
	&emsp;b. Efi (Folder)<br />
	&emsp;c. Sources (Folder)<br />
	&emsp;d. Support (Folder)<br />
	&emsp;e. Autorun.inf (File)<br />
	&emsp;f. Bootmgr (File)<br />
	&emsp;g. Bootmgr.efi (File)<br />
	&emsp;h. Setup.exe (File)<br />
	8. Afterwards, safely eject the Bootable USB Device.<br />


<h2>Kali Linux Install Walk-Through:</h2>

<p align="center">
<i>Back to <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#kali-linux---initial-setup--troubleshooting-guide-windows-10"> main </a></i> 
<br />
<br />
 Go to <a href="https://www.kali.org/get-kali/#kali-installer-images">Kali Installer Images</a>. Select <b>64-bit</b> and click Download icon on <b>Installer</b><br />
 <i>Depending on your ISP, this process may take an hour or more. It is recommended to let this run in the background until completion.</i>
<img src="https://i.imgur.com/hEV3UI1.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 After the download completes, run <b>Oracle VM VirtualBox.</b> In <b>Oracle VM VirtualBox Manager</b>, click <b>New</b>.<br/>
<img src="https://i.imgur.com/V8jLjNL.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Create Virtual Machine</b>, press <b>Guided Mode</b>, enter KaliLinux into the <b>Name</b> field. For <b>ISO Image</b>, select <b>Other</b> and Select <b>kali-linux-2023.2a-installer-amd64.iso</b><br />
 <b>Type</b> should be set to Linux and <b>Version</b> should be set Ubuntu (64-bit). Press <b>Next</b>.<br/>
<img src="https://i.imgur.com/wDFmqzZ.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Hardware</b>, set <b>Base Memory</b> to at least 4096 MB and set <b>Processors</b> to 4 CPUs. Press <b>Next</b>.<br/>
<img src="https://i.imgur.com/Lnjw6Wr.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Virtual Hard disk</b>, select <b>Create a Virtual Hard Disk Now</b> and set <b>Disk Size</b> to at least 20 GB. Press <b>Next</b>.<br />
 <img src="https://i.imgur.com/rtoSkK0.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Summary</b>, review the items and press <b>Finish</b>.<br />
 <img src="https://i.imgur.com/QL98zmI.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Oracle VM VirtualBox Manager</b>, select <b>KaliLinux</b> and select <b>Settings</b>.<br />
 <img src="https://i.imgur.com/sOHN68b.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Settings</b>, select <b>Display</b> and set <b>Video Memory</b> to its Maximum Value. Press <b>OK</b>.<br />
 <img src="https://i.imgur.com/jb4A7I5.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Make sure <b>KaliLinux</b> is selected and press <b>Start</b>.<br />
 <img src="https://i.imgur.com/aujmH1S.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Kali Linux</b>, select <b>Graphical Install</b> and hit <i>Enter</i>.<br />
 <img src="https://i.imgur.com/hmXflQd.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/><br />
<br />
<br />
 Select your preferred language and hit <i>Enter</i>.<br />
 <img src="https://i.imgur.com/Mr9kkyo.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Select the location that matches your time zone and hit <i>Enter</i>.<br />
 <img src="https://i.imgur.com/yjEs3XP.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Select your preferred keyboard configuration and hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/WAlmTn9.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Once you reach <b>Configure the network</b>, leave <b>Hostname</b> as default and hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/Nz2lMyf.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 For <b>Domain name</b>, you can leave the field blank. Hit <i>Enter</i>.<br />
 <img src="https://i.imgur.com/d7cKnWb.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Set up users and passwords</b>, set <b>Full name for the new user</b> as a custom user name. Hit <i>Enter</i>.<br />
 <i>Warning: It may be difficult to change this later, so make sure it is something you will remember!</i><br />
 <img src="https://i.imgur.com/e5nrgoS.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 For <b>Username for your account</b>, a username will be generated from what you typed earlier. Leave as is and hit <i>Enter</i>.<br />
 <i>Warning: It may be difficult to change this later, so make sure it is something you will remember!</i><br />
 <img src="https://i.imgur.com/S9Lw0sk.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Create a password and enter the password in both of the available fields. Press <b>Continue</b>.<br />
 <i>Warning: It may be difficult to change this later, so make sure it is something you will remember!</i><br />
 <img src="https://i.imgur.com/xK5l7mT.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Configure the clock</b>, choose your corresponding time zone and hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/TvHuh3G.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Partition disks</b>, select <b>Guided - use entire desk</b> and hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/RDhHNN5.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 There should only be one disk to select to partition. Hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/E4WfRn8.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Select <b>All files in one partition (recommended for new users)</b> and hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/kLi93zf.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Select <b>Finish partitioning and write changes to disk</b> and hit <i>Enter</i>. <br />
 <img src="https://i.imgur.com/NoiZ6BW.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Select <b>Yes</b> for <b>Write the changes to disks?</b> and hit <i>Enter</i>. <br/>
 <img src="https://i.imgur.com/ZMSX9Xl.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Software selection</b>, leave the default selections and press <b>Continue</b>. <br />
 <img src="https://i.imgur.com/mYxh6Ps.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 In <b>Install the GRUB boot loader</b>, select <b>Yes</b> and press <b>Continue</b>. <br />
 <img src="https://i.imgur.com/d0U9A8y.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Select the first device that appears under <b>Enter device manually</b>. Press <b>Continue</b>. <br />
 <img src="https://i.imgur.com/wDOnTBj.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>
<br />
<br />
 Kali Linux has now been completely installed for use through <b>Oracle VM VirtualBox</b>. Press <b>Continue</b> to reboot the VM. <br />
 <img src="https://i.imgur.com/nbOR9vl.png" height="60%" width="60%" alt="Kali Linux Walk-Through"/>

</p>

<h2>Troubleshooting Guide:</h2>
<p align="center"> <i>Back to <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#kali-linux---initial-setup--troubleshooting-guide-windows-10"> main </a></i> </p>
<br />
 
<h4>Missing Dependencies Python Core / win32api</h4>
<p align="center">
 Install Python from <a href="https://www.python.org/downloads/">here</a> <br />
 Once Python is installed, open cmd and execute the following command: 
<br />
 <i> pip install pywin32 </i>
<br />
 You might have to update pip during this process. To update pip, run the following command in cmd:
<br />
 python.exe -m pip install --upgrade pip
<br />
 You should now be able to proceed with the installations without any further issues.
<br />
 
</p>
<h4>"Not in a hypervisor partition (HVP=0)(VERR_NEM_NOT AVAILABLE)" Error</h4>

<p align="center">
 You need to enable virtualization on your CPU through the BIOS settings. Refer to this <a href="https://recoverit.wondershare.com/partition-tips/not-in-a-hypervisor-partition.html">guide</a>.
<br />
</p>

<h4>Updating Linux through Terminal</h4>
<p align="center">
 Enter the following commands into the terminal: <br />
 <i>sudo apt-get update</i> <br/>
 <i>sudo apt update</i> <br />
 <i>sudo apt upgrade</i> <br />
 Once all of these commands have completed, Linux should be up-to-date. <br />
</p>



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
