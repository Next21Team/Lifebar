# Lifebar

_[English](README.md) | **Русский**_

![Lifebar](images/lifebar.jpg)

AMX Mod X плагин для Counter-Strike.

Плагин добавляет полоску жизни над игроками.

## Настройки
### Квары
- ```lifebar_team "0"``` Лайфбар отображается над всеми игроками, 1 — только над союзниками, 2 — только над противниками.
- ```lifebar_alive "0"``` Лайфбар отображается в любом состоянии игрока, 1 — только в живом, 2 — только в мертвом.
- ```lifebar_max_health "100"``` Максимальное здоровье игрока для 100% состояния лайфбара.

### Определения
Конфигурация производится в файле исходного кода:
```c
// #define COLORED_LIFEBAR // Использовать цветной лайфбар (раскомментировать для поддержки цветов)
#define COLOR_RED Float: { 255.0, 0.0, 0.0 } // Цвет лайфбара для команды террористов
#define COLOR_BLUE Float: { 0.0, 0.0, 255.0 } // Цвет лайфбара для команды контр-террористов
#define LIFEBAR_RENDERMODE kRenderTransTexture
#define LIFEBAR_RENDERAMT 255.0
#define LIFEBAR_SCALE 0.2 // Размер лайфбара

// Модель лайфбара (sprites/next21_efk/lifebar_numeric.spr для цифрового)
new const MODELS_LIFEBAR[2][] = {
	"sprites/next21_efk/lifebar_numeric.spr", // для команды террористов
	"sprites/next21_efk/lifebar_numeric.spr" // для команды контр-террористов
}
```

![Lifebar](images/lifebar2.jpg)

## Авторы
- [Psycrow](https://github.com/Psycrow101)
