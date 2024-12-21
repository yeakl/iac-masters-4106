Поднять vm
```
vagrant up
```
Установить docker роль

```
ansible-galaxy install -r requirements.yml
```

Запустить плейбук

```
ansible-playbook playbook.yml -i hosts.ini   
```