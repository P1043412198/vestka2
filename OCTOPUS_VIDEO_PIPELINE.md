# 🐙 OCTOPUS — пошаговый гайд для новичка (90с TikTok, voice-first)

**Тема:** На Земле уже есть чужой разум — и его можно навестить в аквариуме. Осьминог отделился от нашей ветви ~600 млн лет назад и построил мышление с нуля: ~500 млн нейронов, две трети — в руках; каждая рука «думает» и пробует мир на вкус сама; он меняет цвет в мире, который не видит в цвете; редактирует собственный РНК-код; узнаёт лица. И живёт всего ~1–2 года: мать охраняет кладку, перестаёт есть и умирает к моменту, когда детёныши вылупляются — поэтому всё, что он узнаёт, он узнаёт сам и уносит с собой. (Godfrey-Smith 2016; Hochner 2012; Liscovitch-Brauer et al., Cell 2017; Finn et al., Current Biology 2009; Wang & Ragsdale 2018.)

**Длительность:** 90 секунд → 18 сцен. Каждая сцена = одна voice-фраза + один still + один 8-сек клип.
**Формат:** 9:16 vertical, 1080×1920 (native TikTok / Reels / Shorts).
**Voice:** делаешь в ElevenLabs v3 (голос — контральто, stability 35 / style 40, speed 1.0), ~90–95 сек. Это master timing track — клипы режутся под голос.

---

## 🎯 ЛОГИКА WORKFLOW (voice-first)

```
1. 🎙️ Сгенерить voice в ElevenLabs v3 (~90–95 сек) по скрипту ниже
2. ⏱️ Замерить тайминги — где какая фраза начинается/заканчивается
3. 🎨 Сгенерить scene_01_still в Nano Banana Pro → он становится CANONICAL GRADE (эталон серии)
4. 🖼️ Сгенерить 17 оставшихся stills в Nano Banana Pro (с references)
5. 🎥 Сгенерить 18 animations в Veo 3.1 (по 8 сек, с ingredients для grade lock)
6. 🎞️ Собрать в CapCut: 18 клипов на V1, voice на A2, обрезать каждый клип под voice-фразу
7. 📱 Export 1080×1920 → TikTok
```

**Никакого длинного видео.** 18 независимых .mp4 файлов по 8 сек. Каждый обрезается в CapCut до длины своей voice-фразы.

---

## 📚 СЛОВАРЬ — что значат термины (читать перед началом)

- **Still** — статичная картинка (одно изображение, .png).
- **Animation / clip** — короткое видео (.mp4), у нас 8 секунд каждое.
- **First frame** — стартовый кадр видео. В Veo 3.1 ты загружаешь картинку как first frame, и видео начинается ровно с неё.
- **Last frame (опц.)** — финальный кадр. Мы его НЕ используем — даём Veo свободу анимировать от first frame. (Связку «перетекание сцен» можно включить позже: end frame сцены = first frame следующей — см. примечание в конце.)
- **Ingredient** (Veo 3.1) — reference картинка, которую прикладываешь к промту. Veo принимает **до 3 ingredients** на генерацию. Это «стиль-якоря»: Veo копирует с них палитру, свет, текстуру, общий look. Это НЕ first frame.
- **Reference image** (Nano Banana Pro) — то же самое для генерации картинок. Прикладываешь 1–3 предыдущих stills, и новый still генерится в той же палитре.
- **Canonical grade reference** — твой эталонный кадр. У нас это `scene_01_still.png` (глаз осьминога). После одобрения прикрепляешь его **ко всем** последующим stills и animations. Серия выглядит как один фильм с одним грейдом.
- **Voice phrase** — одна фраза voice-over из ElevenLabs. На каждую сцену = одна фраза.
- **V1 / A1 / A2 / A3** — дорожки в CapCut. **V** = video, **A** = audio. V1 = главная видео-дорожка, A1 = аудио, прикреплённое к V1 (Veo native ambient), A2 = голос (ElevenLabs), A3 = sub-bass, A4 = music bed.
- **Sub-bass** — низкочастотный гул (30–40 Гц), даёт глубину океана. Берёшь sample из Splice / YouTube Audio Library.
- **LUFS** — стандарт громкости. TikTok = **−14 LUFS**.

---

## 🛠️ ЧТО НУЖНО ИМЕТЬ

- **Google Flow** (платный план — нужен для Nano Banana Pro + Veo 3.1)
- **ElevenLabs v3** — для voice
- **CapCut** (desktop версия предпочтительнее для precise timing)
- 1.5–3 часа на полный прогон (зависит от числа регенераций stills)

---

## 🎙️ СКРИПТ ДЛЯ ELEVENLABS (18 фраз, ~90 сек)

> Голос: женский контральто, интимный, почти шёпот. Settings: stability 35, style 40, speed 1.0. Теги в `[ ]` — для ElevenLabs v3.

```
1.  [inhale] [whispered, intimate] There is an alien intelligence on Earth. [breath] You can visit it in an aquarium.
2.  [narrator, low] It didn't come from space. [soft] It came from the same place we did — [whispered] and then went the other way.
3.  [low] Six hundred million years ago, our family tree split. [beat] On one side: us. [whispered] On the other — this.
4.  [soft] It built a mind from scratch. [whispered] Nothing like ours.
5.  [narrator] Half a billion neurons. [beat] But two-thirds of them are not in its head.
6.  [whispered] They're in its arms.
7.  [low] Each arm can taste what it touches. [soft] Each arm can decide on its own.
8.  [soft] It changes color [beat] to match a world it cannot even see in color.
9.  [narrator, low] It edits its own genetic code — [whispered] rewriting its nervous system faster than evolution should allow.
10. [soft] It opens jars. It solves mazes. [whispered] It remembers your face.
11. [beat] [low] And then — [whispered] it lives barely two years.
12. [soft] The mother lays her eggs, [breath] stops eating, [whispered] and guards them in the dark.
13. [low] She dies as they hatch. [whispered] She will never meet them.
14. [soft] So everything it learns, [beat] it learns alone. [whispered] And takes with it.
15. [low] We share an ancestor. [soft] That tiny, forgotten thing.
16. [narrator] From the same beginning, the universe built a mind — [whispered] twice.
17. [beat] [whispered, intimate] And one of them just watched you — [breath] through the glass.
18. [soft] It will never know [whispered] you wondered about it too.
```

---

## ⏱️ ШАГ 1 — РАЗМЕТИТЬ ТАЙМИНГИ ГОЛОСА (один раз в начале)

### Как замерить тайминги
1. Открой ElevenLabs voice mp3 в **CapCut → Import**.
2. На audio timeline (A2) увидишь волну.
3. Включи waveform (правый клик на трек → Show waveform).
4. Кликни на начало каждой voice-фразы, посмотри тайминг в playhead (сверху).
5. Запиши тайминги в таблицу ниже.

### Таблица таймингов (заполни сам после замера)

