Команды выполнять из корневой папки!

```
cd ..
```

Поднять vm
```
vagrant up
```
Установить docker роль

```
ansible-galaxy install -r lab2/requirements.yml
```

Запустить плейбук

```
ansible-playbook lab2/playbook.yml -i hosts.ini   
```