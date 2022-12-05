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
Installed multiple libraries using following commands:
1. Install ncurses by running sudo apt install libncurses-dev
2. Install flex by running sudo apt install flex
3. Install bison by running sudo apt-get install bison
4. Install sudo apt-get install libssl-dev
5. Install sudo apt install libelf-dev
6. Install sudo apt install dwarves
7. Install apt-get install zstd
