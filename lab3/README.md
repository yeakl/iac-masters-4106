## Лабораторная работа №3

### Роли в гитлабе
[Docker-роль](https://gitlab.com/yeklalex-k/ansible-roles/ansible-role-docker)

[Nginx роль](https://gitlab.com/yeklalex-k/ansible-roles/ansible-role-nginx)

### Установка

Из корневой директории репозитория:

Поднять vm
```
vagrant up
```
Установить docker и nginx роли

```
ansible-galaxy install -r lab3/requirements.yml
```

Запустить плейбук

```
ansible-playbook lab3/playbook.yml -i lab3/hosts.ini   
```