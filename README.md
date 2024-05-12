<h1>Kali Linux - Initial Setup & Troubleshooting Guide (Windows 10)</h1>

<h2>Table of Contents</h2>
1. <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#description"> Description </a> <br />
2. <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#virtualbox-install-walk-through"> VirtualBox Install Walk-Through </a> <br />
3. <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#kali-linux-install-walk-through"> Kali Linux Install Walk-Through </a> <br />
4. <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#troubleshooting-guide"> Troubleshooting Guide </a> <br />

<h2>Description</h2>
The Cyber Security Project involves the initial setup and troubleshooting of a Kali Linux virtual machine (VM) using Oracle VM VirtualBox. Kali Linux is a popular Linux distribution widely used for penetration testing, ethical hacking, and security auditing.

The project aims to provide a secure and isolated environment for conducting various security-related activities, such as vulnerability scanning, network analysis, and penetration testing. By setting up a Kali Linux VM, participants can gain hands-on experience with tools and techniques commonly employed by cybersecurity professionals.

The project involves the following steps:

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

Installation of Oracle VM VirtualBox: Participants install the Oracle VM VirtualBox software on their host machine, ensuring compatibility with their operating system. This step may require system configuration adjustments to enable virtualization.

Obtaining Kali Linux: Participants download the Kali Linux ISO image from the official website. The ISO file contains the complete operating system and tools necessary for conducting security assessments.

Creating a Kali Linux VM: Using Oracle VM VirtualBox, participants create a new virtual machine and configure its settings. This includes allocating system resources such as CPU, RAM, and storage for optimal performance.

Installing Kali Linux: Participants mount the Kali Linux ISO image in the virtual machine and proceed with the installation. They follow the installation wizard to set up the operating system, create user accounts, and configure network settings.

Post-installation setup: After installing Kali Linux, participants update the system packages and repositories to ensure they have the latest versions of security tools. They may also customize the VM settings, install additional packages, or configure network adapters based on their project requirements.

Troubleshooting and Issue Resolution: Participants troubleshoot common issues that may arise during the setup process. This includes addressing network connectivity problems, resolving hardware conflicts, or resolving compatibility issues between the host machine and the virtual environment.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------

Throughout the project, participants gain practical knowledge of virtualization technologies, operating system installation and configuration, and troubleshooting techniques. They also become familiar with the Kali Linux ecosystem and its wide range of cybersecurity tools.

By successfully setting up and troubleshooting the Kali Linux VM, participants lay the foundation for performing various cybersecurity tasks within a secure and controlled environment. This project serves as an essential step towards developing practical skills in the field of cyber security and ethical hacking.
<br />

<h3>Minimum Hardware Requirements</h3>

- <b>Processor: A dual-core processor or higher is recommended. However, a single-core processor can suffice for basic usage.</b> 
- <b>RAM: At least 2 GB of RAM is required for running Kali Linux smoothly. However, it is recommended to have 4 GB or more for better performance, especially when running resource-intensive security tools.</b>
- <b>Storage: A minimum of 20 GB of free disk space is required to install Kali Linux. However, it is advisable to allocate more space (at least 40 GB or higher) to accommodate additional software packages, tools, and data.</b>
- <b>Graphics: Any graphics card that supports the host operating system is sufficient for running Kali Linux in a virtual machine.</b>
- <b>Network: A network interface card (NIC) is required for network connectivity within the Kali Linux VM. Oracle VM VirtualBox allows you to configure network adapters, including NAT, Bridged, or Host-only networking, based on your requirements.</b>
- <b>Host Machine: The host machine should meet the minimum requirements for running Oracle VM VirtualBox itself. Refer to the VirtualBox documentation for specific details regarding the host machine's operating system, processor, RAM, and storage requirements.</b>

<i>It is important to note that the above specifications represent the minimum requirements, and for a better experience, it is recommended to have higher specifications, especially when working with resource-intensive tasks or running multiple virtual machines simultaneously. </i>