| Сцена | ENG line | ≈ Старт | ≈ Конец | Длина | Твой реальный старт | Твой реальный конец |
|---|---|---|---|---|---|---|
| 1 | "There is an alien intelligence on Earth. You can visit it in an aquarium." | 0:00 | 0:05.5 | ~5.5 с | _____ | _____ |
| 2 | "It didn't come from space. It came from the same place we did — and then went the other way." | 0:05.5 | 0:11.5 | ~6.0 с | _____ | _____ |
| 3 | "Six hundred million years ago, our family tree split. On one side: us. On the other — this." | 0:11.5 | 0:17.0 | ~5.5 с | _____ | _____ |
| 4 | "It built a mind from scratch. Nothing like ours." | 0:17.0 | 0:21.0 | ~4.0 с | _____ | _____ |
| 5 | "Half a billion neurons. But two-thirds of them are not in its head." | 0:21.0 | 0:26.5 | ~5.5 с | _____ | _____ |
| 6 | "They're in its arms." | 0:26.5 | 0:29.0 | ~2.5 с | _____ | _____ |
| 7 | "Each arm can taste what it touches. Each arm can decide on its own." | 0:29.0 | 0:34.5 | ~5.5 с | _____ | _____ |
| 8 | "It changes color to match a world it cannot even see in color." | 0:34.5 | 0:39.5 | ~5.0 с | _____ | _____ |
| 9 | "It edits its own genetic code — rewriting its nervous system faster than evolution should allow." | 0:39.5 | 0:45.5 | ~6.0 с | _____ | _____ |
| 10 | "It opens jars. It solves mazes. It remembers your face." | 0:45.5 | 0:51.0 | ~5.5 с | _____ | _____ |
| 11 | "And then — it lives barely two years." | 0:51.0 | 0:54.5 | ~3.5 с | _____ | _____ |
| 12 | "The mother lays her eggs, stops eating, and guards them in the dark." | 0:54.5 | 1:00.0 | ~5.5 с | _____ | _____ |
| 13 | "She dies as they hatch. She will never meet them." | 1:00.0 | 1:04.5 | ~4.5 с | _____ | _____ |
| 14 | "So everything it learns, it learns alone. And takes with it." | 1:04.5 | 1:09.5 | ~5.0 с | _____ | _____ |
| 15 | "We share an ancestor. That tiny, forgotten thing." | 1:09.5 | 1:14.0 | ~4.5 с | _____ | _____ |
| 16 | "From the same beginning, the universe built a mind — twice." | 1:14.0 | 1:19.0 | ~5.0 с | _____ | _____ |
| 17 | "And one of them just watched you — through the glass." | 1:19.0 | 1:24.5 | ~5.5 с | _____ | _____ |
| 18 | "It will never know you wondered about it too." | 1:24.5 | 1:30.0 | ~5.5 с | _____ | _____ |

> **Заметка:** если реальный voice длиннее/короче 90 сек — раскидай разницу по самым длинным сценам (2, 9, 18). Запиши реальные тайминги в правые колонки и используй их при сборке в CapCut.

---

## 🎨 ШАГ 2 — СГЕНЕРИТЬ CANONICAL GRADE REFERENCE (scene_01_still)

Это **самая важная** картинка во всём проекте. Она задаёт грейд / палитру / свет / grain для всех остальных 17 сцен. **Не торопись** — генерируй пока не получишь идеал.

### Что делаешь (детально, по клику)
1. Открой **Google Flow** → войди в аккаунт.
2. **New project** → назови `Octopus TikTok 90s`.
3. В левой панели создай **Collection** с тем же именем (все ассеты падают туда).
4. Вверху найди dropdown **Model** → **Nano Banana Pro**.
5. Aspect ratio → **9:16 (1080×1920)**.
6. **Reference images**: НИЧЕГО НЕ ПРИКЛАДЫВАЙ (это первая сцена, эталон ещё не существует).
7. В поле prompt вставь:

```
Extreme macro close-up of a single octopus eye with a horizontal dumbbell-shaped pupil, filling the upper-middle of a vertical frame, emerging from a pure deep abyssal void-black background. Between the viewer and the eye there is a faint sheet of aquarium glass with one soft human handprint smudge in the lower-left. A single soft caustic god-ray of light from the surface above catches the wet curve of the eye; a small bioluminescent teal catch-light glows inside the pupil; the warm octopus-ochre skin around the eye carries faint chromatophore-violet pulses. The rest of the frame falls into deep void-black. The composition is centered, intimate, almost sacred. Style: shot like a premium deep-sea / cephalopod-intelligence documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, a single soft caustic god-ray key light from the surface above, deep low-key chiaroscuro like the abyss at midnight. Mood blends Arrival alien-intelligence awe with BBC Blue Planet deep-sea and Under the Skin otherworldly stillness. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as the rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint moving water-caustic shimmer, slight chromatic aberration at frame edges. Avoid: no real human faces, no recognizable real people, no gore, no text artifacts.
```

8. **Generate** → Flow выдаст 4 варианта.
9. Выбери **самый кинематографичный** — где грейд «abyssal black + teal + ochre», композиция центрированная, grain виден, teal-блик в зрачке яркий.
10. **Если ни один не идеален** — **Regenerate** ещё раз (или подправь промт). Не жалей кредиты — это эталон.
11. Когда выбрал — **Download** → сохрани как **`scene_01_still.png`**.
12. В Flow Collection переименуй ассет → `scene_01_still`.

Теперь у тебя **canonical grade reference**. Со 2-й сцены ты ВСЕГДА прикладываешь его в Reference / Ingredients.

---

## 🧬 СИСТЕМА REFERENCE / INGREDIENT — что куда прикреплять

### A. Nano Banana Pro (генерация stills)
Поле: **Reference images** (кнопка `+` рядом с промтом). До 3 картинок.

### B. Veo 3.1 (генерация animations)
- **First frame** — обязательно. Твой `scene_NN_still.png`. С него начинается клип.
- **Ingredients** (кнопка `+` / "Add reference") — до 3 картинок-якорей стиля.

### Мастер-таблица для всех 18 сцен

| Scene | 🖼️ Nano Banana Pro — Reference images | 🎥 Veo 3.1 — First frame | 🎥 Veo 3.1 — Ingredients (до 3) |
|---|---|---|---|
| 1 | _(нет)_ | scene_01_still.png | _(нет)_ |
| 2 | scene_01_still | scene_02_still.png | scene_01_still |
| 3 | scene_01_still + scene_02_still | scene_03_still.png | scene_01_still + scene_02_still |
| 4 | scene_01_still + scene_03_still | scene_04_still.png | scene_01_still + scene_03_still |
| 5 | scene_01_still + scene_04_still | scene_05_still.png | scene_01_still + scene_04_still |
| 6 | scene_01_still + scene_05_still | scene_06_still.png | scene_01_still + scene_05_still |
| 7 | scene_01_still + scene_06_still | scene_07_still.png | scene_01_still + scene_06_still |
| 8 | scene_01_still + scene_07_still | scene_08_still.png | scene_01_still + scene_07_still |
| 9 | scene_01_still + scene_08_still | scene_09_still.png | scene_01_still + scene_08_still |
| 10 | scene_01_still + scene_09_still | scene_10_still.png | scene_01_still + scene_09_still |
| 11 | scene_01_still + scene_10_still | scene_11_still.png | scene_01_still + scene_10_still |
| 12 | scene_01_still + scene_11_still | scene_12_still.png | scene_01_still + scene_11_still |
| 13 | scene_01_still + scene_12_still | scene_13_still.png | scene_01_still + scene_12_still |
| 14 | scene_01_still + scene_13_still | scene_14_still.png | scene_01_still + scene_13_still |
| 15 | scene_01_still + scene_14_still | scene_15_still.png | scene_01_still + scene_14_still |
| 16 | scene_01_still + scene_15_still | scene_16_still.png | scene_01_still + scene_15_still |
| 17 | scene_01_still + scene_16_still | scene_17_still.png | scene_01_still + scene_16_still |
| 18 | scene_01_still + scene_17_still | scene_18_still.png | scene_01_still + scene_17_still |

