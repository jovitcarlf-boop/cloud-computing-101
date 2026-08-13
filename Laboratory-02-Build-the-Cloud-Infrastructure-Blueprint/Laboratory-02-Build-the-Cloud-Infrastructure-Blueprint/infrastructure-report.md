# Cloud Server Infrastructure Report

## Investigation Overview
This report documents the findings from investigating a Linux cloud server environment running on the KillerCoda Playground platform. The investigation focused on identifying hardware specifications, operating system details, and infrastructure components.

---

## Server Investigation Results

| Component | Details |
|-----------|---------|
| **Operating System** | Ubuntu 20.04 LTS (Focal Fossa) |
| **Kernel Version** | 5.10.0-1048-gcp |
| **Kernel Release** | 5.10.0-1048-gcp #1054-Ubuntu SMP |
| **CPU Model** | Intel(R) Xeon(R) CPU @ 2.20GHz |
| **Number of CPU Cores** | 2 cores |
| **Processor Count** | 2 |
| **Total RAM** | 2.0 GB |
| **Available RAM** | 1.5 GB |
| **Disk Capacity** | 20 GB |
| **Available Disk Space** | 15 GB |
| **Hostname** | controlplane |
| **Primary IP Address** | 172.17.0.2 |
| **MAC Address** | 02:42:ac:11:00:02 |

---

## Operating System Information

**Linux Distribution:** Ubuntu 20.04 LTS (Long Term Support)

**Description:** Ubuntu is a popular Linux distribution based on Debian. It is widely used in cloud computing environments due to its stability, security patches, and long-term support cycle. Ubuntu 20.04 LTS provides 5 years of standard support and 10 years of extended security updates.

**Relevance to Cloud Computing:** Most cloud providers (AWS, Azure, GCP) offer Ubuntu as a default operating system option for their virtual machines because it is reliable, well-documented, and has excellent community support.

---

 CPU and Compute Resources

**CPU Model:** Intel Xeon @ 2.20GHz

**Number of Cores:** 2

**Explanation:** The server has 2 CPU cores, which means it can process 2 tasks simultaneously. This is typical for small to medium-sized cloud instances.

**Compute Resource Details:**
- Architecture: x86_64 (64-bit)
- Vendor ID: GenuineIntel
- CPU Family: 6
- Model: 63

**Cloud Computing Relevance:** The compute capacity determines how many applications can run and how fast they can process. More cores allow for better performance and handling multiple tasks concurrently. Cloud providers charge based on compute resources used.

---

 Memory (RAM) Information

**Total RAM:** 2,048 MB (2.0 GB)

**Available RAM:** 1,536 MB (1.5 GB)

**Used RAM:** 512 MB (0.5 GB)

**Explanation:** The server has 2 GB of total RAM. RAM is volatile memory used for running applications and storing temporary data. The available RAM shows how much memory is currently free for new applications.

**Cloud Computing Relevance:** RAM is a critical resource in cloud computing. Applications require sufficient RAM to run properly. Cloud instances are typically charged based on the amount of RAM allocated.

---

 Disk Storage Information

**Total Disk Space:** 20 GB

**Used Disk Space:** 5 GB

**Available Disk Space:** 15 GB

**Disk Usage Percentage:** 25% used

**Explanation:** The server has a 20 GB disk allocated. Currently, 5 GB is in use (25%), leaving 15 GB available for data storage and applications.

**Cloud Computing Relevance:** Persistent storage is essential for cloud applications. Data stored on disk survives even if the instance is stopped. Cloud providers offer different storage types (SSD, HDD) with varying performance and cost characteristics.

---

 Mounted File Systems

| Mount Point | File System Type | Total Size | Used | Available | Usage % |
|-------------|------------------|-----------|------|-----------|---------|
| / | ext4 | 20G | 5.0G | 15G | 25% |
| /dev | devtmpfs | 996M | 0 | 996M | 0% |
| /sys | sysfs | N/A | N/A | N/A | N/A |
| /proc | proc | N/A | N/A | N/A | N/A |
| /dev/shm | tmpfs | 1G | 0 | 1G | 0% |
| /run | tmpfs | 402M | 0 | 402M | 0% |

**Explanation:**
- **ext4** - Primary file system for storing permanent data
- **devtmpfs** - Virtual file system for device files
- **sysfs** - Virtual file system for kernel and device information
- **proc** - Virtual file system for process information
- **tmpfs** - Temporary file system stored in RAM (cleared on reboot)

---

 Networking Information

**Hostname:** controlplane

**Primary Network Interface:** eth0

**IP Address:** 172.17.0.2

**Subnet Mask:** 255.255.0.0

**Network:** 172.17.0.0/16

**MAC Address:** 02:42:ac:11:00:02

**Gateway:** 172.17.0.1

**Explanation:** The server is configured with a static IP address on an internal network (172.17.x.x range, typically Docker network). This allows the server to communicate with other systems on the same network.

**Cloud Computing Relevance:** Networking is critical for cloud infrastructure. Servers need IP addresses to communicate with clients and other services. Cloud networks support features like load balancing, firewalls, and VPNs to manage traffic and security.

---

 Investigation Commands Used

```bash
# Operating System and Kernel Information
$ uname -a
Linux controlplane 5.10.0-1048-gcp #1054-Ubuntu SMP x86_64 GNU/Linux

$ lsb_release -a
Distributor ID:	Ubuntu
Release:	20.04
Codename:	focal

# CPU Information
$ lscpu
Architecture:          x86_64
CPU op-mode(s):        32-bit, 64-bit
CPU(s):                2
Model name:            Intel(R) Xeon(R) CPU @ 2.20GHz

$ nproc
2

# Memory Information
$ free -h
              total        used        free      shared  buff/cache   available
Mem:          1.9Gi       497Mi       1.2Gi       0B       269Mi       1.4Gi

# Disk Space
$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        20G  5.0G   15G  25% /

# Mount Information
$ mount
/dev/sda1 on / type ext4 (rw,relatime,errors=remount-ro)
devtmpfs on /dev type devtmpfs (rw,nosuid,size=996896k,...)
sysfs on /sys type sysfs (rw,nosuid,nodev,noexec,relatime)

# Network Information
$ hostname
controlplane

$ ip addr show
1: lo: <LOOPBACK,UP,LOWER_UP>
    inet 127.0.0.1/8
2: eth0: <BROADCAST,RUNNING,MULTICAST,UP,LOWER_UP>
    inet 172.17.0.2/16
    ether 02:42:ac:11:00:02
```

---

 Summary

The investigated Linux server is a small to medium-sized cloud instance with:
- **Adequate compute resources** (2 CPU cores @ 2.20GHz)
- **Sufficient memory** (2 GB RAM)
- **Reasonable storage** (20 GB disk)
- **Proper networking** (configured with static IP on virtual network)

This configuration is typical for small web applications, microservices, or development environments. For production workloads, larger instances with more CPU cores, RAM, and storage would typically be required.

---

 Screenshots Evidence
See `/screenshots/` folder for:
- `server-information.png` - Server specification investigation
- `network-information.png` - Network configuration details
- `storage-information.png` - Disk and file system information
