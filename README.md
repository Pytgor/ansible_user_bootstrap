<h3> In this repository l am setting up a simple web-server running a simple bootstrapping playbook that create an administrative user, add an ssh key for that user, and add a sudoers file for that user giving it sudo privileges without the need of typing the password </h3>



<h2> Requirements </h2>
1- Install ansible in your host machine
2- Make sure ssh is started and enable in the target machine as ansible use ssh to communicate

<h2> How to use it </h2>
1-Copy the ip of the target machine in the inventory file <br>
2- Copy your personal ssh key into th ssh_key variable which is found in the host_vars directory
3- Choose the name you want to use to create the account and type it, same as step 2 look for the user variable and type the name as the new value
4- In order to use run the following command
  a- ansible name show in the inventory all you can type (all) follow by -m ping, this wil show if the host can ping the target via ssh
  b- To run the playbook run the next command 
    ansible-playbook bootstrapping.yml