### Правило простое:
- **К каждому стилу/клипу прикладывай ДВА файла:** `scene_01_still` (эталон серии) + предыдущий still (continuity).
- **Исключение:** Scene 1 — без рефов (он сам эталон). Scene 2 — только эталон.

### Усиливающая строка (уже вшита в каждый промт ниже):
```
Match the color palette, lighting, grain, and overall look of the attached reference images. Maintain visual continuity with the series.
```

---

## 🎬 ШАГ 3 — ГЕНЕРИРОВАТЬ 18 СЦЕН

> **Универсальный процесс для каждой сцены:**
> 1. Flow → Image → Nano Banana Pro → 9:16
> 2. Приложи reference картинки (см. таблицу выше)
> 3. Вставь Still prompt → Generate → выбери лучший → download как `scene_NN_still.png`
> 4. Flow → Video → Veo 3.1 → 9:16 → 8 sec
> 5. Загрузи `scene_NN_still.png` как **First frame**
> 6. Приложи ingredients (см. таблицу выше)
> 7. Вставь Animation prompt → Negative prompt в отдельное поле → Generate → download как `scene_NN_video.mp4`
> 8. Переходи к следующей сцене
>
> Negative prompt (одинаковый для всех 18 — копируй):
> ```
> no spoken voice, no dialogue, no speech, no text artifacts, no watermark, no logo, no aspect bars, no fast camera, no recognizable real human faces, no gore, no large on-screen text
> ```

---

### СЦЕНА 1 (≈ 0:00–0:05.5) — HOOK

**🎙️ Voice:** `[inhale] [whispered, intimate] There is an alien intelligence on Earth. [breath] You can visit it in an aquarium.`

**🖼️ Nano Banana Pro:**
- **Reference images:** _(нет)_
- **Prompt:**
```
Extreme macro close-up of a single octopus eye with a horizontal dumbbell-shaped pupil, filling the upper-middle of a vertical frame, emerging from a pure deep abyssal void-black background. Between the viewer and the eye there is a faint sheet of aquarium glass with one soft human handprint smudge in the lower-left. A single soft caustic god-ray of light from the surface above catches the wet curve of the eye; a small bioluminescent teal catch-light glows inside the pupil; the warm octopus-ochre skin around the eye carries faint chromatophore-violet pulses. The rest of the frame falls into deep void-black. The composition is centered, intimate, almost sacred. Style: shot like a premium deep-sea / cephalopod-intelligence documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, a single soft caustic god-ray key light from the surface above, deep low-key chiaroscuro. Mood blends Arrival alien-intelligence awe with BBC Blue Planet deep-sea and Under the Skin stillness. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no recognizable real people, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_01_still.png`
- **Ingredients:** _(нет)_
- **Prompt:**
```
0:00–0:01: Total abyssal black. A faint underwater ambient. The dim curve of the eye emerges from the void.
0:01–0:06: The pupil slowly dilates as a single caustic god-ray drifts across the wet eye; the bioluminescent teal catch-light brightens; a single chromatophore-violet pulse ripples once across the surrounding ochre skin. The camera gently, almost imperceptibly pulls back so the eye becomes one point in a wider darkness.
0:06–0:08: The handprint smudge on the glass catches the light for a moment, then the frame settles, holding the gaze.
Audio (no spoken voice): 0.5 sec of near silence, then deep abyssal sub-bass drone (~35 Hz), a soft distant whale-like tone, faint bubbling water ambient. No music.
Format: 9:16 vertical, 8 sec, low motion intensity.
```

**📝 CapCut overlay (мелко, на voice 0:01–0:05):** тикер снизу `GODFREY-SMITH · 2016` (JetBrains Mono ~22pt, opacity 55%). Без крупных надписей.

---

### СЦЕНА 2 (≈ 0:05.5–0:11.5)

**🎙️ Voice:** `[narrator, low] It didn't come from space. [soft] It came from the same place we did — [whispered] and then went the other way.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still`
- **Prompt:**
```
A deep abyssal void-black field. A single faint bone-cream hairline thread of light enters from the bottom center and travels upward, then forks into two diverging paths heading toward opposite top corners; empty void all around, vast negative space. A faint bioluminescent teal glow lines the threads; a single soft caustic god-ray from above. Match the color palette, lighting, grain, and overall look of the attached reference image; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_02_still.png`
- **Ingredients:** `scene_01_still`
- **Prompt:**
```
0:00–0:01: The single thread of light glows up from the lower edge.
0:01–0:06: The thread travels slowly upward and at ~0:03 splits into two diverging lines that drift apart toward opposite corners; gentle lateral parallax drift; teal glow shimmering along the lines; abyssal calm.
0:06–0:08: The two branches settle far apart, holding the split.
Audio (no spoken voice): sustained sub-bass drone, a soft sonar-like ping at the split moment, faint deep-water ambient.
Format: 9:16 vertical, 8 sec, low motion intensity.
```

**📝 CapCut overlay:** кикер `same origin` (Inter Light italic ~26pt, opacity 70%).

---

### СЦЕНА 3 (≈ 0:11.5–0:17)

**🎙️ Voice:** `[low] Six hundred million years ago, our family tree split. [beat] On one side: us. [whispered] On the other — this.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_02_still`
- **Prompt:**
```
A minimal Saul-Bass-style evolutionary fork on a deep abyssal void-black field: two thin bone-cream lines diverging from one node low-center; the left branch ends in a faint cold human-head silhouette, the right branch ends in a faint octopus silhouette; a single small blood-red dot glows at the fork node. A soft caustic god-ray from above, faint teal rim glow on the lines, vast negative space. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_03_still.png`
- **Ingredients:** `scene_01_still` + `scene_02_still`
- **Prompt:**
```
0:00–0:01: The red node at the fork glows up.
0:01–0:06: The two branches slowly draw outward from the node; the octopus-side branch brightens and the camera drifts gently toward it; the blood-red node pulses once at ~0:03.
0:06–0:08: The human silhouette dims into the void; the octopus side holds the light.
Audio (no spoken voice): low sub-bass swell, a single resonant low chime at the red pulse, deep-water ambient.
Format: 9:16 vertical, 8 sec, low motion intensity.
```

**📝 CapCut overlay:** тикер `~600 MILLION YEARS · LAST COMMON ANCESTOR` (~22pt, opacity 55%). Число несёт расходящееся древо, не крупный текст.

---

### СЦЕНА 4 (≈ 0:17–0:21)

**🎙️ Voice:** `[soft] It built a mind from scratch. [whispered] Nothing like ours.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_03_still`
- **Prompt:**
```
A full octopus suspended in deep abyssal void-black, body in soft focus, with a faint bioluminescent teal neural glow tracing diffusely through its whole form like a living map; a single soft caustic god-ray key light from above; warm octopus-ochre skin with faint chromatophore-violet pulses; vast negative space above and below. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_04_still.png`
- **Ingredients:** `scene_01_still` + `scene_03_still`
- **Prompt:**
```
0:00–0:01: The octopus hangs still in the dark, teal glow faint.
0:01–0:06: The teal neural glow slowly intensifies and concentrates, then begins to migrate outward toward the arms; the octopus drifts and rotates a few degrees; caustic light ripples over its skin. Slow, awe.
0:06–0:08: The glow settles spread across the whole body, holding.
Audio (no spoken voice): rising sub-bass drone, soft ethereal pad-like tone, water ambient.
Format: 9:16 vertical, 8 sec, low motion intensity.
```

**📝 CapCut overlay:** кикер `a different kind of mind` (Inter Light italic ~26pt, opacity 70%).

