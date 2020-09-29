Better Message of the Day
=========================

A collection of MOTD (Message of the Day) scripts I use on my Linux servers.

Messages are displayed by the Unix login command after a successful login, and
just before it executes the login shell.

Features
--------

- System information: hostname, distro and kernel
- System hardware: CPU, memory, processes, uptime and load
- System hard drives: zpool status, usage
- Services: running status
- Supports: fail2ban and docker status
- Notifications: package and security updates

Installation
------------

## Manual 

Install BMOTD by downloading the repo and copying the motd files
to `/etc/update-motd.d/`.

## Using git

Clone the repo and remove readme:

`cd /etc/update-motd.d/`

`git archive --remote=https://github.com/jwjhdev/bmotd | tar -t`
    
`sudo rm -f README.md`

Configuration
-------------

## SSHD Configuration 

Make sure you have the `PrintMotd` option set to `yes` in your sshd config.

## Fail2Ban Configuration 

If you use `50-fail2ban` and `50-fail2ban-status` you will need to make sure
the logs are not compressed by commented out the `compress` option 
in `/etc/logrotate.d/fail2ban`.

Contribute
----------

- Issue Tracker: https://github.com/jwjhdev/bmotd/issues
- Source Code: https://github.com/jwjhdev/bmotd

Support
-------

If you are having issues, please let us know in the issue tracker above.

License
-------

The project is licensed under the BSD license.