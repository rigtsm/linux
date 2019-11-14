# [Linux](https://www.youtube.com/channel/UCvA_wgsX6eFAOXI8Rbg_WiQ/playlists)

## Linux FHS: Filesystem Hierarchy Standart, Linux Directories Explained
[Linux File Structure](https://www.youtube.com/watch?v=HbgzrKJvDRw&pbjreload=10)

- /bin  : binaries, which is another word for programs/apps stored here
- /sbin : system binaries used only by the system administrator
- /boot : files the OS needs to boot
- /dev  : devices, everything is a file so also the devices are seen as files. Disk partition would be /dev/sda
- /etc  : where system configuration are saved, not per user settings 
- /lib  : where the libraries are stored, which are files that applications can use to perform various functions.
- /media: where we find the drives mounted bo the OS
- /mnt  : where we find the drives , wmounted manualy
- /opt  : optional, where manually installed software from venders resides
- /proc : information about the system processes and resources like cpuinfo, uptime
- /root : roots user home folder
- /run  : everything here runs in RAM, evrything is gone after a Reboot
- /snap : snap app folder
- /srv  : servis directory where Web/FTP server data is saved
- /sys: : system file in the way to interect with the Kernel, it is created every time the system boots up.
- /tmp  : temporary folder, where files are temporary saved by applications that could be used during the run time
- /usr  : user application space where the applications will be installed that are used by the user
- /var  : variable directory, files and directories which are expected to grow in size
- /home : where every user stores his personal files and documents and application settings (hiddin files)
     
## Ubuntu package manager APT
     
     sudo apt update # update the source list
     sudo apt upgrade # upgrade the packages
     
     
     apt search firefox
     
     sudo apt install nano
     apt show nano
     sudo apt remove nano
     sudo apt purge nano # remove the configuration settings
     sudo apt autoremove # packages not longer needed
     sudo apt edit-sources # change the source lists
     poweroffss


## Bash Shortcuts
     
     Ctrl a # line beginning
     Ctrl i # end of the line
     Ctrl r # serch a command
     ln -s file1 file2link # create file2link to link to file1, pointer to file1
     head/tail # 10 lines of the file
     tail -f /var/log # follow the file in real time, detached
     shutdown -h now #turn the machine off
     poweroff
     
     


## Interview Questions
1) How to check the kernel version of a [Linux system](https://www.youtube.com/watch?v=l0QGLMwR-lY)?
  
          uname -a
    
2) How to see the current IP address on Linux?

        ifconfig
        ip addr show <eth>

3) How to check for free disk space in Linux?

        df -ah # disk free
        df -h
        
4) How to see if a Linux service is running?

        systemctl status <service>

5) How to check the size of a directory in Linux?

        du -sh <directory>    # disk use

6) How to check for open ports in Linux?

        netstat   # deprecated
        netstat -lepunt (tulpn)
        
        ss -tunapl
        ss -tunpl

7) How to check Linux process information (CPU usage, memory, user information, etc.)?

        ps aux | grep <proc name>
        top
        
8) How to deal with mounts in Linux (USB)

        ls /mnt
        mount #check for existing mounts
        mount (absolute path to the volume) /dev/sda2 (mount point) /mnt

9) Files mounted at boot

        less /etc/fstab

9) Man pages usign it for everything information.


10) Print Unix user identity

        sudo chown $(id -u):$(id -g) $HOME/.kube/config
 
11) Get the CPU info
    
        cat /proc/cpuinfo

12) rsynk command


13) Add a new user
     
        id                            # user information
        id user                       # specific user information
        sudo useradd mom              # add a user
        sudo passwd mom               # add the psw for mom
          
        sudo groupadd nurses          # new group
        tail /etc/group               # check the groups
        sudo usermod -a -G nurses mom # add append(-G) mom to a groud, new group(-g) changing the primary
        sudo userdel mom              # delete a user
        sudo cat /etc/passwd          # user info
        sudo cat /etc/shadow          # where the password are saved
        
        #asign a directory to a group
        #add user with a differen home folder
        sudo useradd -c "User Three" -d /home/STUDENTS/user3 -m user3 
        sudo usermod -g STUDENTS user3     # user3 assigned at group STUDENTDS
        sudo usermod -G FACULTY user3      # add user3 to this group
        
        sudo userdel user3                 # remove user
        sudo userdel -r user3              # remove user and its home directory

        sudo su user3                      # change/login to the user3


## [Mounting files](https://linuxize.com/post/how-to-mount-and-unmount-file-systems-in-linux/)

      blkid | grep sd
      sudo fdisk -l | grep /dev/sd

## [Goups](https://www.linux.com/tutorials/users-groups-and-other-linux-beasts/)