---

### СЦЕНА 5 (≈ 0:21–0:26.5)

**🎙️ Voice:** `[narrator] Half a billion neurons. [beat] But two-thirds of them are not in its head.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_04_still`
- **Prompt:**
```
An octopus arranged so the small central brain region glows a faint but DIM bioluminescent teal, while a vast diffuse cloud of teal points spreads down into the eight arms — visually obvious that most of the glow is NOT in the head. Austere, diagram-like, on deep abyssal void-black; single soft caustic god-ray from above; warm ochre skin. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_05_still.png`
- **Ingredients:** `scene_01_still` + `scene_04_still`
- **Prompt:**
```
0:00–0:01: The dim head-glow holds steady.
0:01–0:06: The arm-glow swells and brightens dramatically over the next seconds, teal points multiplying down the arms; a subtle camera push toward the arms; the head stays dim by contrast.
0:06–0:08: The arms blaze with distributed teal light, the head a small dim dot.
Audio (no spoken voice): sub-bass pulse that spreads outward, soft shimmering high partials, water ambient.
Format: 9:16 vertical, 8 sec, low motion intensity.
```

**📝 CapCut overlay:** тикер `~500,000,000 NEURONS · HOCHNER 2012` (~22pt, opacity 55%). Долю несёт распределение свечения.

---

### СЦЕНА 6 (≈ 0:26.5–0:29) — REVEAL

**🎙️ Voice:** `[whispered] They're in its arms.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_05_still`
- **Prompt:**
```
Extreme close-up of a single octopus arm curling toward camera, suckers in sharp focus, bright bioluminescent teal neural threads running visibly along the arm's length; warm ochre skin with faint violet pulses; the rest falling into deep abyssal void-black; single soft caustic god-ray from above. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_06_still.png`
- **Ingredients:** `scene_01_still` + `scene_05_still`
- **Prompt:**
```
0:00–0:01: The arm hangs, threads dim.
0:01–0:06: The arm coils with independent, searching motion; teal threads pulse along it like firing neurons; a single sucker reaches toward a point of light. Confident reveal.
0:06–0:08: The sucker settles near the light, threads glowing.
Audio (no spoken voice): a sharp low sub-bass accent on the reveal, organic wet movement foley, water ambient.
Format: 9:16 vertical, 8 sec, low-medium motion intensity.
```

**📝 CapCut overlay:** кикер `the arms think` (Inter Light italic ~26pt, opacity 75%, kinetic type-in на «think»).

---

### СЦЕНА 7 (≈ 0:29–0:34.5)

**🎙️ Voice:** `[low] Each arm can taste what it touches. [soft] Each arm can decide on its own.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_06_still`
- **Prompt:**
```
Macro of one octopus sucker pressed against a pale chrome-glass surface; from the contact point faint bone-cream concentric "taste" ripples bloom outward; a bioluminescent teal micro-glow inside the sucker rim; warm ochre skin; deep abyssal void-black around; single soft caustic god-ray from above. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_07_still.png`
- **Ingredients:** `scene_01_still` + `scene_06_still`
- **Prompt:**
```
0:00–0:01: The sucker hovers just off the glass.
0:01–0:06: The sucker presses and releases; faint bone-cream taste-ripples bloom at the contact point at ~0:01 and ~0:03; the touched glass surface begins shifting hue toward teal; slow drift.
0:06–0:08: The sucker eases off, a final ripple fading.
Audio (no spoken voice): soft suction foley, delicate high "taste" shimmer, sub-bass drone, water ambient.
Format: 9:16 vertical, 8 sec, low motion intensity.
```

**📝 CapCut overlay:** тикер `VAN GIESEN ET AL. · CELL · 2020` (~22pt, opacity 55%).

---

### СЦЕНА 8 (≈ 0:34.5–0:39.5)

**🎙️ Voice:** `[soft] It changes color [beat] to match a world it cannot even see in color.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_07_still`
- **Prompt:**
```
A patch of octopus skin filling the frame, chromatophores mid-shift — warm ochre, chromatophore-violet and bioluminescent teal blooming across the surface in an organic stipple of tiny pigment cells; soft caustic light from above; deep abyssal void-black at the edges. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_08_still.png`
- **Ingredients:** `scene_01_still` + `scene_07_still`
- **Prompt:**
```
0:00–0:01: The skin rests, pigment cells still.
0:01–0:06: Waves of color ripple across the skin (chromatophores firing) — ochre to violet to teal — mesmerizing and slow over the full span.
0:06–0:08: Near the end the color pattern resolves into faint thread-like lines, hinting at the next scene.
Audio (no spoken voice): soft tonal sweeps that follow the color waves, sub-bass drone, water ambient.
Format: 9:16 vertical, 8 sec, low-medium motion intensity.
```

**📝 CapCut overlay:** кикер `colorblind` (Inter Light italic ~26pt, opacity 70%).

---

### СЦЕНА 9 (≈ 0:39.5–0:45.5)

**🎙️ Voice:** `[narrator, low] It edits its own genetic code — [whispered] rewriting its nervous system faster than evolution should allow.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_08_still`
- **Prompt:**
```
An abstract bone-cream and bioluminescent teal double-helix-like strand floating in deep abyssal void-black, with several rungs glowing and visibly re-arranging (implied RNA / gene editing) — abstract, not literal, no real molecules. Single soft caustic god-ray from above; faint chromatic aberration. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_09_still.png`
- **Ingredients:** `scene_01_still` + `scene_08_still`
- **Prompt:**
```
0:00–0:01: The strand floats, rungs steady.
0:01–0:06: Rungs of the strand flicker and swap positions as if being edited; the strand slowly coils tighter; faint chromatic aberration shimmers at the edges.
0:06–0:08: The strand dissolves toward a single point of teal light.
Audio (no spoken voice): glitchy soft digital-organic ticks, sub-bass drone, water ambient.
Format: 9:16 vertical, 8 sec, low motion intensity.
```

**📝 CapCut overlay:** тикер `LISCOVITCH-BRAUER ET AL. · CELL · 2017` (~22pt, opacity 55%).

---

### СЦЕНА 10 (≈ 0:45.5–0:51)

**🎙️ Voice:** `[soft] It opens jars. It solves mazes. [whispered] It remembers your face.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_09_still`
- **Prompt:**
```
An octopus pressed to the inside of aquarium glass, one eye fixed directly at camera; a soft human-face reflection ghosted faintly on the glass between viewer and octopus; one arm reaching toward a faint human handprint smudge on the glass. Warm ochre skin, teal catch-light in the eye, chrome-glass highlights; deep abyssal void-black behind; single soft caustic god-ray from above. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real recognizable human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_10_still.png`
- **Ingredients:** `scene_01_still` + `scene_09_still`
- **Prompt:**
```
0:00–0:01: The octopus holds against the glass, eye on the viewer.
0:01–0:06: The eye tracks slightly as if following the viewer; the reaching arm touches the glass at ~0:03; the ghosted human-face reflection steadies. Hold the tension.
0:06–0:08: The eye holds the gaze, unblinking. (No transition — hard cut after this scene.)
Audio (no spoken voice): intimate room-tone of an aquarium hall, a soft glass-tap at the arm touch, sub-bass drone.
Format: 9:16 vertical, 8 sec, low motion intensity.
```

**📝 CapCut overlay:** кикер `it remembers your face` (Inter Light italic ~28pt, opacity 80%, kinetic type-in) + тикер `FINN ET AL. · CURRENT BIOLOGY · 2009`.

---

