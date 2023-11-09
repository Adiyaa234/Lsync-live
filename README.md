# Lsync-live
lsync live sync

### Step 1 

    install lsyncd
  
### Step 2

    mkdir /etc/lsyncd/lsyncd.conf.lua
  
### Step 3
    sudo nano /etc/lsyncd/lsyncd.conf.lua
  
  
### Step 4

    settings {
          logfile = "/var/log/lsyncd/lsyncd.log",
          statusFile = "/var/log/lsyncd/lsyncd.status",
    }
  
    sync  {
          default.rsyncssh,
          source = "/path/from/source/",
          host = "user@IP",
          targetdir = "/path/to/destination/",
          delete = false,
          delay = 10,
    }
  
### Step 5 Root deer hiigdeh
  
    sudo ssh-keygen -t rsa
    ssh user@IP
    login once
  
    sudo systemctl restart lsyncd

### Step 6 To tail log

    sudo nano ~/.ssh/authorized_keys
    

### Step 7 Copy The Root rsa key into authorized_keys file in Destination

    Confirm the permission as 600 and 700 chmod
    tail -f /var/log/lsyncd/lsyncd.log
    cat /var/log/lsyncd/lsyncd.log
  
