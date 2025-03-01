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

Даем права пользователю sudo chown -R $(id -u):$(id -g) {/mnt/common_volume/swarm/grafana/config,/mnt/common_volume/grafana}

Файл grafana.ini уже существует, команда touch /mnt/common_volume/grafana/grafana-config/grafana.ini обновит его временные метки (время последнего доступа и изменения). Если файл не существует, команда создаст новый пустой файл с указанным именем по указанному пути.

Команда cp config/* /mnt/common_volume/swarm/grafana/config/ копирует все файлы и подкаталоги из директории config в директорию /mnt/common_volume/swarm/grafana/config/

Переименовываем файл grafana.yaml в docker-compose.yaml командой mv grafana.yaml docker-compose.yaml

Проверяем где мы находимся командой ls
![Снимок14](https://github.com/user-attachments/assets/0dac4392-d45f-4bc8-b509-396e4f481e86)

cd grafana_stack_for_docker/ для перехода в папку

sudo docker compose up -d создает и запускает контейнеры в фоновом режиме
![Снимок12](https://github.com/user-attachments/assets/cd543f0c-a22a-40c3-8ce1-d7bb8668f1c2)

Останавливаем процесс sudo docker compose stop. Принаписанни через дефис - ошибка. Решение: пишем черещ пробел.
![0](https://github.com/user-attachments/assets/3e7530ac-b74e-4cf3-89f1-9ac5f7ed4fbe)

Останавливаем процесс с удалением  файлов sudo socker compose dowm
![1](https://github.com/user-attachments/assets/b11ba872-c023-4470-bed8-193c81987ce5)



