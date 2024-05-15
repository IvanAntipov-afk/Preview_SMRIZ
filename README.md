# YouTube Preview Generator

## Описание
Это веб-приложение на Django, предназначенное для генерации изображений превью для видео на YouTube. Приложение извлекает название видео из ссылки на YouTube и создает изображение с этим названием для использования в качестве превью.

## Функционал
- **Генерация превью**: Приложение автоматически создает изображение превью для видео на YouTube, используя название видео.

## Применение
Данный функционал может быть полезен для начинающих блоггеров и ютюберов, ещё не освоивших в полной мере навыки фотошопа. Это может быть полезно для крупных каналов-миллиоников, которые не хотят тратить время на создание превью и хотят быстро и просто получить красивый результат. Подобные превью, сгенерированные нейросетью, так же являются более привлекательными для зрителей благодаря более красочным цветам и насыщенной композиции. Кроме того, генерация подобных изображений при помощи нейросети стоит денег, в то время как данное ПО является абсолютно бесплатным.

## Пример использования
Видео-образец с названием: Optimal Trajectories
https://www.youtube.com/watch?v=exQV2XrGFLA

Полученный результат при помощи веб-приложения:
![image](https://github.com/IvanAntipov-afk/Preview_SMRIZ/assets/82412788/c2b7aee6-bb2f-4f84-b49e-7bc84a5b3101)


## Методы REST API
1. **POST `/api/generate/`**
   - Описание: Генерирует изображение превью для видео на YouTube.
   - Параметры запроса:
     - `video_url` (строка): Ссылка на видео на YouTube.
   - Пример запроса:
     ```json
     {
       "video_url": "https://www.youtube.com/watch?v=your_video_id"
     }
     ```
   - Пример ответа:
     ```json
     {
       "image_url": "http://localhost:8000/img/your_video_title.jpg"
     }
     ```

## Инструкция по развертыванию
1. Установите Docker и Docker Compose.
2. Склонируйте репозиторий: `git clone https://github.com/your-username/your-repo.git`
3. Перейдите в директорию проекта: `cd your-repo`
4. Скачайте образ Docker: `nablascom/cuda-pytorch`
5. Выполните команду: `docker-compose up -d`
6. Приложение будет доступно по адресу: `http://localhost:8000`

## Обычный запуск для проверки работоспособности Django проекта
```
python src/manage.py runserver
```
