Based on https://share.zabbix.com/cat-app/powerdns-and-powerdns-recursor but uses dependent items instead.

1. Copy zabbix_powerdns.sudoers to /etc/sudoers.d/zabbix_powerdns

2. Copy userparameter_powerdns.zabbix_agentd.conf to /etc/zabbix/zabbix_agentd.conf.d/userparameter_powerdns.conf

3. Create the following value map (Administration -> General -> Value mapping: Create value map)
Name: PowerDNS Security Status
0 -> Resolution failure
1 -> OK
2 -> Upgrade recommended
3 -> Upgrade mandatory

4. Import zabbix-powerdns.xml Zabbix template. The template uses "Agent (active)" type to get raw values -
change the type to "Agent" if you use passive agents.
