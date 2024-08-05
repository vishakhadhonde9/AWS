# Virtualization-
- Virtualization is a process that allows for more efficient use of physical computer hardware and is the foundation of cloud computing.
- With the help of Virtualization, multiple operating systems and applications can run on the same machine and its same hardware at the same time, increasing the utilization and flexibility of hardware.
- Virtualization uses software to create an abstraction layer over computer hardware called hypervisor, enabling the division of a single computer's hardware components—such as processors, memory and storage—into multiple virtual machines (VMs).
- Each VM runs its own operating system (OS) and behaves like an independent computer, even though it is running on just a portion of the actual underlying computer hardware.


![image](https://github.com/user-attachments/assets/d8fd73a9-e7da-4ed8-8dba-ac154f974cd2)

- Host Machine:  The physical computer on which the virtual machine (VM) is created and run..
- Guest Machine: The virtual machine is referred to as a Guest Machine.

## Hypervisor- 
- A hypervisor is the software layer that manages and coordinates virtual machines (VMs).
- It acts as an interface between the VMs and the underlying physical hardware, ensuring efficient and secure allocation of hardware resources.
- Ensures each VM's memory space and compute cycles are isolated and protected.
- There are two types of hypervisors:

## Type 1 hypervisors-

- Type 1 or “bare-metal” hypervisors are installed directly on the physical hardware of the host machine.
- Type 1 hypervisors interact with the underlying physical resources, replacing the traditional operating system altogether.
- They most commonly appear in virtual server scenarios.


## Type 2 hypervisors-

- Type 2 hypervisors also known as hosted hypervisor.
- It runs on top of a regular operating system (the host).
- This means it relies on the host OS to manage the computer's hardware resources, like CPU, memory, and storage, to create and run virtual machines

![image](https://github.com/user-attachments/assets/6b7d7162-a542-4f2f-a04d-5c09385cf24c)


# AWS Global Infrastructure-
## Data Center -
- A data center is a physical location that stores computing machines and their related hardware equipment.
- These data centers allow businesses to store data, run applications, and access computing power over the internet, without needing to maintain their own hardware.
- Generally data center infrastructure falls into three broad categories:
    - Compute
    - Storage
    - Network
    
## Region -
- Region is a specific geographical area where AWS has multiple data centers.
- Each region allows you to store and process data closer to your location, providing better performance and reliability.
- Each Region is isolated from others to ensure fault tolerance and minimize impact from regional failures.

## Availability Zones -
- Inside each region, there are multiple Availability Zones.
- An Availability Zone is made up of one or more data centers with backup power, networking, and connectivity.
