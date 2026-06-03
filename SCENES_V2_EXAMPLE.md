# 🎬 Конкретный пример «до → после» (Сцены 1–4 в стиле v2)

Демонстрация системы из `CINEMATIC_SYSTEM_V2.md` на первых сценах ролика про anendophasia.
Показывает: **референс-лок стиля**, **чейнинг сцен (first/last frame)** и **инфографику без крупного текста**.

> Предпосылка: один раз сгенерирован `Style DNA Kit` = `[palette_plate, lighting_plate, head_sheet, motif_sheet]`.
> В каждой NBP-генерации он подаётся как reference images, поэтому промпт описывает ТОЛЬКО содержание.

---

## SCENE 1 (0:00–0:05) — HOOK

**Line:** *«Some people have never heard a voice in their head. They might be reading this right now.»*

**NBP still (с референсами):**
> Reference: `[palette_plate, lighting_plate, motif_sheet]`.
> «Match palette/grain/DOF/lighting of refs exactly. Compose: extreme macro of a single human ear in profile, upper-mid frame; faint bone-cream concentric sound-wave ripple emanating from the ear canal; rest of head in void-black. Lower 35% empty void. No text/glyphs/numbers anywhere.»

**Veo 3.1 (chaining):**
> `first_frame = still_S1`, `last_frame = still_S2`.
> Motion: 4 ripples expand from the ear (1 / 1.2 s); **at 0:03 camera begins a slow pull-back** so the ear starts becoming part of the head silhouette of S2. Single dust mote drifts past at 0:03.

**Текст на экране (минимальный):**
- ❌ Убрано: `SOME PEOPLE / NEVER HEAR IT.` (Druk Wide 88pt).
- ✅ Только моно-тикер снизу: `HURLBURT RT · 2011` — JetBrains Mono 22pt, opacity 55%, нижние 6%.
- Смысл «some people never hear it» несёт **голос**, а не плашка.

---

## SCENE 2 (0:05–0:10) — THE ASSUMPTION

**Line:** *«Most of us assume thinking sounds like talking. A voice that narrates.»*

**NBP still (с референсами):**
> Reference: `[palette_plate, head_sheet, motif_sheet]`.
> «Match refs. Compose: warm skin-midtone head silhouette in profile (identical to head_sheet), slightly left of center; a bone-cream sound-wave ribbon flows from the closed mouth outward to the right edge. Upper 20% / lower 25% empty. No text.»

**Veo 3.1 (chaining):**
> `first_frame = still_S2` (= last_frame S1), `last_frame = still_S3`.
> Motion: ribbon oscillates как «речь»; **к 0:04 силуэт начинает множиться** в ряд фигур → готовит S3.

**Текст на экране:**
- ❌ Убрано: `THINKING SOUNDS / LIKE TALKING.` (72pt).
- ✅ Кикер сбоку: `thinking = talking?` — Inter Light italic 26pt, opacity 70%. Один короткий вопрос-глиф, не заголовок.

---

## SCENE 3 (0:10–0:15) — THE PERCENTAGE  *(инфографика как изображение)*

**Line:** *«But thirty to fifty percent of people don't experience that voice. At all.»*

**NBP still (с референсами):**
> Reference: `[palette_plate, lighting_plate]`.
> «Match refs. Compose: austere row of 10 human silhouettes shoulder-to-shoulder, public-health-diagram style; some warm with faint inner cream glow, others pure void-black. Void background. Upper 25% / lower 40% empty. No text, no numbers.»

**Veo 3.1 (chaining):**
> `first_frame = still_S3`, `last_frame = still_S4`.
> Motion: **3–5 из 10 фигур гаснут до void-black по очереди** (внутренний голос «выключается») — именно это анимированное гашение и есть «30–50%». Затем ряд начинает сжиматься в одну фигуру → S4.

**Текст на экране — ГЛАВНЫЙ приём минимализма:**
- ❌ Убрано: большой `30–50%`.
- ✅ Число несёт **сам визуал**: гаснущие фигуры = доля. На экране только крошечный тикер `HEAVEY & HURLBURT · 2008` (22pt, opacity 55%).
- Зритель «считает» долю глазами, а не читает цифру.

---

## SCENE 4 (0:15–0:20) — ANENDOPHASIA

**Line:** *«In 2024, scientists gave it a name. Anendophasia. The absence of inner speech.»*

**NBP still (с референсами):**
> Reference: `[palette_plate, head_sheet, motif_sheet]`.
> «Match refs. Compose: single head silhouette; where the inner voice would be — an empty bone-cream outline of a speech-bubble with a single thin blood-red `#7A1B1B` stroke (bubble interior empty). Void around. No text inside the bubble.»

**Veo 3.1 (chaining):**
> `first_frame = still_S4` (= last_frame S3), `last_frame = still_S5`.
> Motion: красный контур пузыря **прорисовывается линией** (0:00–0:02), затем пустеет; камера медленно толкается внутрь головы → S5.

**Текст на экране:**
- ❌ Убрано: крупная плашка `ANENDOPHASIA`.
- ✅ Термин печатается **по буквам** мелким моно внутри/под пустым пузырём: `anendophasia` — JetBrains Mono 30pt, opacity 85%, kinetic type-in в ритме голоса. Снизу тикер `NEDERGAARD & LUPYAN · 2024`.
- Это единственная сцена, где термин показан текстом — потому что это новое слово. Один глиф, мелко, в кадре.

---

## Что демонстрирует пример

1. **Единый стиль** — каждый кадр наследует `Style DNA Kit` через референсы, а не переписанный `GLOBAL STYLE LOCK`.
2. **Связность** — `last_frame[N] == first_frame[N+1]`, сцены перетекают морфингом/движением камеры, а не кросс-фейдом.
3. **Без крупных текстов** — смысл несут голос + анимированный визуал-данные; на экране максимум один мелкий глиф/тикер.
</content>
