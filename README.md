# ansible-vzwatchd-install
[![GitHub tag](https://img.shields.io/github/tag/sys0dm1n/ansible-vzwatchd-install.svg?style=plastic)](https://github.com/sys0dm1n/ansible-vzwatchd-install)
[![GitHub stars](https://img.shields.io/github/stars/sys0dm1n/ansible-vzwatchd-install.svg?style=plastic)](https://github.com/sys0dm1n/ansible-vzwatchd-install)
[![GitHub license](https://img.shields.io/github/license/sys0dm1n/ansible-vzwatchd-install.svg?style=plastic)](https://github.com/sys0dm1n/ansible-vzwatchd-install)
[![GitHub forks](https://img.shields.io/github/forks/sys0dm1n/ansible-vzwatchd-install.svg?style=plastic)](https://github.com/sys0dm1n/ansible-vzwatchd-install)
[![GitHub release](https://img.shields.io/github/release/sys0dm1n/ansible-vzwatchd-install.svg?style=plastic)](https://github.com/sys0dm1n/ansible-vzwatchd-install)
[![GitHub followers](https://img.shields.io/github/followers/sys0dm1n.svg?style=plastic)](https://github.com/sys0dm1n/)
[![Github Releases](https://img.shields.io/github/downloads/sys0dm1n/ansible-vzwatchd-install/latest/total.svg?style=plastic)](https://github.com/sys0dm1n/ansible-vzwatchd-install)


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

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

