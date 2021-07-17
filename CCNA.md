# Device Modes
User Mode > (enable/disable) > Privileged Mode > (configure terminal) > Global Config Mode




# CLI commands

### Move to the start of the line
CTRL+a

### Move to the end of the line
CTRL+e

### Jump back from anywhere to the privileged mode
### (The same as 'end')
CTRL+z

### enable the privileged mode
enable

### disable the privileged mode
disable

### show your current privilege level
show privilege

### enter global config mode
configure terminal

### enter the gigabitEthernet config mode
interface gigabitEthernet 0/0

### enter line config
line vty 0

### jump to the previous mode
exit

### jump to privileged mode from anywhere
### The same as CTRL+z
end


### Show physical port info
show ip interface brief


### clear config
write erase







# NAMING
## 'config' mode commands
### rename the host
hostname some-name-here

### set the login banner (motd = message of the day)
banner motd $ hello world $









# SET PASSWORD FOR THE PRIVILEGED MODE
## 'config' mode commands
### set a password (unhashed) for the privileged mode
enable password some-pass-here
### remove the password
no enable password
### set a secret (hashed) for the privileged mode
enable secret some-secret-here
### (privileged mode) show running config
show running-config








# SET PASSWORD FOR VIRTUAL TERMINAL
### 'vty' (virtual teletype)
### configure all the virtual terminals from 0 to 4
### (i.e. enter config mode for virtual terminals)
line vty 0 4
### remove login
no login
### enable login
login
### set a password
password some-password here





# SET PASSWORD FOR THE CONSOLE TERMINAL
### (config mode command)
### enter config mode for the console terminal
line con 0
### enable login
login
### set password
password some-pass-here







# SET USERNAME
### (config mode)
### create a username
username some-username
### or create a username with secret
username some-username secret som-secret




# SET IP ADDRESS FOR THE ROUTER AND TURN ON THE INTERFACE
show ip interface brief
enable 
configure terminal
interface gigabitEthernet 0/0
### assign an ip address to the interface
ip address 192.168.10.1 255.255.255.0
### turn on the interface
no shutdown




# DISABLE DNS LOOKUP (FOR SHOWING MISTAKES WHEN YOU MISTYPE SOMETHING...)
# ENCRYPT EXISTING PLAIN-TEXT PASSWORDS
enable
configure terminal 
### disable dns lookup
no ip domain-lookup
### convert the existing unencrypted passwords into encrypted ones
service password-encryption



# ENABLE SYNCHRONOUS LOGGING
enable
configure terminal 
line con 0
logging synchronous





# SAVE CONFIGURATION (ON DEVICE)
enable
copy running-config startup-config
### or shortcut
write
### check the startup config
show startup-config



# TELNET TO ROUTER USING USERNAME AND PASSWORD
enable 
conf t
username zavanton secret some-secret
### configure the virtual terminal
line vty 0 4
### enable login/password with telnet
login local










