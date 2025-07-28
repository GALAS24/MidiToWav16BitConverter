# Шрифты для ImGui

## ProggyClean.ttf
Моноширинный шрифт по умолчанию для ImGui.
- Уже встроен в ImGui
- Хорошо читается в малых размерах
- Подходит для технических интерфейсов

## DroidSans.ttf (опционально)
Более современный шрифт для улучшения внешнего вида.
- Скачать: Google Fonts или Android SDK
- Размер: ~190KB
- Поддерживает Unicode

## Использование в коде:

```cpp
ImGuiIO& io = ImGui::GetIO();

// Загружаем дополнительный шрифт
ImFont* font = io.Fonts->AddFontFromFileTTF(
    "assets/fonts/DroidSans.ttf", 
    16.0f
);

// Использование в интерфейсе
ImGui::PushFont(font);
ImGui::Text("Текст специальным шрифтом");
ImGui::PopFont();
```

Если файлы шрифтов отсутствуют, ImGui будет использовать встроенный шрифт.
