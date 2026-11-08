# Caesar Spine Rig & Pop-Squash Setup (Цезарь — Персонаж 1)

> 📌 **Глобальные правила всех ИИ:** [F:\AI\GLOBAL_RULES.md](file:///F:/AI/GLOBAL_RULES.md)

## 1. Содержимое комплекта Spine (Вариант А)

- **`caesar.json`** — скелет Spine 3.8 (версия 3.8.99), содержащий:
  - 12 костей: `root`, `torso`, `head`, `wing_L`, `wing_L_tip`, `wing_R`, `wing_R_tip`, `leg_L`, `foot_L`, `leg_R`, `foot_R`, `pouch`.
  - Единый деформируемый меш `caesar_base`: 55 вершин (22 контур hull + 33 интерьерных), 86 треугольников с привязкой весов (Weights/Skinning).
  - Анимация `idle` (мягкое дыхание).
  - Анимация `pop_squash` (быстрый упругий переход 0.10с: $1.0 \rightarrow 1.28 \times 0.72 \rightarrow 0.92 \times 1.12 \rightarrow 1.0$).
- **`caesar_rig_wireframe.png`** — визуальная схема триангуляции сетки и иерархии костей.
- **`images/`** — папка исходных изображений:
  - `caesar_base.png` (основной меш стойки).
  - `sq_01_crawl_flat.png` ... `sq_08_tube_shiver.png` (8 конгруэнтных зажатых состояний).
  - `flight_flapping.png`, `landing_flared.png`, `landing_crouch.png`.

---

## 2. Как открыть в Spine Editor (3.8 / 4.x)

1. Откройте **Spine Editor**.
2. В главном меню выберите **Spine** $\rightarrow$ **Импорт данных** (`Import Data`).
3. Выберите файл `assets/caesar_spine/caesar.json`.
4. В поле «Папка изображений» (`Images path`) укажите относительный путь `./images/` (или абсолютный `assets/caesar_spine/images/`).
5. Нажмите **Импорт**. Проект откроется с готовой иерархией костей, мешем и анимациями!
