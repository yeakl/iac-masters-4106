## Лабораторная работа №4

### Роли в гитлабе
[OpenVPN-роль](https://gitlab.com/yeklalex-k/ansible-roles/anisble-role-openvpn)


### Установка

Из корневой директории репозитория:

Поднять vm
```
vagrant up
```
Установить роли

```
ansible-galaxy install -r lab4/requirements.yml
```

Запустить плейбук

```
ansible-playbook lab4/playbook.yml -i lab4/hosts.ini   
```