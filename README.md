Устанавливаем Linux на VirtualBox. Обязательно выбираем английский язык

Устанавливаем пакет wget командой sudo yum install wget в командной строке Oracle, далее вводим свой пароль
![Снимок](https://github.com/user-attachments/assets/68d8ded3-7bb5-40ad-b6b2-2623858b2c06)


Устанавливаем curl для того, чтобы копировать и вставлять текст в командную строку
![Снимок 2](https://github.com/user-attachments/assets/f17c27b9-b3f5-4996-b85d-ae2436321811)

Скачиваем файл репозатория
![Снимок2](https://github.com/user-attachments/assets/db45030e-a36a-4aef-88c1-940081aac031)

Устанавливаем Docker Compose
![Снимок3](https://github.com/user-attachments/assets/ed679c89-c1b6-4a1e-9ca3-95d11d52e980)
![Снимок4](https://github.com/user-attachments/assets/e9a8333a-2c92-49e2-9f2f-f7ff3304623c)

Запускаем и разрешаем автозапуск
![Снимок5](https://github.com/user-attachments/assets/913211e4-f5d2-45c8-a49c-011821518a16)

Устанавливаем переменную COMVER. Grep находит последнюю версию
![Снимок 7](https://github.com/user-attachments/assets/990a8b72-9d95-4e16-9d6c-e7462c1c2b24)

Выкачиваем последнюю версию Docker Compose
![Снимок8 (2)](https://github.com/user-attachments/assets/35f4b2a0-d432-4a4e-be79-75002e50ffdb)

Установка git командой git clone https://github.com/skl256/grafana_stack_for_docker.git. Выбираем "y" и нажимаем Enter

Переходим в папку cd grafana_stack_for_docker

Создаем папки sudo mkdir -p /mnt/common_volume/swarm/grafana/config



-d продолжает команду в фоновом режиме

проблема с sudo docker-compose stop (решение - писать через пробел sudo docker compose stop)

