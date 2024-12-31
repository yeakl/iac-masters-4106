## Лабораторная работа №5

### Роли в гитлабе
[Postgresql-роль](https://gitlab.com/yeklalex-k/ansible-roles/ansible-role-pgsql)


### Установка

Из корневой директории репозитория:

Поднять vm
```
vagrant up
```
Установить роли

```
ansible-galaxy install -r lab5/requirements.yml
```

Запустить плейбук

```
ansible-playbook lab5/playbook.yml -i lab5/inventories 
```


Поднимаются два сервера, master srv1 и replica srv2. В group_vars указаны переменные, необходимые для каждого сервера.