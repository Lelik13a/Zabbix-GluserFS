# Description
GlusterFS volumes monitoring through Zabbix.

Template "Template GlusterFS disks" finds all volumes, creates new items and triggers.

Monitor size, innodes, status, bricks count.

# Dependencies
perl, sudo, zabbix-agent, gluster.

libswitch-perl library.

Installation
============
1. copy gluster-monitoring.pl to /etc/zabbix/
2. copy zabbix_agentd.d/gluster.conf to /etc/zabbix/zabbix_agentd.d/
3. copy sudoers.d/zabbix (or its content) to /etc/sudoers.d/ 
4. chown root:root /etc/sudoers.d/zabbix ; chmod 440 /etc/sudoers.d/zabbix
5. chmod 755 /etc/zabbix/gluster-monitoring.pl
6. restart zabbix-agent daemon.
7. import "zbx_templates/Template GlusterFS disks.xml" into your templates.
8. apply template "Template GlusterFS disks" to host with gluster tools.
9. enjoy.
