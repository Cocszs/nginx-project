# NGINX Configuration Project

Учебный проект по установке и настройке веб-сервера NGINX. Включает базовые примеры конфигураций, настройку виртуальных хостов и раздачу статических файлов.

## Описание проекта
Этот проект демонстрирует:
- структуру конфигурационных файлов NGINX
- базовый server block
- раздачу статического сайта
- проксирование запросов (reverse proxy)
- структуру репозитория

## Установка и запуск

### 1. Установка NGINX (Ubuntu)
```sudo apt updat```
sudo apt install nginx

### Проверка статуса NGINX
```systemctl status nginx```

### 2. Проверка конфигурации
```sudo nginx -t```

### 3. Перезапуск NGINX
```sudo systemctl restart nginx```

## Структура репозитория
```
nginx-project/
│── nginx.conf               # Основной конфигурационный файл NGINX
│── README.md                # Документация проекта
│
├── sites-available/
│     └── example.conf       # Конфигурация виртуального хоста
│
├── sites-enabled/
│     └── example.conf       # Активированная конфигурация (копия)
│
└── html/
      └── index.html         # Статическая веб-страница 
      ```
### 4.Пример базового server block 
```
server {
 listen 80;
 server_name localhost;
 root /var/www/nginx-project/html;
 index index.html;
 location / {
  try_files $uri $uri/ =404;
    }
}
```
### 5.Пример URL 
```http://localhost```
### 6.Технические требования 
NGINX: 1.18+

ОС: Ubuntu / Linux / WSL / macOS

Текстовый редактор: VS Code

Дополнительно:

Git

GitHub-аккаунт
