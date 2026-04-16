# Upgrading & Setting Up NVMe M.2 SSD

### Introduction

The computer was previously equipped with a 1TB Western Digital HDD. With this configuration, the system experienced significant delays in startup and a lack of responsiveness when launching applications and browsers. It frequently reached 100% disk utilization** during routine tasks, which are typically handled efficiently by an SSD. 

<img src="Screenshots/1_HDD_100%_ Utilization.PNG" alt="HDD 100% Utilization" width="800">

<img src="Screenshots/2_Lack_Response_Taskbar.jpeg" alt="Slow Response Taskbar" width="800">

To remedy this problem, the Hard Disk Drive was upgraded to a 2TB Samsung 990 Pro M.2 SSD. SSDs are significantly faster than HDDs because have a faster storing technology compare to HDD's mechanical disk technology. Specifically NVMe M.2 SSD are even more significantly faster than traditional SSDs by utilizing the PCIe slot for a more direct connection to the motherboard rather than SATA connection.

<img src="Screenshots/3_Samsung_990_Pro_NVMe_M2_SSD.jpeg" alt="Samsung 990 Pro NVMe M.2 SSD" width="800">

Samsung provided an easy data transfer software that allows users to mirror their saved data from their old storage drive to their upgraded storage drive. Before installing the new NVMe SSD, it is always important to backup all data.

<img src="Screenshots/4_Samsung_Magician_Migration_Tool.PNG" alt="Samsung Magician Migration Tool" width="800">

Files were backed up in an external hard drive in case problem arises in the process.

<img src="Screenshots/5_External_Hard_Drive_Backup.jpeg" alt="External Hard Drive Backup" width="800">

### Tools and Equipments

- Samsung 900 Pro NVMe M.2 SSD
- Philips screwdriver 
- M.2 screw and stand-off hardwares that came with the motherboard
- Anti-Static wristband and mat

<img src="Screenshots/6_Philips_Screwdriver.jpeg" alt="Phillips Screwdriver" width="800">

<img src="Screenshots/7_M2_PC_Screws.jpeg" alt="M2 PC Screws" width="800">

<img src="Screenshots/8_Antistatic_Wristband.jpeg" alt="Anti-static Wristband" width="800">

## Hardware Installation Procedure

1) Check Motherboard Manual to find where the NVMe M.2 PCIe slot is located. For my motherboard, ASUS Prime x470 Pro Series, it is located between the CPU and the first slot of the x16 PCIe slot.

<img src="Screenshots/9_Locating_M.2_Slot.jpeg" alt="Locating M.2 Slot" width="800">

2) Remove any components in the way of installation (ie. Dedicated Graphics Card) and unscrew the heatsink (if provided by the motherboard) to unveil the M.2 PCIe slot


<img src="Screenshots/10_PC_Before_Installation.jpeg" alt="PC Before SSD Installation" width="800">


<img src="Screenshots/11_PC_Components_Removed.jpeg" alt="PC Components Removed" width="800">

3) Screw in the standoff provided by the motherboard for the NVMe SSD to its correct length; usually marked on the motherboard. In my case it's 2280, 22mm wide x 80mm long.

<img src="Screenshots/12_NVMe_Standoff.jpeg" alt="NVMe Standoff" width="800">

4) Insert the NVMe M.2 SSD and screw down the SSD to the standoff. The SSD should be inserted easily.

<img src="Screenshots/13_SSD_M.2_Inserted.jpeg" alt="SSD M.2 Inserted" width="800">

<img src="Screenshots/14_M.2_SSD_Screwed_Down.jpeg" alt="M.2 SSD Screwed Down" width="800">

5) Peel off the adhesive from the back of th heatsink to expose the thermal pad to attach on the SSD to regulate its temperature. NVMe tends to generate heat during heavy use; the heatsink allows the heat to be dispearsed and disappated.

<img src="Screenshots/15_Heatsink_Before.jpeg" alt="Heatsink Before Adhesive Removed" width="800"> 

<img src="Screenshots/16_Heatsink_Adhesive_Removed.jpeg" alt="Heatsink Adhesive Removed" width="800"> 

6) Assemble all components back together.

## SSD Setup and Data Migration

For any new storage drive it must be partioned properly for use. This can be done under Disk Management. If installed correctly, Windows will be able to detect it, but will not be able to use until it is properly partitioned.

In Disk Management, right-click on the NVMe SSD and select "New Simple Volume" to create a basic storage unit. This will launch the wizard that would be used to complete the setup of the newly installed SSD.

After the SSD is installed, it is time to migrate the data from the old storage drive. Fortunately, specifically for the Samsung 990 Pro NVMe M.2 SSD, Samsung provide a tool call Samsung Magician that seemlessly migrate data from the old storage drive to the new SSD. 

Once the data has been migrated successfully, everything should work as it was before, but better and faster.

Lastly, to make sure that the UEFI easily finds the OS and boots correctly, change the boot order in the UEFI. 




