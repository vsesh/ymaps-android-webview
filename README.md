# ymaps-android-webview
Пример проекта Android Studio, который использует API Яндекс.Карт во WebView.

# Развёртывание
1. Склонируйте проект.
2. Откройте проект в последней версии Android Studio.

# Использование
При использовании API Яндекс.Карт во WebView необходимо передавать HTTP заголовок <a href="https://ru.wikipedia.org/wiki/HTTP_referer" target=_blank>Referer</a> вида "http://<идентификатор вашего приложения в Google Play>".

Пример: 
<pre>http://ru.yandex.api.yandexmapswebviewexample.ymapapp</pre>

Чтобы <a href="https://github.com/vsesh/ymaps-android-webview/blob/master/project/app/src/main/java/me/vsesh/ymaps_android_webview/ymaps_android_webview/MainActivity.java#L34">WebView</a> содержал заголовок "HTTP Referer",  необходимо использовать метод <a href="http://developer.android.com/reference/android/webkit/WebView.html#loadDataWithBaseURL(java.lang.String, java.lang.String, java.lang.String, java.lang.String, java.lang.String" target=_blank>loadDataWithBaseURL</a>.

Не забудьте добавить разрешение на использование интернета в <a href="https://github.com/vsesh/ymaps-android-webview/blob/master/project/app/src/main/AndroidManifest.xml">разрешениях</a> своего приложения:
<pre>&#60;uses-permission android:name="android.permission.INTERNET" /&#62;</pre>

Ключевые моменты:
* <a href="https://github.com/vsesh/ymaps-android-webview/blob/master/project/app/src/main/java/me/vsesh/ymaps_android_webview/ymaps_android_webview/MainActivity.java#L34">WebView</a>
* <a href="https://github.com/vsesh/ymaps-android-webview/blob/master/project/app/src/main/assets/index.html">Страница, которая открывается во WebView</a>
* <a href="https://github.com/vsesh/ymaps-android-webview/blob/master/project/app/src/main/AndroidManifest.xml">Разрешения приложения</a>
