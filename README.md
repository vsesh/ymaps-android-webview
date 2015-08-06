# ymaps-android-webview
Пример проекта Android Studio, который использует API Яндекс.Карт во WebView.

# Развёртывание
1. Склонируйте проект.
2. Откройте проект в последней версии Android Studio.

# Использование
При использовании API Яндекс.Карт во WebView необходимо передавать HTTP заголовок Referer (https://ru.wikipedia.org/wiki/HTTP_referer) вида "http://<идентификатор вашего приложения в Google Play>".

Пример: *http://ru.yandex.api.yandexmapswebviewexample.ymapapp*

Чтобы WebView содержал заголовок "HTTP Referer",  необходимо использовать метод loadDataWithBaseURL (http://bit.ly/1hlaw1G).

Не забудьте добавить разрешение на использование интернета в разрешения своего приложения.

*< uses-permission android:name="android.permission.INTERNET" />*
