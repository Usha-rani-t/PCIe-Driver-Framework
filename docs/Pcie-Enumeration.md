## PCIe Enumeration:
PCIe Enumeration is the process by which the system discovers and configures PCIe devices during boot. 
The Root Complex scans the PCIe bus, identifies connected devices, allocates resources, and enables communication 
between software and hardware.

## Enumeration Process
### Bus Discovery
The Root Complex scans all available PCIe buses and detects connected devices.

### Device Identification
Each PCIe device contains: Vendor ID - Manufacturer; Device ID - Device; Class code - Device Functionality; Revisio ID - Device Revision number

### Resource Allocation
The operating system allocates resources for each detected device like Memory Space, I/O Space, Interrupts, Bus Numbers

### BAR Configuration
Base Address Registers (BARs) define the memory regions used by a PCIe device.
The operating system assigns addresses to BARs and maps them for software access.

### Driver Binding
Linux searches for a matching driver based on: Vendor ID and Device ID
When a match is found, the driver's probe() function is called.

System Boot 
  | 
PCI Bus Scan 
  | 
Device Discovery 
  | 
Resource Allocation 
  | 
BAR Configuration 
  | 
Driver Matching 
  | 
probe() Execution
