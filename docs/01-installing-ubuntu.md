Installing Ubuntu Server

--

Why Ubuntu?
* Before I could begin self-hosting services, I needed an operating system that could run continuously and support Docker containers.
* After researching different options, I decided to use Ubuntu Server because it is widely used, well documented, free, and commonly found in professional server environments.

--

Creating the Bootable USB:
* The first step was downloading the Ubuntu Server ISO from the official Ubuntu website.
* After downloading the ISO, I used Rufus to create a bootable USB drive.
* Rufus allowed me to take the Ubuntu installation image and write it to a USB drive so that the laptop could boot directly into the installer.
* Once the USB was created, I changed the laptop's boot order in the BIOS and launched the Ubuntu installer.

--

The First Major Problem:
* The installation did not go as planned.
* During the storage configuration process, Ubuntu was unable to properly install onto the laptop's drive.
* After troubleshooting the issue, I discovered that the laptop contained an Intel IMSM RAID configuration that was interfering with the installation process.
* At the time, I had little knowledge of RAID systems and storage controllers, so this became my first major learning experience.

--

Troubleshooting the RAID Issue:
* Researching the error led me to learn about
  - RAID configurations
  - Disk controllers
  - Linux storage management
  - BIOS storage settings
* After identifying the RAID-related configuration and removing the obstacle, Ubuntu was finally able to detect and configure the drive correctly.
* The installation was then able to proceed successfully.

--

First Successful Boot:
* After Ubuntu completed installation, the system rebooted successfully and presented the login screen.
* This marked the beginning of the homelab project.
* From this point forward, I could begin learning Linux commands, remote administration, Docker containers, and self-hosted services.

--

Lessons Learned:
* This installation taught me that building a server is not always as simple as following instructions.
* Unexpected problems can occur, and troubleshooting those problems is often where the most learning happens.
* The RAID issue was the first major obstacle I encountered and gave me my first experience diagnosing and solving a real server deployment problem.
