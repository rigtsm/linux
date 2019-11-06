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
     
     
     
## Interview Questions
1) How to check the kernel version of a [Linux system](https://www.youtube.com/watch?v=l0QGLMwR-lY)?
  
        uname -a
    
2) How to see the current IP address on Linux?

        ifconfig
        ip addr show <eth>

3) How to check for free disk space in Linux?

        df -ah # disk free

4) How to see if a Linux service is running?

        systemctl status <service>

5) How to check the size of a directory in Linux?

        du -sh <directory>    # disk use

6) How to check for open ports in Linux?

        netstat 
        netstat -lepunt

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





















