## CU Research Computing Resources
This is documentation on using the shared resources available at University of Colorado Boulder. 

At the time of writing this, I (TR) prefer to use Summit for computing, since it is going to be retired this winter. Summit is supported by the National Science Foundation (awards ACI-1532235 and ACI-1532236), the University of Colorado Boulder, and Colorado State University. Alpine will be replacing Summit and is moving to stage 2 during the spring 2022 semester. Alpine is a more robust and modern system that is jointly funded by the University of Colorado Boulder, the University of Colorado Anschutz, Colorado State University, and the National Science Foundation (award 2201538). It's easier to get allocations for Summit and creates a better environment for learning. Future work will be required to transition to Alpine.

---
#### Mount Summit's Filesystem
CU Research Computing offeres multiple types of disk space. It is possible to use ```ssh``` to access the shared drive but mounting the filesystem on your machine allows the use of your favorite IDE, all other applications, and operating system GUI. 

If you are using Ubuntu or Linux, this shouldn't require much more than a few ```sudo``` commands in the terminal to install ```sshfs```. Just follow the instructions below and install what it tells you to install. The filesystem will be mounted until you restart your machine.

1. Create a mount point named "summit" in the home directory using ```mkdir```. Get the path to the directory with ```pwd```
2. Your username will be your CU Research Computing username. Use the following command to mount:
```cpp
                                                     Mount point on
                        + -- Your username           your local filesystem --+ 
                        |                                                    |
                        |                                                    |
                        |                                                    |
sshfs -o idmap=user tyre6015@login.rc.colorado.edu:/home/tyre6015 ~/Users/tylerreiser/dev/summit
```

3. Enter password and then authenticate with DUO

4. Un-mount Summit's filesystem using the following command:
```cpp
fusermount -u ~/Users/tylerreiser/dev/summit
```

If you are using an Apple machine with MacOS, there are additional steps needed to install SSHFS and give permissions to use it. Follow these instructions:

1. Download and install MacFUSE and SSHFS [from this link](https://osxfuse.github.io/).
2. Follow instructions to give permissions. Note: you will need to restart your machine, enter recovery mode, and change the permissions to allow use of MacFUSE. **Follow the instructions given by the app**.
3. Open a new terminal and follow the mounting instructions outlined above. 
4. Open a new Finder and navigate to the mount point. It should take a few seconds to load after you click on the mount point for the first time. You should see all the files on in your home directory on Summit's filesystem.

The mounted filesystem can be opened in VsCode or any other IDE to develop files.  

---
### Resources
[Research Computing User Guide](https://curc.readthedocs.io/en/latest/)   

**CURC Point of Contact:** rc-help@colorado.edu