### СЦЕНА 11 (≈ 0:51–0:54.5) — THE TURN

**🎙️ Voice:** `[beat] [low] And then — [whispered] it lives barely two years.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_10_still`
- **Prompt:**
```
The octopus small and alone in a vast empty abyss, a single caustic ray narrowing around it like a closing spotlight; most of the frame deep abyssal void-black; the teal glow dimmer than before; warm ochre skin in shadow. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_11_still.png`
- **Ingredients:** `scene_01_still` + `scene_10_still`
- **Prompt:**
```
0:00–0:01: The octopus sits small in the dark.
0:01–0:06: The narrow caustic light slowly closes in; the octopus settles lower; the teal glow dims a notch. Very slow, heavy, lonely.
0:06–0:08: The light tightens to a small pool around it.
Audio (no spoken voice): a single low mournful tone, sub-bass drone thinning, distant water ambient.
Format: 9:16 vertical, 8 sec, very low motion intensity.
```

**📝 CapCut overlay:** тикер `LIFESPAN · ~1–2 YEARS` (~22pt, opacity 55%).

---

### СЦЕНА 12 (≈ 0:54.5–1:00)

**🎙️ Voice:** `[soft] The mother lays her eggs, [breath] stops eating, [whispered] and guards them in the dark.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_11_still`
- **Prompt:**
```
An octopus mother curled protectively over a hanging cluster of pearl-like translucent eggs glowing faint bone-cream; she is in soft shadow, one eye barely catching the light; tender, still, reverent. Deep abyssal void-black around; single soft caustic god-ray from above; faint teal glow. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_12_still.png`
- **Ingredients:** `scene_01_still` + `scene_11_still`
- **Prompt:**
```
0:00–0:01: The eggs hang still, faintly glowing.
0:01–0:06: The eggs shimmer faintly as the mother fans water over them; her body barely moves in vigil; her glow continues to dim slowly. Stillness as devotion.
0:06–0:08: She settles closer over the eggs, dimmer.
Audio (no spoken voice): soft slow water-fanning foley, a tender low pad, sub-bass drone.
Format: 9:16 vertical, 8 sec, very low motion intensity.
```

**📝 CapCut overlay:** кикер `she stops eating` (Inter Light italic ~26pt, opacity 70%).

---

### СЦЕНА 13 (≈ 1:00–1:04.5) — DEATH BEAT (never graphic)

**🎙️ Voice:** `[low] She dies as they hatch. [whispered] She will never meet them.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_12_still`
- **Prompt:**
```
The egg cluster releasing tiny drifting paralarvae as specks of light rising upward; below, the mother's silhouette fading into deep abyssal void-black; a single soft blood-red pulse glows once where her eye was. Dignified, never graphic, reverent. Single soft caustic god-ray from above; faint teal and bone-cream specks. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no graphic death, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_13_still.png`
- **Ingredients:** `scene_01_still` + `scene_12_still`
- **Prompt:**
```
0:00–0:01: The eggs begin to open.
0:01–0:06: Tiny hatchlings drift upward as points of light; the mother's glow fades to black with one final soft blood-red pulse at ~0:03. Dignified, tender, never graphic.
0:06–0:08: Only the rising specks of light remain over near-black. (No transition — hard cut after this scene.)
Audio (no spoken voice): a single soft heartbeat-like low pulse fading to silence, faint rising shimmer for the hatchlings, sub-bass thinning to nothing.
Format: 9:16 vertical, 8 sec, very low motion intensity.
```

**📝 CapCut overlay:** тикер `WANG & RAGSDALE · J EXP BIOL · 2018` (~22pt, opacity 55%). Без кикера — пусть сцена дышит.

---

### СЦЕНА 14 (≈ 1:04.5–1:09.5)

**🎙️ Voice:** `[soft] So everything it learns, [beat] it learns alone. [whispered] And takes with it.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_13_still`
- **Prompt:**
```
A single small octopus alone in deep abyssal void-black, a faint bioluminescent teal knowledge-glow held entirely inside its own body, nothing passing outward; no parent, no others; vast emptiness around it; single soft caustic god-ray from above. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_14_still.png`
- **Ingredients:** `scene_01_still` + `scene_13_still`
- **Prompt:**
```
0:00–0:01: The lone octopus drifts, glow inside.
0:01–0:06: Its internal teal glow flickers as it learns, but none of it leaves its body; the camera slowly pulls back to reveal total emptiness around it.
0:06–0:08: It becomes a single small point of light in the void.
Audio (no spoken voice): a lonely sustained tone, sub-bass drone, sparse water ambient.
Format: 9:16 vertical, 8 sec, low motion intensity.
```

**📝 CapCut overlay:** кикер `no one taught it` (Inter Light italic ~26pt, opacity 70%).

---

### СЦЕНА 15 (≈ 1:09.5–1:14)

**🎙️ Voice:** `[low] We share an ancestor. [soft] That tiny, forgotten thing.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_14_still`
- **Prompt:**
```
Extreme macro of a minuscule, simple worm-like ancient creature (soft, abstract, almost a smudge of light) centered in deep abyssal void-black, humble and primordial, with a faint bone-cream glow; single soft caustic god-ray from above; vast negative space. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_15_still.png`
- **Ingredients:** `scene_01_still` + `scene_14_still`
- **Prompt:**
```
0:00–0:01: The tiny creature pulses faintly in the void.
0:01–0:06: Two thin threads of light begin to grow out of it in opposite directions (the coming split); humble, quiet, slow.
0:06–0:08: The two threads reach toward opposite edges.
Audio (no spoken voice): a single fragile high tone, deep sub-bass, near-silence.
Format: 9:16 vertical, 8 sec, very low motion intensity.
```

**📝 CapCut overlay:** кикер `~600 million years ago` (Inter Light italic ~24pt, opacity 65%).

---

### СЦЕНА 16 (≈ 1:14–1:19)

**🎙️ Voice:** `[narrator] From the same beginning, the universe built a mind — [whispered] twice.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_15_still`
- **Prompt:**
```
Two glowing forms mirrored across the frame — on the left a faint cold human-brain glow, on the right a faint distributed octopus-glow — both grown from one shared point of light at center; symmetry; deep abyssal void-black; single soft caustic god-ray from above; teal and ochre tones. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_16_still.png`
- **Ingredients:** `scene_01_still` + `scene_15_still`
- **Prompt:**
```
0:00–0:01: One shared point of light glows at center.
0:01–0:06: Both minds glow up in parallel from the shared point — human-brain on the left, distributed octopus on the right; symmetrical bloom.
0:06–0:08: The octopus side rushes gently forward toward camera, ending close on it. (No transition — hard cut after this scene.)
Audio (no spoken voice): a rising two-note harmonic that resolves, sub-bass swell, water ambient.
Format: 9:16 vertical, 8 sec, low-medium motion intensity.
```

**📝 CapCut overlay:** кикер `twice` (Inter Light italic ~28pt, opacity 80%, kinetic type-in).

---

### СЦЕНА 17 (≈ 1:19–1:24.5) — META-TWIST

