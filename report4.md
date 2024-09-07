Команды для настройки SSH:
На целевой машине-сервере:
sudo nano /etc/ssh/sshd_config
Например, можно поменять порт для подключения

На клиенте сгенерировать ключ:
ssh-keygen
Скопировать публичную часть ключа на сервер:
ssh-copy-id username@server_ip_address
либо
scp name.txt user@ip_addr:/path

Перезапуск ssh-server
sudo systemctl restart ssh

После этого можно подключиться, например:
ssh -i ~/.ssh/test_linux user@127.0.0.1 -p 3055

