# YouTube Preview Generator

## Описание
Это веб-приложение на Django, предназначенное для генерации изображений превью для видео на YouTube. Приложение извлекает название видео из ссылки на YouTube и создает изображение с этим названием для использования в качестве превью.

## Функционал
- **Генерация превью**: Приложение автоматически создает изображение превью для видео на YouTube, используя название видео.

## Методы REST API
1. **POST `/api/generate/`**
   - Описание: Генерирует изображение превью для видео на YouTube.
   - Параметры запроса:
     - `youtube_url` (строка): Ссылка на видео на YouTube.
   - Пример запроса:
     ```json
     {
       "youtube_url": "https://www.youtube.com/watch?v=your_video_id"
     }
     ```
   - Пример ответа:
     ```json
     {
       "success": true,
       "thumbnail_url": "http://your-app.com/media/thumbnails/your_video_title.jpg"
     }
     ```

## Postman Коллекция
- [Ссылка на Postman коллекцию](https://api.postman.com/collections/14852565-9b013a80-4f7d-420b-8d89-b4cb8500a2f6?access_key=PMAT-01HGF2F9PRT1FVVF0YDHHZZDJ3)

## Инструкция по развертыванию
1. Установите Docker и Docker Compose.
2. Склонируйте репозиторий: `git clone https://github.com/your-username/your-repo.git`
3. Перейдите в директорию проекта: `cd your-repo`
4. Создайте файл `.env` и установите необходимые переменные окружения (например, `DJANGO_SECRET_KEY`, `DEBUG`, и т.д.).
5. Скачайте образ Docker: `nablascom/cuda-pytorch`
6. Выполните команду: `docker-compose up -d`
7. Приложение будет доступно по адресу: `http://localhost:8000`

## Запуск для проверки Django проекта
```
python src/manage.py runserver
```