**🎙️ Voice:** `[beat] [whispered, intimate] And one of them just watched you — [breath] through the glass.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_16_still`
- **Prompt:**
```
An octopus eye filling the frame (callback to scene 1), now with a single blood-red catch-light reflected in the pupil and a faint reflection of a human face on the aquarium glass between viewer and eye; intimate, unsettling; warm ochre skin, chrome-glass highlights; deep abyssal void-black; single soft caustic god-ray from above. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real recognizable human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_17_still.png`
- **Ingredients:** `scene_01_still` + `scene_16_still`
- **Prompt:**
```
0:00–0:01: The eye holds, blood-red glint waiting.
0:01–0:06: The pupil contracts as if focusing on the viewer; the blood-red catch-light flares once at ~0:02; the human-face reflection sharpens, then the camera drifts so eye and reflection nearly merge.
0:06–0:08: Eye and ghost-reflection hold, almost one.
Audio (no spoken voice): all ambient cuts to a held breath of near-silence at ~0:02, then a single deep sub-bass note.
Format: 9:16 vertical, 8 sec, low motion intensity.
```

**📝 CapCut overlay:** кикер `through the glass` (Inter Light italic ~28pt, opacity 80%). В CapCut музыку/амбиент обрежь на ~0:02 этой сцены.

---

### СЦЕНА 18 (≈ 1:24.5–1:30) — FINAL HOOK

**🎙️ Voice:** `[soft] It will never know [whispered] you wondered about it too.`

**🖼️ Nano Banana Pro:**
- **Reference images:** `scene_01_still` + `scene_17_still`
- **Prompt:**
```
The octopus slowly receding into deep abyssal void-black, one arm still resting against the aquarium glass over a faint human handprint, the eye dimming; almost the entire frame is void; a last faint teal glow; single soft caustic god-ray from above narrowing to nothing. Match the color palette, lighting, grain, and overall look of the attached reference images; maintain visual continuity with the series. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain, faint water-caustic shimmer, slight chromatic aberration at edges. Avoid: no real human faces, no gore, no text artifacts.
```

**🎥 Veo 3.1:**
- **First frame:** `scene_18_still.png`
- **Ingredients:** `scene_01_still` + `scene_17_still`
- **Prompt:**
```
0:00–0:01: The octopus rests against the glass, eye dim.
0:01–0:06: The octopus drifts back into darkness; the arm slips from the glass at ~0:03; the last teal glow fades toward void.
0:06–0:08: The frame settles to near-total abyssal black; one final, barely-audible breath; the handprint lingers a moment, then darkness.
Audio (no spoken voice): a single soft exhale-like tone, sub-bass fading to silence, the clip ends in near-black quiet.
Format: 9:16 vertical, 8 sec, very low motion intensity.
```

**📝 CapCut overlay:** кикер `we were both wondering.` (Inter Light italic ~26pt, opacity 75%, fade-in 0:01 / fade-out 0:04) + хэндл канала мелко снизу.

---

## 🎞️ ШАГ 4 — CAPCUT СБОРКА (пошагово)

### 4.1 Создать проект
1. Открой **CapCut Desktop**.
2. New Project → resolution **1080×1920 (9:16 Vertical)** → 30 fps.
3. Сохрани проект → `Octopus_TikTok_90s`.

### 4.2 Импортировать ассеты
1. Drag&drop в Media bin:
   - Все 18 файлов `scene_NN_video.mp4`
   - 1 voice файл из ElevenLabs (.mp3)
   - (опц.) sub-bass loop .wav из Splice / YouTube Audio Library
   - (опц.) music bed (deep ambient / oceanic drone, минор) — ищи "deep ocean drone", "underwater ambient", "cinematic suspense"

### 4.3 Уложить voice на A2 (master timing)
1. Перетащи voice .mp3 на дорожку **A2**.
2. Начало voice → **00:00:00**.
3. Включи waveform (правый клик на трек).
4. Замерь тайминги фраз → запиши в таблицу (Шаг 1).

### 4.4 Уложить 18 клипов на V1
Для **каждой** сцены N (1→18):
1. Перетащи `scene_NN_video.mp4` на **V1** в позицию старта voice-фразы N (из таблицы таймингов).
2. Кликни на клип → правая панель → **Audio** → **Mute** (убрать Veo native audio). ИЛИ оставь Veo audio на A1 на −18 dB как ambient слой.
3. **Обрежь конец клипа** до конца voice-фразы: playhead на конец фразы N → потяни правый край клипа влево до playhead.
4. Переходи к сцене N+1.

> **Стыки:** сцены идут встык (cut). На смысловых ударах **S10→S11, S13→S14, S16→S17** оставь жёсткий хард-кат (ничего не смягчай). Остальные стыки можно смягчить очень коротким (≤0.2 с) dissolve, если хочется «перетекания».

### 4.5 Если voice-фраза длиннее 8 сек
- **Speed-ramp:** клик на клип → **Speed** → **0.7–0.8x** (растянет до ~10–11 сек).
- Либо **Freeze frame:** playhead на последний кадр → правый клик → **Freeze frame** → растяни до конца voice.
- Добавь **Fade out** (Animation → Out) на финальной сцене 18 — 1 сек.

### 4.6 Добавить мелкие тикеры/кикеры (НЕ крупный текст)
> Это ключевое отличие серии: **инфографика без огромных надписей**. Только мелкие подписи.
1. **Text** → **Default text** → перетащи на **V2** в позицию overlay (см. таблицу ниже).
2. Введи текст.
3. Шрифты: **JetBrains Mono** для тикеров (источники/числа), **Inter Light Italic** для кикеров (смысловые подписи). Если нет — скачай с Google Fonts → импортируй.
4. Размер: тикеры **~22pt**, кикеры **~26–28pt** (НИКАКИХ 80pt-заголовков).
5. Opacity: тикеры **55%**, кикеры **70–80%**, цвет — белый / bone-cream.
6. **Положение:** верхняя треть (y < 350) или центр. **НЕ нижние 320 px** — там TikTok UI.
7. Animation In/Out: **Fade** 0.3 сек (кикеры — лёгкий kinetic type-in на ключевом слове).

### 4.7 Таблица overlay (мелкий текст)

| Сцена | Тайминг | Тип | Текст |
|---|---|---|---|
| 1 | 0:01–0:05 | тикер | `GODFREY-SMITH · 2016` |
| 2 | 0:06–0:11 | кикер | `same origin` |
| 3 | 0:12–0:16 | тикер | `~600 MILLION YEARS · LAST COMMON ANCESTOR` |
| 4 | 0:17–0:21 | кикер | `a different kind of mind` |
| 5 | 0:21–0:26 | тикер | `~500,000,000 NEURONS · HOCHNER 2012` |
| 6 | 0:27–0:29 | кикер | `the arms think` |
| 7 | 0:30–0:34 | тикер | `VAN GIESEN ET AL. · CELL · 2020` |
| 8 | 0:35–0:39 | кикер | `colorblind` |
| 9 | 0:40–0:45 | тикер | `LISCOVITCH-BRAUER ET AL. · CELL · 2017` |
| 10 | 0:46–0:51 | кикер+тикер | `it remembers your face` · `FINN ET AL. 2009` |
| 11 | 0:51–0:54 | тикер | `LIFESPAN · ~1–2 YEARS` |
| 12 | 0:55–1:00 | кикер | `she stops eating` |
| 13 | 1:01–1:04 | тикер | `WANG & RAGSDALE · 2018` |
| 14 | 1:05–1:09 | кикер | `no one taught it` |
| 15 | 1:10–1:14 | кикер | `~600 million years ago` |
| 16 | 1:15–1:19 | кикер | `twice` |
| 17 | 1:20–1:24 | кикер | `through the glass` |
| 18 | 1:26–1:30 | кикер | `we were both wondering.` |

> Сдвинь тайминги под свои реальные voice-моменты.

