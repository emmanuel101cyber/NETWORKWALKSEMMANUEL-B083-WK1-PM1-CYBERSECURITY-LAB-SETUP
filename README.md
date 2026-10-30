# 🔐 Cybersecurity Lab Environment Setup

**Building an isolated virtual laboratory for cybersecurity practice, penetration testing, and ethical hacking.**

`VirtualBox` `Kali Linux` `Windows 11 Pro` `Network Configuration` `Virtualization` `Penetration Testing` `Ethical Hacking`

---

## 📌 Project Overview

This project focuses on setting up and configuring a virtual cybersecurity laboratory using Oracle VirtualBox and Kali Linux.

The objective is to create a controlled environment where cybersecurity tools and techniques can be explored, tested, and practiced safely.

The virtual lab provides a foundation for performing network reconnaissance, vulnerability assessments, penetration testing, and other hands-on cybersecurity exercises.

It is also designed to support the integration of additional virtual machines that can serve as target systems for authorized security testing.

## 🖥️ Lab Configuration

The following table summarizes the hardware and software specifications used during the laboratory setup.

| Component                 | Configuration           |
| ------------------------- | ----------------------- |
| Host Operating System     | Windows 11 Pro          |
| Host RAM                  | 8 GB                    |
| Processor                 | Intel Core i5           |
| Hypervisor                | Oracle VirtualBox 7.2   |
| Security Operating System | Kali Linux 2024.2       |
| Allocated VM RAM          | 4 GB                    |
| Virtual Network           | NAT Network             |
| Network Subnet            | 10.0.0.0/24             |
| Network Interface         | eth0                    |
| Kali Linux IP Address     | 10.0.2.15               |
| Default Gateway           | 10.0.2.2                |
| DNS Server                | 8.8.8.8                 |

## 🎯 Implementation Steps

The following steps were performed to establish the virtual cybersecurity laboratory:

1. Downloaded and installed 7-Zip for file extraction.
2. Downloaded and installed Oracle VirtualBox 7.2.
3. Created a custom NAT Network with the subnet `10.0.0.0/24` and enabled DHCP.
4. Downloaded and imported the Kali Linux 2024.2 VirtualBox image.
5. Allocated 4 GB of RAM to the Kali Linux virtual machine.
6. Configured the network interface and assigned a static IPv4 address.
7. Enabled Bidirectional Clipboard and Drag & Drop in the virtual machine settings.
8. Configured Shared Folders to access the host machine's Downloads folder.
9. Verified network connectivity and internet access from Kali Linux.
10. Created a snapshot of the working virtual machine to preserve its configuration.

## 🛠️ Tools and Technologies Used

| Tool                  | Purpose                                       |
| --------------------- | --------------------------------------------- |
| Oracle VirtualBox 7.2 | Virtualization and virtual machine management |
| Kali Linux 2024.2     | Cybersecurity testing environment             |
| 7-Zip                 | File extraction                               |
| NetworkManager        | Linux network configuration                   |
| Windows 11 Pro        | Host operating system                         |

## 📸 Screenshots and Evidence

Screenshots documenting the laboratory setup and configuration will be included in this section.

* VirtualBox installation and configuration.
* Kali Linux virtual machine running successfully.
* Network configuration and IP address verification.
* NAT Network configuration.
* Successful internet connectivity test.
* Virtual machine snapshot.

## 🔧 Troubleshooting Experience

### Issue: Loss of Internet Connectivity After Static IP Configuration

**Problem:**

After assigning a static IP address to the Kali Linux virtual machine, internet connectivity was lost. The virtual machine could no longer access the internet as expected.

**Cause:**

The issue was associated with NetworkManager's handling of Duplicate Address Detection (DAD) during IPv4 network configuration. This affected the network connection after the static IP configuration.

**Solution:**

I used the NetworkManager command-line utility (`nmcli`) to modify the connection settings and reset the network interface.

The following commands were executed:

```bash
sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0

sudo nmcli connection down "Wired connection 1"

sudo nmcli connection up "Wired connection 1"
```

**Result:**

After applying the configuration changes, the network connection was reactivated and internet connectivity was restored.

This allowed the Kali Linux virtual machine to communicate with external networks successfully.

**Key Takeaway:**

This troubleshooting experience improved my understanding of Linux network configuration, NetworkManager, IPv4 addressing, and command-line network troubleshooting.

## 🧠 Lessons Learned

Through this practical exercise, I gained hands-on experience in:

* Installing and managing virtual machines using Oracle VirtualBox.
* Deploying Kali Linux as a cybersecurity testing environment.
* Configuring virtual networks and network interfaces.
* Understanding IPv4 addressing and subnet configuration.
* Configuring static IP addresses.
* Managing shared folders and virtual machine settings.
* Troubleshooting Linux network connectivity issues.
* Creating virtual machine snapshots for recovery and backup.

## 🚀 Project Outcome

Successfully established a virtual cybersecurity laboratory using Oracle VirtualBox and Kali Linux.

The environment provides a foundation for future practical exercises involving network reconnaissance, vulnerability assessment, penetration testing, and other cybersecurity activities.

This project represents my first practical exercise during the Networkwalks Cybersecurity Internship.

---

## 👨‍💻 Author

**Idowu Oluwaferanmi Emmanuel**

* **GitHub:** [@emmanuel101cyber](https://github.com/emmanuel101cyber)
* **Organization:** Networkwalks
* **Internship:** Cybersecurity Internship
* **Internship ID:** NW-084-000
* **Week:** 01

---

**Learning. Practicing. Building. Growing.**

*Better Security Tomorrow.*


