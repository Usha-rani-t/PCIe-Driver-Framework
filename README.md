# PCIe-Driver-Framework

Linux PCIe Driver Framework demonstrating PCI device enumeration, BAR mapping, MMIO access, interrupt handling, and user-space communication.

##Key Features
- PCIe Device Enumeration
- PCIe Device Registration
- BAR Resource Management
- MMIO Read/Write Operations
- MSI/MSI-X Interrupt Support
- Character Device Interface
- User-Space Test Application
- DMA Support
- Detailed Architecture Documentation

##Technology Stack
- C
- Linux Modules
- PCIe Subsystem
- Embedded Linux
- Interrupts
- DMA
- Git
- GCC
- Ubuntu

## Architecture

+----------------------+
|   User Application   |
+----------+-----------+
           |
           | read/write/ioctl
           |
+----------v-----------+
| Character Device     |
| Interface            |
+----------+-----------+
           |
+----------v-----------+
| PCIe Driver          |
| - probe()            |
| - remove()           |
| - BAR Mapping        |
| - MMIO Access        |
| - MSI Interrupts     |
+----------+-----------+
           |
+----------v-----------+
| PCIe Endpoint Device |
+----------------------+

## Project Roadmap

### Phase 1
- PCIe Fundamentals
- Linux PCI Subsystem Study
- Driver Skeleton Creation

### Phase 2
- PCI Driver Registration
- Probe and Remove Callbacks
- PCI Device Detection

### Phase 3
- BAR Mapping
- MMIO Read/Write Operations

### Phase 4
- Character Device Interface
- User-Space Test Application

### Phase 5
- MSI/MSI-X Interrupt Handling
- Interrupt Testing and Debugging

### Phase 6
- DMA Support
- Performance Optimization
