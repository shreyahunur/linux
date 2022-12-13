## CMPE-283 | Assignment 3

Team members: 
- Pranika Kakkar - 015569983
- Shreya Hunur - 015269501

### Individual Contribution

We performed the experiment in a group on Shreya's machine.

#### Pranika's Contribution
I worked with Shreya to edit the code forked from the torvalds/linux. We met and discussed a solution to make changes to cpuid.c and vmx.c. I made changes for leaf node (0x4ffffffe). I had to run the make a few times to debug the errors in the make and receive the output for our \test3.c file. We had to run make command in sudo mode because permission errors were popping up. 

#### Shreya's Contribution
I worked with Pranika to modified the vmx.c file and cupid.c file for the CPUID leaf node %eax=0x4FFFFFFF
I also tested the changes made in the nested VM.



#### Steps to reproduce
``` bash
After editing code in vmx.c and in cpuid.c run the following commands: 
1. make -j 8 modules
```
<img width="461" alt="image" src="https://user-images.githubusercontent.com/64269342/205554792-f58a90c3-e9e4-4a98-91c9-951d64dbfd5c.png">

``` bash
2. make INSTALL_MOD_STRIP=1 modules_install && make install
3. lsmod | grep kvm
4. rmmod kvm
5. rmmod kvm_intel
6. modprobe kvm
7. modprobe kvm_intel
```

<img width="432" alt="image" src="https://user-images.githubusercontent.com/64269342/205554813-7405eeef-392d-47d0-9fe6-eef5951c8988.png">

``` bash
Reference: https://phoenixnap.com/kb/ubuntu-install-kvm 

8. Created a nested debian VM.
9. Check whether VM works by running command `kvm-ok`
```

<img width="362" alt="image" src="https://user-images.githubusercontent.com/64269342/205554861-f2941eb1-c400-484c-a0f6-20e8be58a304.png">

``` bash
10. Created testing code that calls cpu in inline assembly.
11. Observed and printed output
```

### Output Screenshots

Part 3 - For CPUID leaf node %eax=0x4FFFFFFE: Return the number of exits for the exit number provided (on input) in %ecx. This value should be returned in %eax 

<img width="950" alt="op3-1" src="https://user-images.githubusercontent.com/64269342/207231637-8a512839-5792-449b-aade-213a170933e3.png">

<img width="952" alt="op3-2" src="https://user-images.githubusercontent.com/64269342/207231668-d4db6255-f9c7-42d5-bd3a-b107c9cfe274.png">


Part 4 - For CPUID leaf node %eax=0x4FFFFFFF: Return the time spent processing the exit number provided (on input) in %ecx. Return the high 32 bits of the total time spent for that exit in %ebx. Return the low 32 bits of the total time spent for that exit in %ecx

<img width="960" alt="op4-1" src="https://user-images.githubusercontent.com/64269342/207231372-b94df64b-d719-4fb6-a8ff-f1a058469bf4.PNG">

<img width="960" alt="op4-2" src="https://user-images.githubusercontent.com/64269342/207231388-688657dc-9739-4cf4-8ff7-9fa10484caae.PNG">

<img width="960" alt="op4-3" src="https://user-images.githubusercontent.com/64269342/207231408-983f4817-4343-4a5e-aa60-aae9d94e26c8.PNG">

#### Questions 

1. Comment on the frequency of exits – does the number of exits increase at a stable rate? Or are there 
more exits performed during certain VM operations? Approximately how many exits does a full VM 
boot entail?

2. Of the exit types defined in the SDM, which are the most frequent? Least?

The most frequent exit types -

|Exit Number     |  Exit Description | 
|---------|------------------|
|0 |  Flask App |
|7|  Flask App |

The least frequent exit types - 


