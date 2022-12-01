## CMPE-283 | Assignment 1

Team members: 
- Pranika Kakkar - 015569983
- Shreya Hunur - 015269501

### Individual Contribution

We performed the experiment in a group on Shreya's machine

#### Pranika's Contribution
I worked with Shreya on this assignment. We carefully reviewed the Assignment documentation and video uploaded on Canvas. We noted the expectations of this assignment and started the work. On her machine we performed the initial setup. I downloaded the VMWare workstation iso and downloaded the ubuntu. We tried running the make file and executed the .c code to look at the intial output as shown in the video. We both divided the task of adding the remaining structs and I added structs for ***Exit Controls***, ***Entry Controls*** and ***PinBased Controls*** and the function calls to these capabilities. I helped in code debugging when the execution failed for the .ko file and added comments for better readability. I documented my individual contribution and the steps for reproducing the output.

#### Shreya's Contribution
I worked with Pranika to complete this assignment. We first went through the Intel SDM to understand the different types of controls and how they worked. After installation of the VMware workstation, I proceeded to define the capability _info structs of all the ***Procbased controls*** . I added the calls for the same in the detect_vmx_features function.  I created a repository on Github and we both pushed the code to the repo. After merging our code, we tested it on the VM by running make command. We figured out the errors in the code when faced with execution failure. Also added the individual contribution, steps and screenshots of the output.

### Commands to run the assignment

1. Download the VMWare Workstation
2. Download ubuntu iso
3. Create a VM on VMware workstation and assign 
- RAM of 8GB
- 90GB Disk Space 
- 8 cores of processors 

Before : \
![Reproduce-Ubuntu-Setup](https://user-images.githubusercontent.com/64269342/198120968-e6064996-174b-439c-983b-5511dedd3cb4.png)

After: \
![Reproduce-Ubuntu-Setup-After](https://user-images.githubusercontent.com/64269342/198120983-886e1267-a683-49a1-bf44-709af4f39c77.png)

Note - Enable Nested Virtualization for the image

4. Use ubuntu iso image for the VM
5. Enable "Virtualize Intel VT-x/EPT or AMD- V/RVI" checkbox
6. Run the following commands
```bash

# Install make
sudo apt intall gcc make

# Check the linux version 
linux -name 
>> 5.15.0-52-generic

# Install the linux-headers
sudo apt-get linux-headers-$(uname -r)

# Check the make file
make

# Command to insert the module into a kernel
insmod ./cmpe283-1.ko

# To display the kernel output
demsg

# To Stop a running .ko file and build a new make run 
rmmod cmpe283-1

```

### Output Screenshots

![output-1](https://user-images.githubusercontent.com/64269342/198120832-7eaa4551-a0d4-426c-a18e-7caff2f069a0.png)

![output-3](https://user-images.githubusercontent.com/64269342/198120892-c841f6e0-df2e-450f-85d6-c433fc677c69.png)

![output-4](https://user-images.githubusercontent.com/64269342/198120918-e800a6bb-6b8c-4c69-9261-33432c0e7b82.png)

![output-2](https://user-images.githubusercontent.com/64269342/198120871-e1f2bb11-3c90-4218-b44d-ee4010012e9a.png)


