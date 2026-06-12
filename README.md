# 2x2 Workout - Android App

Приложение для тренировок на Android, обёрнутое в WebView.

## Быстрый старт (сборка через GitHub Actions)

### Шаг 1: Создайте репозиторий на GitHub
1. Зайдите на [github.com](https://github.com) и создайте аккаунт (если нет)
2. Нажмите **New repository**
3. Назовите репозиторий `2x2-workout-android`
4. Нажмите **Create repository**

### Шаг 2: Загрузите файлы
1. На странице репозитория нажмите **"Add file" → "Upload files"**
2. Перетащите ВСЕ файлы из этой папки (или выберите через проводник)
3. Важно: загрузите ВСЮ структуру папок (app/, gradle/, .github/ и т.д.)
4. Нажмите **"Commit changes"**

### Шаг 3: Запустите сборку
1. Перейдите во вкладку **Actions**
2. Нажмите **"Build APK"** слева
3. Нажмите **"Run workflow"** → **"Run workflow"**
4. Ждите 3-5 минут

### Шаг 4: Скачайте APK
1. Когда сборка завершится (зелёная галочка), откройте её
2. Пролистайте вниз до раздела **Artifacts**
3. Скачайте **debug-apk** или **release-apk**
4. Распакуйте ZIP — внутри будет `app-debug.apk`

### Шаг 5: Установите на телефон
1. Перекиньте APK на телефон (Telegram, USB, облако)
2. На телефоне разрешите установку из неизвестных источников
3. Установите APK

---

## Структура проекта

```
2x2-workout-android/
├── .github/workflows/build.yml   # GitHub Actions конфигурация
├── app/
│   ├── build.gradle              # Конфигурация сборки
│   ├── src/main/
│   │   ├── AndroidManifest.xml   # Манифест приложения
│   │   ├── assets/
│   │   │   └── index.html        # Ваше HTML-приложение (замените!)
│   │   ├── java/com/workout/app/
│   │   │   └── MainActivity.java # Главная активность с WebView
│   │   └── res/
│   │       ├── layout/
│   │       │   └── activity_main.xml
│   │       ├── values/
│   │       │   ├── colors.xml
│   │       │   ├── strings.xml
│   │       │   └── themes.xml
│   │       └── mipmap-hdpi/
│   │           └── ic_launcher.png
├── gradle/wrapper/
│   └── gradle-wrapper.properties
├── build.gradle
├── settings.gradle
├── gradle.properties
├── gradlew
├── gradlew.bat
└── README.md
```

## Важно!

**Замените файл `app/src/main/assets/index.html`** на ваше HTML-приложение перед сборкой!

---

Если возникнут проблемы — создайте Issue в репозитории.
