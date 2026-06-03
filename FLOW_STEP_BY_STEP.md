# 🎬 Пошаговая инструкция в Google Flow — как сделать ролик по системе v2

> Для тех, кто создаёт **и кадры, и анимацию прямо в Google Flow** (Nano Banana Pro = картинки, Veo 3.1 = видео), а потом собирает в CapCut.
> Пример — ролик «Octopus / Other Minds», но шаги одинаковы для любой темы.

## Кто что делает (разделение труда)

| Где | Что делаем |
|---|---|
| **Google Flow** | 1) генерим кадры (Nano Banana Pro), 2) анимируем и **связываем сцены** (Veo 3.1 через start/end frame) |
| **ElevenLabs** | озвучка (голос-контральто, теги v3) |
| **CapCut** | сборка клипов, грейд/LUT, зерно, **мелкая типографика (тикеры/кикеры)**, аудио-микс, мастер |

Главное правило системы v2: **стиль лочим один раз картинками-референсами, сцены связываем через start/end frame, крупный текст НЕ пишем в кадре — он мелкий и только в CapCut.**

---

## ШАГ 0. Создать проект в Flow

1. Зайти на **flow.google** → **New project**.
2. В окне промпта справа выставить:
   - **Aspect ratio: 9:16** (вертикаль — обязательно для TikTok).
   - **Model:** для картинок — **Nano Banana Pro** (по умолчанию), для видео — **Veo 3.1**.
   - **Outputs:** 2–4 (чтобы было из чего выбрать).
3. Все генерации копятся в проекте — это и есть твоя «полка» с кадрами и клипами.

---

## ШАГ 1. Style DNA Kit — залочить единый стиль (генерим 4 картинки ОДИН раз)

> Это то, что делает все 18 сцен «одним фильмом». Без этого стиль будет плавать.

В режиме картинки (model = **Nano Banana Pro**, выключи Veo) сгенерируй 4 эталона. Для каждого: впиши промпт → **Generate** → выбери лучший → он сам сохранится в проекте как ассет.

1. **palette_plate** — промпт:
   > `Abstract style plate, deep abyssal ocean black, bioluminescent teal glow #1FB6C9, warm octopus-ochre skin tones #9C5A3C, chromatophore violet #6E2A4D pulses, chrome-glass highlights, water caustics shimmer, fine cinematic film grain, anamorphic 35mm, shallow depth of field, low-key chiaroscuro. No text.`
2. **lighting_plate** — промпт:
   > `Lighting reference plate, single caustic god-ray of light from the surface above piercing deep dark water, teal bioluminescent secondary glow, everything else void-black, cinematic low-key, anamorphic 35mm, film grain. No text.`
3. **creature_sheet** (герой — осьминог, самое важное) — промпт:
   > `Character reference sheet of one octopus on a plain dark background: 3 angles — full body, close-up of one eye with horizontal dumbbell pupil, close-up of one arm with suckers. Consistent ochre skin with chromatophores, teal neural glow. Cinematic, plain background. No text.`
4. **motif_sheet** — промпт:
   > `Reference sheet of recurring motifs on plain dark background: a sucker close-up, a single octopus eye, a thin teal bioluminescent neural thread, aquarium glass with a faint human handprint, a forking evolutionary tree line, a cluster of pearl-like eggs. No text.`

> Совет Flow: референсы лучше работают на **чистом/тёмном фоне** без лишних объектов. Если осьминог на creature_sheet получился «гуляющим» по цвету — перегенери, пока 3 ракурса не станут одинаковыми. Это твой канон героя.

---

## ШАГ 2. Сгенерировать 18 кадров — с reference-lock (ingredients)

Теперь для **каждой сцены** делаем кадр, подавая Style DNA Kit как **ingredients** (референсы). Тогда палитра/свет/герой будут одинаковыми во всех 18.

Для каждой сцены (model = **Nano Banana Pro**, 9:16):

1. Под промптом нажми **Add** (или перетащи в окно, или впиши **`@`** и выбери ассет) → добавь **ingredients**: `palette_plate`, `lighting_plate`, `creature_sheet` (и `motif_sheet`, если в сцене есть мотив).
2. Впиши **короткий** промпт сцены (не переписывай весь стиль — его несут референсы). Пример для **SCENE 1**:
   > `Match the palette, grain, caustic light and depth of field of the references. Keep the octopus identical to the creature sheet. Compose: extreme close-up of a single octopus eye emerging from abyssal black, faint aquarium glass with a human handprint at lower-left, teal catch-light in the pupil. Empty void space top and bottom. No text, no letters, no numbers.`
3. **Generate** → выбери лучший кадр. Сохрани/переименуй его понятно: `still_S1`.
4. Повтори для всех 18 сцен — бери **NBP-промпты прямо из** `OCTOPUS_OTHER_MINDS_V2.md` (раздел «18 SCENES», строка **NBP Still**). Каждый промпт там уже написан под reference-lock.

> Итог шага: 18 кадров `still_S1 … still_S18`, все в одном стиле, с одним и тем же осьминогом.

---

## ШАГ 3. Анимировать и СВЯЗАТЬ сцены — Veo 3.1 через start/end frame

> Это и есть «соединять сцены между собой». Секрет: **конец клипа сцены N = начало клипа сцены N+1** (один и тот же кадр). Тогда стыка не видно — сцена перетекает в сцену.

Переключи model на **Veo 3.1**, 9:16. Для **каждой** сцены:

