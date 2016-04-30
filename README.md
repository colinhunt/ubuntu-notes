# ubuntu-notes

## 4: init

### 4.3: SysVinit Runlevels


- Numbered from 0-6

- Reserved on all distributions:
  - 0: system halt state
  - 1: single-user mode
  - 6: system reboot

- Ubuntu runlevels:
  - 2-5: full multi-user mode

- Display current runlevel:

        runlevel
      
- Change runlevel to 5

        sudo /sbin/telinit 5

### 4.5 Startup Scripts

- First runs the `/etc/init.d/rc` script 

- `/etc/init` is where the upstart init configs live.

- `/etc/init.d` is where all the traditional sysvinit scripts and the backward compatible scripts for upstart live.

- `/etc/init/rc-sysinit.conf` controls execution of traditional scripts added manually or with update-rc.d to traditional runlevels in `/etc/rc*`

- `/etc/default` has configuration files allowing you to control the behaviour of both traditional sysvinit scripts and new upstart configs