### 4.8 Добавить sub-bass + music bed
1. Импортируй sub-bass loop (.wav) → **A3** → растяни на весь таймлайн → loop. Уровень **−24 dB**.
2. Импортируй music bed (deep ocean ambient) → **A4** → начало 0:00. Уровень **−18 dB**.
3. Включи **Ducking** на A4 под voice: −4 dB.
4. Опц. A5: underwater room tone / vinyl crackle на −30 dB.
5. **Важно:** на сцене 17 (~0:02 внутри клипа) сделай резкий обрыв music/ambient (тишина) для удара мета-твиста.

### 4.9 Финальный мастеринг
1. **Project Settings** → **1080×1920**, 30 fps.
2. **Audio peak:** peak ≤ **−1 dBTP**.
3. **LUFS target:** **−14 LUFS** integrated (плагин в pro CapCut, или измерь онлайн через Adobe Podcast / loudness.io после экспорта).
4. **Color match:** если клипы разнятся по грейду → правый клик → **Adjustments** → подкрути температуру/тинт.
5. **Export:** MP4 → H.264 → 1080×1920 → 30 fps → bitrate Recommended (HD) → Export.

---

## 🎚️ ШАГ 5 — AUDIO MIX (cheat sheet)

| Дорожка | Содержание | Уровень | Заметки |
|---|---|---|---|
| **V1** | 18 анимированных клипов | — | главная video timeline |
| **A1** (опц.) | Veo 3.1 native ambient (drone/foley) | −18 dB или mute | mute если конфликтует |
| **A2** | ElevenLabs voice (~90 сек) | **−6 dB** | master timing track |
| **A3** | Sub-bass loop 30–40 Hz | −24 dB | всё видео |
| **A4** | Music bed (deep ocean ambient) | −18 dB | duck −4 dB под voice; обрыв на S17 0:02 |
| **A5** (опц.) | Underwater room tone | −30 dB | всё видео |

**Master:** −14 LUFS, peak −1 dBTP

---

## 🎯 ВИРАЛЬНАЯ HOOK-СТРАТЕГИЯ (что куда попадает)

| Зона | Тайминг | Контент | Цель |
|---|---|---|---|
| **HOOK** | 0:00–0:03 | Сцена 1: глаз осьминога сквозь стекло + voice "alien intelligence on Earth" | "не свайпай" |
| **Curiosity build** | 0:03–0:17 | Сцены 2–3: общий предок / раскол 600 млн лет | "что это?" |
| **THE REVEAL** | 0:17–0:35 | Сцены 4–8: мозг с нуля / нейроны в руках / вкус кожей / смена цвета | момент wow |
| **Документация** | 0:35–0:51 | Сцены 9–10: правит РНК / узнаёт лицо | факты, доверие |
| **THE TURN** | 0:51–1:09 | Сцены 11–14: живёт 2 года / мать умирает / учится один | эмоция |
| **EMOTIONAL CLOSE** | 1:09–1:30 | Сцены 15–18: общий предок / разум дважды / он смотрел на тебя | финал + твист |

---

## 📱 TIKTOK ОПИСАНИЯ (выбери одно)

### 🥇 Главный вариант
```
There is an alien intelligence on Earth — and you can visit it in an aquarium 🐙

It split from our family tree 600 million years ago and built a mind from scratch. Half a billion neurons — two-thirds of them in its arms. Each arm tastes, decides, and thinks on its own. It edits its own genetic code. It remembers your face.

And it lives barely two years. The mother guards her eggs, stops eating, and dies as they hatch — so everything it learns, it learns alone.

One of them just watched you. Through the glass.

Watch till the end.

#octopus #ocean #consciousness #science #fyp
```

### 🥈 Pattern interrupt
```
Two-thirds of an octopus's mind is not in its head 🐙

It's in the arms. Each one tastes what it touches and decides on its own. It changes color in a world it can't even see in color. It rewrites its own nervous system faster than evolution should allow.

The closest thing to alien intelligence isn't in space. It's in the water — and it remembers your face.

Watch till the end.

#octopus #marinebiology #alienintelligence #science #fyp
```

### 🥉 Emotional hook
```
She stops eating to guard her eggs — and dies as they hatch 🐙

The octopus is the closest thing to an alien mind on Earth. It split from us 600 million years ago and built intelligence a completely different way. But it lives barely two years, and never meets its young.

So everything it learns, it learns alone. And takes with it.

#octopus #ocean #nature #science #fyp
```

---

## 🖼️ COVERS (3 варианта, 9:16, 1080×1920)

Генеришь как обычные stills в Nano Banana Pro (9:16), приложив `scene_01_still` как reference для единого грейда.

### COVER 1 — "ALIEN MIND"
```
Vertical 9:16 thumbnail composition, 1080×1920. Centered against deep abyssal void-black: a single huge octopus eye with a horizontal dumbbell pupil, a bioluminescent teal catch-light inside it, seen through a faint sheet of aquarium glass with one human handprint smudge. Across the upper third, in bold uppercase condensed sans-serif white typography with a subtle chrome-silver finish: "AN ALIEN MIND" — two lines ("AN ALIEN" / "MIND"). Below the eye, smaller bone-cream text: "and it remembers your face". A single thin blood-red horizontal seam across the lower third. Style: premium deep-sea / alien-intelligence documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain. Avoid: no real human faces, no gore.
```

### COVER 2 — "TWO-THIRDS IN ITS ARMS"
```
Vertical 9:16 thumbnail composition, 1080×1920. Centered against deep abyssal void-black: a full octopus suspended, its eight arms blazing with distributed bioluminescent teal neural glow while the head stays dim — visually showing the mind is in the arms. Across the upper third, in bold uppercase condensed sans-serif white typography with chrome-silver finish: "ITS MIND IS IN ITS ARMS" — three lines ("ITS MIND" / "IS IN ITS" / "ARMS"). Below, smaller bone-cream text: "500 million neurons". A thin blood-red seam across the very bottom. Style: premium deep-sea documentary — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain. Avoid: no real human faces, no gore.
```

### COVER 3 — "THROUGH THE GLASS"
```
Vertical 9:16 thumbnail composition, 1080×1920. Centered against deep abyssal void-black: an octopus pressed to aquarium glass with one eye fixed at the viewer and a faint ghosted human-face reflection on the glass between them, one arm reaching toward a human handprint; a single blood-red catch-light in the pupil. Across the upper third, in bold uppercase condensed sans-serif white typography with chrome-silver finish: "IT WATCHED YOU" — two lines ("IT WATCHED" / "YOU"). Below, smaller bone-cream text: "through the glass". A thin blood-red seam across the middle. Style: premium deep-sea documentary mixed with psychological stillness — anamorphic 35mm lens, shallow depth of field around f/1.4, single soft caustic god-ray key light from above, deep low-key chiaroscuro. Muted desaturated palette: abyssal void-black, bioluminescent teal, warm octopus-ochre, chromatophore-violet, chrome-glass silver, bone-cream, blood-red as rare accent. 9:16 vertical 1080×1920, fine 35mm film grain. Avoid: no real recognizable human faces, no gore.
```

---

## ⚠️ ЧАСТЫЕ ПРОБЛЕМЫ И РЕШЕНИЯ

### Проблема 1: Veo 3.1 клип ушёл по грейду (палитра холоднее/теплее)
**Решение:** регенерь с двумя ingredients: `scene_01_still` + предыдущий still. В промт добавь явно: "Match the exact color palette, lighting, grain, and overall look of the attached reference images. Maintain visual continuity with the series."

### Проблема 2: Nano Banana Pro рисует осьминога с другим числом/формой рук, скелет, «гуманоидность»
**Решение:** добавь в промт: "a realistic soft-bodied octopus with exactly eight arms, no bones, no humanoid features, no face". Регенерь.

