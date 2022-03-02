# Installing-Virtualbox-6.1

Start the Installation of the latest version of VirtualBox on your Kali Linux Desktop by following below steps by step.
Start by upgrading your system

    $ sudo apt update && sudo apt -y full-upgrade
    [ -f /var/run/reboot-required ] && sudo reboot -f
     
1. Import apt repoitory
         
       Add repository key:
   
       $ curl -fsSL https://www.virtualbox.org/download/oracle_vbox_2016.asc|sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/oracle_vbox_2016.gpg
       $ curl -fsSL https://www.virtualbox.org/download/oracle_vbox.asc|sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/oracle_vbox.gpg 
 
2. Add the VirtualBox repository
     
       Now that the repository key has been imported running the command:

       $ echo "deb [arch=amd64] https://download.virtualbox.org/virtualbox/debian bullseye contrib" | sudo tee /etc/apt/sources.list.d/virtualbox.list
       
3. Install VirtualBox & Extension pack

       The install VirtualBox & Extension pack on your Kali Linux.
       $ sudo apt update
       $ sudo apt install linux-headers-$(uname -r) dkms
       $ sudo apt install virtualbox virtualbox-ext-pack

      Finally, run:

          $ sudo apt update
          $ sudo apt-get install virtualbox-6.1

      Once VirtualBox is installed, you can launch it using the terminal or Desktop applications search.   

          $ virtualbox

      