1. **+ Add start frame** → перетащи `still_S{N}` (кадр этой сцены).
2. **+ Add end frame** → перетащи `still_S{N+1}` (кадр следующей сцены — цель перехода).
3. В промпте опиши **движение и переход** — бери его из `OCTOPUS_OTHER_MINDS_V2.md`, строка **Veo 3.1 (chaining)**. Пример для **SCENE 1**:
   > `The pupil slowly dilates, a caustic ray drifts across the eye; over 5 seconds the camera gently pulls back so the eye becomes one point in a wider darkness; a single violet pulse ripples across the skin. Slow, hushed, intimate.`
4. **Generate** → выбери лучший дубль → сохрани `clip_S1`.

**Таблица связки (так выглядит вся цепочка):**

| Клип | start frame | end frame | промпт перехода берём из |
|---|---|---|---|
| clip_S1 | still_S1 | still_S2 | Veo-строка SCENE 1 |
| clip_S2 | still_S2 | still_S3 | Veo-строка SCENE 2 |
| clip_S3 | still_S3 | still_S4 | … |
| … | … | … | … |
| clip_S17 | still_S17 | still_S18 | Veo-строка SCENE 17 |
| clip_S18 | still_S18 | *(без end frame)* | финальный уход в темноту |

> **Хард-каты** (без перетекания) делаем только на 3 сценах: **S10→S11, S13→S14, S16→S17**. Для них в clip_S10 / clip_S13 / clip_S16 можно НЕ ставить end frame (или поставить тот же кадр), а резкий стык собрать уже в CapCut. Так задумано в библии — это смысловые удары.

**Про длину клипа:** Flow генерит ~8 сек. Нам надо **5 сек на сцену** — просто подрежешь в CapCut (Шаг 5). Если сцена должна быть длиннее/плавнее — клик по клипу → **Extend** → допиши продолжение.

> Если хочешь, чтобы сцена «держалась» дольше перед переходом, а не морфилась все 5 сек: добавь только **start frame** (без end), опиши лёгкое движение «на месте», а сам переход к следующей сцене сделай коротким кросс-морфом или склейкой в CapCut. Но базовый путь (start+end) — самый плавный.

---

## ШАГ 4. (Опц.) Голос и вариации в Flow

- **Вариации:** включи **Agent** в окне промпта и попроси, напр. `Give me 4 variations of this with different camera moves` — выберешь лучшую.
- **Голос:** Flow умеет голос-референс через `@Voice: Имя`, **но только в генерациях с ingredients**. Для нашей серии озвучку всё равно лучше делать в **ElevenLabs v3** (контральто, stability 35 / style 40, шёпот на S17–S18) — настройки в `OCTOPUS_OTHER_MINDS_V2.md`.

---

## ШАГ 5. Скачать 18 клипов и собрать в CapCut

1. Скачай все `clip_S1 … clip_S18` из Flow (9:16, 1080×1920).
2. В CapCut по порядку на дорожку V1; каждый **подрежь до 5 сек** → всего 90 сек.
3. Импортируй WAV-озвучку из ElevenLabs на A1, выровняй каждую реплику по своей сцене.
4. **LUT «Abyss»** на весь V1 (давим чёрный, тянем teal в тени, кожа тёплая).
5. **Один проход зерна** (10%) + лёгкий caustic-shimmer на весь тайм-лайн (не по клипам!) + виньетка 15%.
6. Хард-каты на S10→S11, S13→S14, S16→S17. Остальное уже перетекает само (мы связали через frames).
7. **Мелкая типографика** на V2: тикеры-цитаты (JetBrains Mono ~22pt, opacity 55%) и кикеры (Inter Light italic ~26–28pt). **Никаких крупных заголовков Druk Wide в самом видео** — тексты берём из библии (строка «CapCut (minimal)» каждой сцены).
8. Аудио-микс по 7 дорожкам (см. библию), проверь тишину/дропы на S11/S13/S17.
9. **Мастер:** 1080×1920, 30 fps, H.264, −14 LUFS, −1 dBTP, ≤50 MB.

---

## ⚡️ Главные советы по Flow (чтобы не мучиться)

- **Чистые ingredients:** референсы — на простом/тёмном фоне, без лишних объектов. Так модель лучше «склеивает» стиль.
- **Не противоречь сам себе:** текст промпта должен *дополнять* референсы, а не спорить с ними (если в референсе тёмный кадр — не пиши «bright daylight»).
- **Один и тот же осьминог:** всегда добавляй `creature_sheet` в ingredients для сцен с существом — иначе он будет менять вид.
- **Генерируй по 2–4 дубля** и выбирай — это нормально, с первого раза редко идеально.
- **История версий:** в Flow есть History panel — старые варианты не теряются, можно вернуться.
- **Брейншторм промптов:** можно скинуть кадр/идею в Gemini и попросить переписать промпт.

---

## ✅ Мини-чеклист «по шагам»

1. [ ] Проект 9:16, выбраны модели (NBP / Veo 3.1)
2. [ ] Сгенерён **Style DNA Kit** (4 картинки) — стиль залочен
3. [ ] 18 кадров `still_S1…S18` через **ingredients** (промпты из библии)
4. [ ] 18 клипов через **start frame + end frame** (связка N→N+1)
5. [ ] Хард-каты только S10→S11, S13→S14, S16→S17
6. [ ] Озвучка ElevenLabs v3
7. [ ] CapCut: LUT + зерно (один проход) + мелкие тикеры/кикеры + аудио-микс
8. [ ] Мастер −14 LUFS, ≤50 MB; обложка + капшен из библии
</content>