### Проблема 3: Nano Banana Pro мажет текст в кадре
**Решение:** убери любые упоминания текста из промта (у нас их и нет). Все подписи добавляешь в CapCut мелкими тикерами/кикерами.

### Проблема 4: Veo 3.1 добавил голос/speech в native audio
**Решение:** в CapCut выключи Veo audio (mute V1 audio) или замени на свой underwater room tone. В промт на регенерацию добавь в начало: "ABSOLUTELY NO SPOKEN VOICE, NO DIALOGUE, NO HUMAN SPEECH in the audio. Only ambient / foley / drone."

### Проблема 5: Veo 3.1 не показывает кнопку Ingredients
**Решение:** убедись что у тебя Pro/Ultra план Google Flow. Бесплатный план может не давать ingredients.

### Проблема 6: Клипы не похожи по свету (свет с разных сторон)
**Решение:** во всех промтах есть "single soft caustic god-ray key light from above". Если Veo игнорит — усиль: "MANDATORY: a single soft caustic god-ray of light comes from the surface directly above. All shadows fall downward. This lighting must be identical across the entire series."

### Проблема 7: модерация флагает сцену смерти матери (13)
**Решение:** формулировки уже moderation-safe («dignified, never graphic, no gore»). Если флагнуло — замени «dies / death» на «her light fades», «she goes still». Смысл несёт голос, не картинка.

---

## 🎬 ФИНАЛЬНЫЙ CHECKLIST

- [ ] ElevenLabs voice mp3 готов (~90 сек)
- [ ] Тайминги фраз замерены в CapCut и записаны в таблицу
- [ ] Nano Banana Pro: 18 stills сгенерированы (включая scene_01_still как canonical grade)
- [ ] Veo 3.1: 18 видео-клипов сгенерированы (8 сек, с ingredients)
- [ ] Все ассеты в Flow Collection "Octopus TikTok 90s" с правильными именами
- [ ] Импортированы в CapCut, voice на A2
- [ ] 18 клипов на V1, обрезаны под voice-фразы
- [ ] Хард-каты на S10→S11, S13→S14, S16→S17
- [ ] Сцена 18 удлинена при необходимости (speed-ramp / freeze) + fade-out
- [ ] Мелкие тикеры/кикеры добавлены (JetBrains Mono / Inter Light, верхняя треть/центр, НЕ крупные)
- [ ] Sub-bass на A3, music bed на A4, обрыв звука на S17 0:02
- [ ] Audio peak ≤ −1 dBTP, LUFS −14
- [ ] Export 1080×1920, 30 fps, H.264
- [ ] 3 cover stills сгенерированы
- [ ] TikTok описание выбрано
- [ ] Upload на TikTok с cover + description

---

## 🤖 БОНУС — Flow Agent автоматизация (для продвинутых)

Если у тебя Pro план и доступ к Flow Agent — вставь этот промт, он прогонит stills + animations сам. Voice он не делает (ElevenLabs внешний).

```
=== START MASTER PROMPT FOR FLOW AGENT ===

ROLE: You are my full-pipeline animation agent for a 90-second vertical TikTok video about the octopus as an alien intelligence. Execute a 4-phase pipeline. Voice is added later from ElevenLabs — do NOT generate any spoken voice in any output. Confirm at the end of each phase.

==== PHASE A — SETUP ====
1. Image default → Nano Banana Pro, aspect 9:16 (1080×1920).
2. Video default → Veo 3.1, aspect 9:16, duration 8 seconds.
3. Create collection "Octopus TikTok 90s".

==== PHASE B — 18 STILLS WITH REFERENCES ====
For each scene N from 1 to 18:
  a) Use Nano Banana Pro with the STILL PROMPT I provide.
  b) Attach references:
     - Scene 1: no references.
     - Scene 2: attach scene_01_still.
     - Scenes 3-18: attach BOTH scene_01_still (canonical grade) AND scene_(N-1)_still (continuity).
  c) Save as scene_{N:02d}_still. Move into collection.

==== PHASE C — 18 ANIMATIONS (motion + ambient audio only, NO voice) ====
For each scene N from 1 to 18:
  a) Use Veo 3.1 with the VIDEO PROMPT I provide.
  b) First frame = scene_{N:02d}_still.
  c) Ingredients: Scene 1 none; Scene 2 scene_01_still; Scenes 3-18 scene_01_still + scene_(N-1)_still.
  d) Negative prompt: "no spoken voice, no dialogue, no speech, no text artifacts, no watermark, no logo, no aspect bars, no fast camera, no recognizable real human faces, no gore, no large on-screen text".
  e) Save as scene_{N:02d}_video. Move into collection.

==== PHASE D — 3 COVERS + RENAME ====
1. Generate 3 cover stills with Nano Banana Pro at 9:16 using the COVER PROMPTS I provide (attach scene_01_still as reference). Save as cover_01_alien_mind, cover_02_arms, cover_03_through_the_glass.
2. Verify all assets are in the collection.
3. Final progress report.

FAILURE HANDLING:
- If moderation flags a prompt, paraphrase the trigger ("death" → "her light fades", "dies" → "goes still") and retry once.
- If a still mangles in-frame text, regenerate without any text and tag "needs_capcut_overlay".
- If Veo adds spoken voice, regenerate with the negative prompt enforced and prepend "ABSOLUTELY NO SPOKEN VOICE in audio".

I will paste the 18 STILL PROMPTS, 18 VIDEO PROMPTS, and 3 COVER PROMPTS next.

=== END MASTER PROMPT FOR FLOW AGENT ===
```

После запуска копируй блоки из секций "СЦЕНА N → 🖼️ Nano Banana Pro / 🎥 Veo 3.1" и кидай Agent'у.

---

## 🎨 ПАЛИТРА (для справки, уже зашита в промты)

- **Abyssal void-black** (фон / тени): `#03060A`
- **Bioluminescent teal** (нейро-свечение / ключевой акцент): `#1FB6C9`
- **Warm octopus-ochre** (кожа, midtones): `#9C5A3C`
- **Chromatophore-violet** (пульсации кожи): `#6E2A4D`
- **Chrome-glass silver** (стекло аквариума / блики): `#C7D0D4`
- **Bone-cream** (яйца / древо / предок): `#D9C9A0`
- **Blood-red accent** (редкий акцент — сцены 3, 13, 17): `#7A1B1B`

---

## 🔗 (Опционально) Связать сцены «перетеканием» вместо встыка

Если хочешь, чтобы сцены не просто резались, а **перетекали** одна в другую (морфинг), используй last frame в Veo 3.1:
- Для сцены N задай **end frame = `scene_(N+1)_still.png`** (кроме хард-катов S10→S11, S13→S14, S16→S17 — там last frame НЕ ставь).
- Тогда конец клипа N = начало клипа N+1, и стык невидим.
- Это дороже по генерациям и сложнее контролировать грейд, поэтому в основном workflow выше мы оставили first-frame-only. Включай по желанию.

---

## ✅ ГОТОВО

После полного прогона у тебя на руках:
- 18 stills (.png, 1080×1920)
- 18 animations (.mp4, 8 сек, 1080×1920, native ambient audio)
- 1 voice track (.mp3, ~90 сек)
- 3 cover stills (.png, 1080×1920)
- 1 финальный TikTok-ready видеофайл (.mp4, 1080×1920, ~90 сек, −14 LUFS)

Время прогона: 1.5–3 часа от старта Flow до финального экспорта.
