# Самоконтроль выполненения задания

1. Где расположен файл с `some_fact` из второго пункта задания?
playbook/group_vars/all/examp.yml
2. Какая команда нужна для запуска вашего `playbook` на окружении `test.yml`?
ansible-playbook site.yml -i inventory/test.yml
3. Какой командой можно зашифровать файл?
ansible-vault encrypt group_vars/deb/examp.yml group_vars/el/examp.yml
4. Какой командой можно расшифровать файл?
ansible-vault decrypt group_vars/deb/examp.yml group_vars/el/examp.yml --ask-vault-password
5. Можно ли посмотреть содержимое зашифрованного файла без команды расшифровки файла? Если можно, то как?
ansible-vault view  group_vars/deb/examp.yml --ask-vault-password
6. Как выглядит команда запуска `playbook`, если переменные зашифрованы?
ansible-playbook site.yml -i inventory/prod.yml --ask-vault-password
7. Как называется модуль подключения к host на windows?
ANSIBLE.BUILTIN.WINRM    (/usr/lib/python3/dist-packages/ansible/plugins/connection/winrm.py)
8. Приведите полный текст команды для поиска информации в документации ansible для модуля подключений ssh
ansible-doc -t connection ssh
9. Какой параметр из модуля подключения `ssh` необходим для того, чтобы определить пользователя, под которым необходимо совершать подключение?
- remote_user
        User name with which to login to the remote server, normally set by the remote_user keyword.

