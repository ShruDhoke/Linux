# Linux

# pipe command
    ls  | wc -l
ls act as input to the wc command

# tee command
it reads standard input and writes it to one or more files.

    ls | tee file1 file2

# shell commands:
it will kill all processes named proc

          killall proc
          
# To review boot messages in Linux:
you can follow these steps:

Open a terminal: Launch a terminal on your Linux system. You can usually find it in the Applications menu or by using the shortcut key combination Ctrl+Alt+T.

View system logs: Linux distributions typically store boot messages in system log files. The most common log file to review boot messages is /var/log/dmesg. Run the following command to display the boot messages:

  dmesg
  
This command displays the entire boot log.

# How can I verify which ports are listening on the Linux server?/ How to check if the port is in use in
it may be necessary to check if a port is already in use by a different application on your servers.
Open a terminal application i.e. shell prompt.

Run any one of the following commands on Linux to see open ports

         - lsof -i  | grep LISTEN      < it only gives you what are the ports are open to access, "systemd-127.0.0.1", 
         - ss -tulpn | grep LISTEN
         - netstat -tulpn | grep ':80'
          - nc -zv ip port
# ** Network troubleshooting commands **

netstat -plunt | grep "listen"

# sed command
            sed 's/unix/Linux/' geekfile.txt
////find the empty directory inside Linux? $ find /path/to/directory -type d -empty

# search pattern in Linux. 
 grep -i "error" /var/log/messages

# FIND disk type of Linux

/usr/sbin/lspci | grep SATA

available disk in Linux
$ lscsi

# K10 login not found
When Kasten login is not found

    helm install k10 kasten/k10 --namespace=kasten-io --version=5.5.6 --set global.persistence.storageClass=<storage-class-name> --set eula.accept=true  --set eula.company="COMPANY NAME" --set eula.email="COMPANY EMAIL"
# DNS SERVER SETUP
Open Server Manager & Add Roles & features--> Select default & go ahead and check if we have the correct hostname & IP --> Select Active Dir, DNS & add these features inside Add Roles & Features Wizard. After adding features click on Promote this server to domain & add new forest enter citiuscloud.com Inside Domain Controller Options give Password Inside NETBIOS Name we will see CITIUSCLOUD as by default name Check on pre-requites check & once it is green click on install Once everything is done we can see Citius cloud written inside Network Configuration To check if everything is correct then run the command --> nslookup (We use the nslookup command to check DNS)
