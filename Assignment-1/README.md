# CMPE 283: Virtualization Technologies
## Assignment 1: Discovering VMX Features 
###### Bhavya Tetali (014535144),  Supriya Meduri (015262767)

## Contribution of Team Members:
Supriya Meduri - Created the environment using VMware Fusion Pro and built kernel code for IA32_VMX_PROCBASED_CTLS  and IA32_VMX_PROCBASED_CTLS processor-based controls.

Bhavya Tetali - Created the environment using VMware Fusion Pro and built kernel code for 	IA32_VMX_ENTRY_CTLS and IA32_VMX_EXIT_CTLS  processor-based controls.

We distributed the assignment uniformly so that each one of us wrote 2 MSR's Linux kernel code. We have therefore followed the same process for setting up, building, and creating the environment. We worked together to document the steps we followed in doing the assignment.

## Environment Setup

1. Downloaded the VMware Fusion Pro. 
2. Created an outer VM by selecting Ubuntu 64-bit as the guest operating system through the ISO image file. 
3. Configure it with 200 GB hard disk space and 4 GB memory. 
4. Now, run the VM and install Ubuntu.
5. To enable nested virtualization in the system, make changes in the processor section of the outer VM settings in the VMware Fusion.
6. Install KVM packages using the below command and verify processor support for KVM.
    > $ sudo apt install qemu-kvm libvirt-clients libvirt-daemon-system bridge-utils virt-manager

    > $ ls -l /dev/kvm
7. Ideally, the output should be “kvm-ok” and “KVM acceleration can be used”.
8. Installed virt-manager with the below command.
    > $ sudo apt-get install virt-manager
9. Created inner VM using Virtual Machine Manager GUI with 20GB hard disk support and downloaded Ubuntu into the inner VM.
10.Executed the below command to check if nested virtualization is enabled.
    > $ cat/proc/cpuinfo | more 
    
 ## Build and Development Process
 
1. Downloaded the cmpe283-1.c and Makefile from the Canvas file section.
2. Installed vi editor.
3. Installed make and GCC using the below commands.
    > $ sudo apt install make
    > $ sudo apt install gcc
4. Build the file using the Make command.
    > $ make
    <img width="1440" alt="make" src="https://user-images.githubusercontent.com/71044935/97088566-91572180-15e6-11eb-9d27-c384433ba921.png">