<h3>Languages and Utilities Used</h3>

- <b>VirtualBox 7.0.8 Platform Packages</b> (Windows hosts)
- <b>VirtualBox 7.0.8 Oracle VM VirtualBox Extension Pack</b> (All supported platforms)
- <b>Kali Linux - Installer Images</b> (64-bit Installer)
- <b>Bash</b>
- <b>BIOS</b>

<h3>Environments Used </h3>

- <b>Windows 10</b> (22H2 / OS Build 19045.2965)
- <b>Kali Linux</b> (2023.2)


<h2>VirtualBox Install Walk-Through:</h2>

<p align="center">
 <i>If you already have VirtualBox installed, please skip ahead to <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#kali-linux-install-walk-through"> Kali Linux Install </a>. </i> <br />
 <i>Back to <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#kali-linux---initial-setup--troubleshooting-guide-windows-10"> main </a></i> <br />
 <br />
 <br />
 Go to <a href="https://www.virtualbox.org/wiki/Downloads">VirtualBox</a>.<br /> 
 Download <b>VirtualBox 7.0.8 Platform Packages</b> (Windows hosts) and <b>VirtualBox 7.0.8 Oracle VM VirtualBox Extension Pack</b> (All supported platforms).
<br/>
<img src="https://i.imgur.com/YIHswd0.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 Go to Downloads Folder. Run <b>VirtualBox-7.0.8-156879-Win.exe.</b><br/>
<img src="https://i.imgur.com/0PTxQKW.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 In the <b>Oracle VM VirtualBox Setup Wizard</b>, Click <b>Next</b>.<br/>
<img src="https://i.imgur.com/o4EZXBL.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 For the <b>Custom Setup</b>, leave Location as <b>C:\ProgramFiles\Oracle\VirtualBox\</b> and press <b>Next</b>.<br/>
<img src="https://i.imgur.com/tJ4t5U3.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 Proceed with the installation by pressing <b>Next</b>.<br/>
 <i>Warning: You will be disconnected from your Network during a brief portion of this installation. </i><br />
 <i>Warning: If you are Missing Dependencies Python Core / win32api, refer to the <a href="https://github.com/raygborje/Kali.Linux.VM/blob/main/README.md#missing-dependencies-python-core--win32api">Troubleshooting Section</a>.</i><br />
 <img src="https://i.imgur.com/2y8DnD4.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 At the <b>Ready to Install</b> window, press <b>Install</b>, allow the install, and let the installation complete.<br />
 <i>You may receive a prompt for a network/usb adapter during this process. Make sure to press Yes when this occurs.</i><br />
 <img src="https://i.imgur.com/QVwKIkv.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 Once the installation is complete, leave the checkmark as checked and press <b>Finish</b>.<br />
 <img src="https://i.imgur.com/iC60Y7u.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 Now, we will be installing the extension pack we downloaded earlier onto <b>VirtualBox</b>.<br />
 In <b>Oracle VM VirtualBox Manager</b>, go to <b>Tools</b>, click on the blue squares, and select the <b>Extensions</b> tab. <br />
 <img src="https://i.imgur.com/A3e0HW6.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 Click on <b>Install</b> and select the <b>Oracle_VM_VirtualBox_Extension_Pack-7.0.8.vbox-extpack</b> file. Press <b>Open</b>.<br />
 <img src="https://i.imgur.com/8rDPIwY.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 Click on <b>Install</b>, scroll down to the <b>VirtualBox License</b>, press <b>I Agree</b>.<br />
 <img src="https://i.imgur.com/JZLJbYX.png" height="60%" width="60%" alt="VirtualBox Install Steps"/><br />
 <img src="https://i.imgur.com/7SFC5FV.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
 The Extension Pack has been successfully installed and <b>Oracle VM VirtualBox</b> is ready for use.<br />
 <img src="https://i.imgur.com/bNKEvgE.png" height="60%" width="60%" alt="VirtualBox Install Steps"/>
<br />
<br />
</p>

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
