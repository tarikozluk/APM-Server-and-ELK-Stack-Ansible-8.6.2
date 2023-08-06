# APM-Server-and-ELK-Stack-Ansible-8.6.2
Ansible Playbooks: ELK Stack and APM-Server Installation for version 8.6.2

ELK Upgrade is comfortable with 8.x and higher versions. You can use the same playbook to upgrade ELK Stack with APM Server by adding this block to your playbook yml

```
cp /etc/elasticsearch/elasticsearch.yml /home/current_user/
cp /etc/apm-server/apm-server.yml /home/current_user/
cp /etc/kibana/kibana.yml /home/current_user/
```

After the upgrade process;

```
mv  /home/current_user/elasticsearch.yml /etc/elasticsearch/
mv /home/current_user/apm-server.yml /etc/apm-server/ 
mv /home/current_user/kibana.yml /etc/kibana/
```
add systemctl restart for all application that you want to upgrade and teady to use.

### Graylog Server yml will be added as well
