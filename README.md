# Справочник препаратов (Акнекутан · Аквамарис · Оптинол)

Приложение на Capacitor: веб-интерфейс в `www/` + нативные оболочки Android и iOS.
Функции: карточки препаратов с составом и инструкцией, калькулятор дозы Акнекутана,
подбор Аквамарис по возрасту, напоминания-будильники (Оптинол), аптеки Москвы, форма о нежелательных явлениях.

## Получить APK без установки Android Studio (через GitHub)
1. Создайте бесплатный аккаунт на github.com и новый репозиторий.
2. Загрузите в него всё содержимое этой папки (кнопка Add file → Upload files; папка `.github` тоже).
3. Откройте вкладку Actions → «Build Android APK» → Run workflow (≈5–8 минут).
4. Скачайте `app-debug-apk` из результатов → внутри `app-debug.apk`. Перекиньте на телефон и установите
   (разрешите установку из неизвестных источников).

## Локально
```
npm install
npx cap add android
npx cap sync android
cd android && ./gradlew assembleDebug      # нужен Android SDK + JDK 17
```
APK: `android/app/build/outputs/apk/debug/app-debug.apk`

## iPhone / iOS
Нужен Mac с Xcode и аккаунт Apple Developer:
```
npx cap add ios && npx cap sync ios && npx cap open ios
```
Дальше Product → Archive → TestFlight / App Store.

## Свои фотографии препаратов
Положите файлы `aknekutan.jpg`, `aquamaris.jpg`, `optinol.jpg` в `www/img/` — они заменят нарисованные значки.
