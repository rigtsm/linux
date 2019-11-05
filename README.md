# [Linux](https://www.youtube.com/channel/UCvA_wgsX6eFAOXI8Rbg_WiQ/playlists)

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








