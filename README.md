# Script Editor

Простой редактор Qt Script (.qs) файлов на Qt 5.15 + C++, предназначенный для ручного редактирования скриптов и обмена ими с внешним приложением — Script Runner.

Редактор предоставляет минималистичный UI для просмотра, изменения и сохранения скриптов, а также включает встроенный UDP-сервер, который позволяет приложению-клиенту (например, [Script Runner](https://github.com/sova2022/ScriptRunner)) удалённо запросить текущий открытый скрипт.

# Зависимости

- **Qt 5.15** (MSVC 2019, 64-bit)  
- **Visual Studio 2019 Build Tools**  

# Сборка:

```bash
git clone https://github.com/sova2022/ScriptEditor.git
```

Открыть проект:
ScriptEditor.sln в Visual Studio 2019.

В выпадающих списках выбрать конфигурацию:
Debug | x64 или Release | x64

Нажать Local Windows Debugger (зелёная кнопка «▶»).
Приложение запустится непосредственно из среды разработки.

# Запуск:

Запуск без Visual Studio (после деплоя)

Чтобы приложение запускалось на любом ПК без установленного Qt и Visual Studio, необходимо выполнить Qt Deployment:

Соберите проект в Release:
Release | x64

Выполните деплой через windeployqt:
windeployqt.exe ScriptEditor.exe

пример:
```cmd
C:\Qt5\5.15.0\msvc2019_64\bin\windeployqt.exe --release D:\C++\ScriptEditor\x64\Release\ScriptEditor.exe
```

После этого в папку с ScriptEditor.exe будут добавлены все необходимые Qt-библиотеки (Qt5Core.dll, Qt5Widgets.dll, платформенные плагины, styles и т.д.).

# Запуск программы

После деплоя приложение запускается обычным двойным кликом:

ScriptEditor.exe
