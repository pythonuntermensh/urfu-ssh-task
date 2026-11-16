# SSH-доступ к GitHub

## 1. Генерация ключей

Проверил SSH-клиент. Создал ключ ed25519 (публичный и приватный) с заданным passphrase:

```bash
ssh-keygen -t ed25519 -C "pythonuntermensh@gmail.com" -f ~/.ssh/id_ed25519
```

Приватный и публичный ключи сохранены в `~/.ssh/`.

![Генерация ключей](screenshots/01-keygen.jpg)

## 2. Добавление ключа в GitHub

Добавил публичный ключ `~/.ssh/id_ed25519.pub` в GitHub.

![Ключ в настройках GitHub](screenshots/02-github-key.jpg)

## 3. Проверка подключения

Выполнил:

```bash
ssh -T git@github.com
```

После ввода passphrase GitHub подтвердил успешную аутентификацию.

![Проверка SSH-подключения](screenshots/03-connection.jpg)
