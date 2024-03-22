# XCP-ng 

To facilitate hosting virtual machines (VMs) in this project, I've opted to utilize the Xen hypervisor, allowing me to run VMs on my XCP-ng server.

When beginning the installation, I first needed to download the ISO file for XCP-ng, creating a bootable USB stick using Rufus. I then used the bootable USB drive to start the host and completed the BIOS install. For the networking portion of the installation guide, I chose to use DHCP.

## Adding ISO VM Files

To streamline the process, I created a shareable file on my Windows host system, ensuring that the XCP-ng server can fetch any ISO files residing on my host.

To accomplish this:
- Identify the IP address of the host machine by executing ipconfig in the command prompt.
- Utilize the IP address of the host machine along with the path to the shareable folder housing the ISO files.
By following these steps, I established a foundation for hosting VMs on my XCP-ng server and ensured seamless access to ISO files for VM provisioning.



