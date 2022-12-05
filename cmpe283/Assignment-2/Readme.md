## CMPE-283 | Assignment 2

Team members: 
- Pranika Kakkar - 015569983
- Shreya Hunur - 015269501

### Individual Contribution

We performed the experiment in a group on Shreya's machine.

#### Pranika's Contribution


#### Shreya's Contribution
I worked with Pranika to make changes to cpuid.c and vmx.c file. I made changes to compute total number of exits (0x4ffffffc).
While running the make command, I encountered this error "make[1]: *** No rule to make target 'debian/canonical-certs.pem', needed by 'certs/x509_certificate_list'.
To resolve this error I changed the kernel configuration file from this: CONFIG_SYSTEM_TRUSTED_KEYS="debian/canonical-certs.pem" 
to this: CONFIG_SYSTEM_TRUSTED_KEYS="".
There were a couple of challenges faced in the first installation of debian VM. I tried installing ubunutu nested VM and it failed. 
We had to go through the installation process a number of times. Our final debian system which ran successfully had 2 cores of CPU 
and 20GB of disk space with debian 11.5.0 OS on it.

## Functions performed
``` bash

Installed multiple libraries using following commands:
#Install ncurses by running 
sudo apt install libncurses-dev

#Install flex by running 
sudo apt install flex

#Install bison by running 
sudo apt-get install bison

#Install 
sudo apt-get install libssl-dev

#Install 
sudo apt install libelf-dev

#Install 
sudo apt install dwarves

#Install
apt-get install zstd
```
### Output Screenshots

Part 1 - For CPUID leaf node %eax=0x4FFFFFFC:Return the total number of exits (all types) in %eax
![output-1](https://github.com/shreyahunur/linux/blob/master/cmpe283/Assignment-2/outputs/part1_output.PNG)

Part 2 - For CPUID leaf node %eax=0x4FFFFFFD:
Return the high 32 bits of the total time spent processing all exits in %ebx
Return the low 32 bits of the total time spent processing all exits in %ecx
%ebx and %ecx return values are measured in processor cycles, across all VCPUs
![output-1](https://github.com/shreyahunur/linux/blob/master/cmpe283/Assignment-2/outputs/part2_output.PNG)

## Some reference weblinks useful for setup and debugging
1. How to add sudo users in Debian?

https://www.cloudpanel.io/tutorial/how-to-add-user-to-sudoers-in-debian/


2 . Installation of Vim on Debian for writing test script

https://vitux.com/how-to-install-vim-editor-on-debian/

3. Installing KVM on Ubuntu

https://phoenixnap.com/kb/ubuntu-install-kvm#ftoc-heading-5
