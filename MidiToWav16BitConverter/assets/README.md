# Assets - Ресурсы проекта

Эта папка содержит ресурсы, необходимые для работы MIDI to 16-bit WAV конвертера.

## Содержимое папки:

### 1. demo.mid
Демонстрационный MIDI файл для тестирования конвертера.
- Содержит простую мелодию в стиле 16-битных игр
- Использует несколько инструментов (фортепиано, струнные, барабаны)
- Длительность: примерно 30 секунд

### 2. TimGM6mb.sf2
Компактный General MIDI SoundFont (около 6MB).
- Содержит базовый набор инструментов GM
- Оптимизирован для небольшого размера
- Совместим с FluidSynth
- Источник: MuseScore 1.3

### 3. fonts/
Папка со шрифтами для ImGui интерфейса:
- ProggyClean.ttf - моноширинный шрифт по умолчанию
- DroidSans.ttf - альтернативный шрифт

### 4. presets/
Папка с пресетами эффектов:
- snes.preset - настройки для SNES-стиля
- genesis.preset - настройки для Sega Genesis/Mega Drive
- gameboy.preset - настройки для Game Boy

## Где взять файлы:

### TimGM6mb.sf2:
- Скачать с: https://musical-artifacts.com/artifacts/1036
- Или установить пакет: `sudo apt install timgm6mb-soundfont`
- Путь в Ubuntu: `/usr/share/sounds/sf2/TimGM6mb.sf2`

### Создание demo.mid:
Можно создать в любом MIDI-секвенсоре (FL Studio, LMMS, MuseScore) или использовать готовый файл.

### Шрифты:
- ProggyClean встроен в ImGui
- DroidSans можно скачать как open-source шрифт

## Использование в коде:

```cpp
// Загрузка SoundFont
midiProcessor.loadSoundFont("assets/TimGM6mb.sf2");

// Конвертация демо-файла
midiProcessor.convertToWav("assets/demo.mid", "output.wav");

// Загрузка шрифта в ImGui
ImGuiIO& io = ImGui::GetIO();
io.Fonts->AddFontFromFileTTF("assets/fonts/DroidSans.ttf", 16.0f);
```
