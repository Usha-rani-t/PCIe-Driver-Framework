# PCIe Overview

## What is PCIe?

Peripheral Component Interconnect Express (PCIe) is a high-speed serial communication interface used to connect peripherals such as Ethernet controllers, NVMe SSDs, GPUs, FPGA cards, and custom hardware to a host processor.

## PCIe Architecture

A PCIe system consists of:

- Root Complex (RC)
- PCIe Switch (Optional)
- Endpoint Devices (EP)

### Root Complex

The Root Complex connects the CPU and memory subsystem to the rest of the PCIe topology. It initiates enumeration and resource allocation during system boot.

### PCIe Switch

A PCIe switch expand the number of available connection ports, allowing multiple endpoints to connect to a single root port

### Endpoint

An Endpoint is a PCIe device such as:
- Network Card
- NVMe SSD
- GPU's
- AI Accelerator

## Base Address Registers (BARs)

BARs define memory or I/O regions used by a PCIe device.

Linux maps BARs into kernel virtual memory to allow software access to device registers.

## Interrupts

PCIe devices can generate:

### Legacy Interrupts (INTx)

Traditional interrupt mechanism.

### MSI

Message Signaled Interrupts use memory write transactions instead of dedicated interrupt lines.

Advantages:
- Better performance
- Reduced interrupt sharing
- Improved scalability

### MSI-X

Enhanced version of MSI supporting multiple interrupt vectors.

## Linux PCI Subsystem

Linux provides APIs for:

- PCI Device Enumeration
- Driver Registration
- BAR Mapping
- Interrupt Handling
- DMA Operations

Common APIs:

- pci_register_driver()
- pci_enable_device()
- pci_iomap()
- pci_alloc_irq_vectors()

## References

This document is part of the PCIe Driver Framework learning project.
