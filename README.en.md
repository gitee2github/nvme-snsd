# redf

#### Description
REDF is a set of Many plug-ins for reliable data transfer assistance for nvme over fabric SAN storage networks. The plug-ins can be deployed on the host side or the storage side and defines a set of transmission interface definitions. The two ends of communication transmission and the middle switch device must support the transmission interface. For details, see the spetcial definition of the corresponding plug-in README. These plug-in also describes the supported Operating system environment and device types.


#### Software Architecture
Software architecture description
The plug-in is deployed on the SAN, host nodes, and storage nodes. After the deployment is complete, the host and storage nodes register devices with the switch. The switch stores network device registration information to the database. In addition, the switch synchronizes information to other switches on the SAN and other storage devices. The host device node and host device determine whether the storage device is online and proactively discovers and logs in to the storage device. In this way, the disk objects of the storage device can be quickly scanned. In addition, when a device is offline (for example, a fault exits or a zone member exits), the host quickly detects that the device is offline and switches to another path to access the device.    
SNSD:    
snsd_main: initialization module    
snsd_nvme: NVME cmd execution module    
snsd_reg: device information registration module    
snsd_connect: device discovery and automatic connect module    
snsd_conn_peon: Connect task scheduling and execution module    
snsd_direct: network device processing module in direct networking    
snsd_server: network message processing module in switch networking    
snsd_mgt: device information obtaining and management module    
snsd_cfg: configuration file parsing module    
Others: tools and other related modules    

#### Installation

For details, see the corresponding plug-in installation guide.

#### Instructions

For details, see the corresponding plug-in usage description.
