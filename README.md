# ansible-vzwatchd-install
Ansible Playbook to quick install vzwatchd on your Openvz Ubuntu/Debian servers.

Vzwatchd is an OpenVZ monitoring daemon that informs the server administrator by email when a limit of the container is reached.


Requirements
------------
ANSIBLE pre installed.


Executing the script:
----------------------
Edit the vzwatchd-install.yml file and replace Your_Server_Name by your server's inventory name and edit the "dest_email_add" variable with your email address.

    #  ansible-playbook -k vzwatchd-install.yml
    
**Enter root password, you should end with an output similar to this:**

TASK: [vzwatchd | Only if it is an OpenVZ] ************************************

ok: [Your_Server_Name]

TASK: [vzwatchd | Check if it is an OpenVZ container and OS Debian or Ubuntu] ***

skipping: [Your_Server_Name]

TASK: [vzwatchd | Installing make package] ************************************

ok: [Your_Server_Name] => (item=make,gcc)

TASK: [vzwatchd | Install vzwatchd from CPAN] *********************************

changed: [Your_Server_Name]

TASK: [vzwatchd | Edit vzwatchd.conf file] ************************************

ok: [Your_Server_Name]

TASK: [vzwatchd | Configure vzwatchd to start automatically] ******************

changed: [Your_Server_Name]

TASK: [vzwatchd | Start vzwatchd] *********************************************

changed: [Your_Server_Name]

PLAY RECAP ********************************************************************

Your_Server_Name        : ok=7    changed=3    unreachable=0    failed=0
