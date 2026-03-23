## Запуск плэйбуков:

### manage_docker.yml

**Все сервера:**
ansible-playbook -i inventory docker-compose-manage.yml -e "compose_action=up"

**Группа серверов:**
ansible-playbook -i inventory docker-compose-manage.yml -e "compose_action=up" --limit zabbix-proxy-servers

### deploy-ssh-keys.yml

**Все сервера:**
ansible-playbook -i inventory deploy-ssh-keys.yml -e "@ssh-key-secret.yml"

**Группа серверов:**
ansible-playbook -i inventory deploy-ssh-keys.yml -e "@ssh-key-secret.yml" --limit zabbix-proxy-servers
