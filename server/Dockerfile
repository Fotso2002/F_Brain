FROM python:3.11-slim

ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

WORKDIR /app

# Install dependencies first
RUN pip install --upgrade pip \
    && pip install --no-cache-dir django \
    && pip install --no-cache-dir djangorestframework

# Copy code AFTER installing dependencies
COPY . .

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
