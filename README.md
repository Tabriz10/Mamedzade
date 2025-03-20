Устанавливаем Linux на VirtualBox. Обязательно выбираем английский язык

1. Устанавливаем пакет wget командой sudo yum install wget в командной строке Oracle, далее вводим свой пароль
![Снимок](https://github.com/user-attachments/assets/68d8ded3-7bb5-40ad-b6b2-2623858b2c06)


2. Устанавливаем curl для того, чтобы копировать и вставлять текст в командную строку. В VM нажимаем Устройства - Общий буфер обмена - Двунаправленный. Устройства - Функция Drag and Drop - Двунаправленный.
![Снимок 2](https://github.com/user-attachments/assets/f17c27b9-b3f5-4996-b85d-ae2436321811)

3. Скачиваем файл репозатория
![Снимок2](https://github.com/user-attachments/assets/db45030e-a36a-4aef-88c1-940081aac031)

4. Устанавливаем Docker Compose
![Снимок3](https://github.com/user-attachments/assets/ed679c89-c1b6-4a1e-9ca3-95d11d52e980)
![Снимок4](https://github.com/user-attachments/assets/e9a8333a-2c92-49e2-9f2f-f7ff3304623c)

5. Запускаем и разрешаем автозапуск
![Снимок5](https://github.com/user-attachments/assets/913211e4-f5d2-45c8-a49c-011821518a16)

6. Устанавливаем переменную COMVER. Grep находит последнюю версию
![Снимок 7](https://github.com/user-attachments/assets/990a8b72-9d95-4e16-9d6c-e7462c1c2b24)

7. Предоставление прав на выполнение файла docker-compose
![Предоставление прав на выполнение файла docker-compose](https://github.com/user-attachments/assets/71b15fb8-8e29-4086-9a1e-b90098ddc1b9)

8. Проверка версии Docker Compose
   ![Проверка установленной версии Docker Compose](https://github.com/user-attachments/assets/021afd35-a7c5-4fed-85b1-90300157c847)
   
9. Выкачиваем последнюю версию Docker Compose
![Снимок8 (2)](https://github.com/user-attachments/assets/35f4b2a0-d432-4a4e-be79-75002e50ffdb)

10. Проверка версии Docker Compose
![Проверка установленной версии Docker Compose](https://github.com/user-attachments/assets/511e22be-e301-4653-be12-83809b6bd2bf)

11. Установка git
![install git](https://github.com/user-attachments/assets/5f2bb5b7-d77f-40c8-825f-347996132660)

12. Создание папки с проектом
![git clone 256](https://github.com/user-attachments/assets/34de07e6-5f30-4905-8df3-b8fb6bcd951d)

13. Переходим в папку cd grafana_stack_for_docker
![Снимок2](https://github.com/user-attachments/assets/9e0e968b-590e-45e1-9962-94f1eba3a0df)

14. Создаем все необходиые директории sudo mkdir -p /mnt/common_volume/swarm/grafana/config
![Снимок3](https://github.com/user-attachments/assets/c8a14b4c-6978-4a57-b3cf-26f37666f5ca)

15. Создаем директории grafana-config, grafana-data, и prometheus-data внутри /mnt/common_volume/grafana/
![Создаем три директории grafana](https://github.com/user-attachments/assets/e333b1df-10a5-4613-a108-c6132ce354d2)

16. Даем права пользователю sudo chown -R $(id -u):$(id -g) {/mnt/common_volume/swarm/grafana/config,/mnt/common_volume/grafana}
![Снимок4](https://github.com/user-attachments/assets/16472bfc-5904-47c0-960b-9ae3722fbd9f)

17. Файл grafana.ini уже существует, команда touch /mnt/common_volume/grafana/grafana-config/grafana.ini обновит его временные метки (время последнего доступа и изменения). Если файл не существует, команда создаст новый пустой файл с указанным именем по указанному пути.
![Снимок5](https://github.com/user-attachments/assets/e78e70d3-0337-4dc1-832e-82a28971a703)

18. Команда cp config/* /mnt/common_volume/swarm/grafana/config/ копирует все файлы и подкаталоги из директории config в директорию /mnt/common_volume/swarm/grafana/config/
![Снимок6](https://github.com/user-attachments/assets/1df5ed62-a158-47fb-961b-1061ce6601b5)

19. Переименовываем файл grafana.yaml в docker-compose.yaml командой mv grafana.yaml docker-compose.yaml
![переименовали](https://github.com/user-attachments/assets/708d0db7-de2a-4c89-9ce5-542ee6c9e259)

20. Проверяем где мы находимся командой ls
![Снимок14](https://github.com/user-attachments/assets/0dac4392-d45f-4bc8-b509-396e4f481e86)

21. cd grafana_stack_for_docker/ для перехода в папку (забыл скрин)

22. sudo docker compose up -d создает и запускает контейнеры в фоновом режиме
![up -d](https://github.com/user-attachments/assets/2f1acfa5-b5a1-4623-877b-3088b72e6281)

23. Останавливаем процесс sudo docker compose stop. При написанни через дефис - ошибка. Решение: пишем через пробел.
![0](https://github.com/user-attachments/assets/3e7530ac-b74e-4cf3-89f1-9ac5f7ed4fbe)

Останавливаем процесс с удалением  файлов sudo socker compose dowm
![1](https://github.com/user-attachments/assets/b11ba872-c023-4470-bed8-193c81987ce5)



