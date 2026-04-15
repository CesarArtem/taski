# Базовый слой с Python 3.10
FROM python:3.10

# Рабочая директория в контейнере
WORKDIR /app

RUN pip install gunicorn==22.0.0

# Копируем файл зависимостей
COPY requirements.txt .

# Устанавливаем зависимости
RUN pip install -r requirements.txt --no-cache-dir

# Копируем весь код проекта
COPY . .

# Запускаем сервер разработки
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]
