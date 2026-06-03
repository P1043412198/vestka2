# 🐙 Готовый набор промптов для Flow — «Octopus / Other Minds» (копировать-вставлять)

> **GLOBAL STYLE LOCK вшит В КАЖДЫЙ промпт** (а не отдельным блоком) — как ты просил. Просто копируй блок целиком в Flow.
> Порядок: сначала 4 кадра Style DNA Kit (по желанию), потом 18 сцен. Для картинок model = **Nano Banana Pro**, для видео = **Veo 3.1**, везде **9:16**.
> Опционально для консистентности осьминога: добавляй `creature_sheet` в **ingredients** (кнопка **Add** или `@`). Стиль это не заменяет — он уже в тексте промпта.

---

## STYLE DNA KIT (4 кадра — генерим один раз, model = Nano Banana Pro, 9:16)

**1) palette_plate**
```
Abstract cinematic style plate, no subject. Deep abyssal ocean black #03060A, bioluminescent teal glow #1FB6C9, warm octopus-ochre skin tones #9C5A3C, chromatophore-violet pulses #6E2A4D, chrome-glass highlights #C7D0D4, bone-paper cream #D9C9A0 accent. Anamorphic 35mm, shallow depth of field f/1.4, water-caustic shimmer, fine film grain, low-key chiaroscuro, 9:16 vertical 1080x1920. No letters, no numbers, no text anywhere.
```

**2) lighting_plate**
```
Lighting reference plate, no subject. A single caustic god-ray of light from the surface above piercing deep dark water, soft bioluminescent teal secondary glow #1FB6C9, everything else deep void-black #03060A. Cinematic anamorphic 35mm, shallow depth of field f/1.4, fine film grain, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. No letters, no numbers, no text anywhere.
```

**3) creature_sheet** (герой — держит осьминога одинаковым во всех сценах)
```
Character reference sheet of ONE octopus on a plain dark background, three angles on one sheet: full body, close-up of one eye with a horizontal dumbbell pupil, close-up of one arm with suckers. Consistent warm ochre skin #9C5A3C with subtle chromatophores, faint bioluminescent teal neural glow #1FB6C9. Cinematic anamorphic 35mm, shallow depth of field, plain dark background, fine film grain, 9:16 vertical 1080x1920. No letters, no numbers, no text anywhere.
```

**4) motif_sheet**
```
Reference sheet of recurring motifs on a plain dark background: a single sucker close-up, one octopus eye, a thin teal bioluminescent neural thread, aquarium glass with a faint human handprint, a forking evolutionary-tree line, a cluster of pearl-like translucent eggs. Cinematic anamorphic 35mm, teal #1FB6C9 + ochre #9C5A3C + void-black #03060A palette, fine film grain, 9:16 vertical 1080x1920. No letters, no numbers, no text anywhere.
```

---

# 18 СЦЕН

> Для каждой сцены: **NBP** = промпт картинки (стиль уже внутри). **Veo 3.1** = промпт анимации + какие кадры ставить в `start frame` / `end frame`. **CapCut** = мелкий текст (в видео крупного текста нет).

---

## SCENE 1 (0:00–0:05) — HOOK
**Реплика:** *"There is an alien intelligence on Earth. You can visit it in an aquarium."*

**NBP (картинка):**
```
Extreme close-up of a single octopus eye with a horizontal dumbbell pupil, filling the upper-mid frame, emerging from abyssal black; a faint sheet of aquarium glass between viewer and eye with one soft human handprint smudge at lower-left; a bioluminescent teal catch-light in the pupil. Lower 35% and upper 18% are empty void-black for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bioluminescent teal #1FB6C9 + warm ochre #9C5A3C, chrome-glass highlights, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S1` · `end frame: still_S2`:
```
The pupil slowly dilates; a single caustic ray drifts across the eye over 5 seconds; the camera gently pulls back so the eye becomes one point in a wider darkness; a single chromatophore-violet pulse ripples once across the surrounding skin. Slow, hushed, intimate. 9:16.
```
**CapCut:** только тикер снизу `GODFREY-SMITH · 2016` (JetBrains Mono 22pt, opacity 55%). Без заголовка.

---

## SCENE 2 (0:05–0:10) — NOT FROM SPACE
**Реплика:** *"It didn't come from space. It came from the same place we did — and then went the other way."*

**NBP (картинка):**
```
Deep abyssal field; a single faint bone-cream hairline thread of light enters from the bottom and forks into two diverging paths heading to opposite top corners; empty void all around. Upper 20% and lower 25% empty negative space for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bone-paper cream #D9C9A0 thread + faint bioluminescent teal #1FB6C9, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S2` · `end frame: still_S3`:
```
The single thread of light travels upward and at 0:03 splits into two diverging lines that drift apart toward opposite corners; slow lateral drift left-to-right; abyssal calm. 9:16.
```
**CapCut:** кикер `same origin` (Inter Light italic 26pt, opacity 70%).

---

## SCENE 3 (0:10–0:15) — THE SPLIT
**Реплика:** *"Six hundred million years ago, our family tree split. On one side: us. On the other — this."*

**NBP (картинка):**
```
Minimal Saul-Bass-style evolutionary fork: two thin bone-cream lines diverging from one node low-center; the left branch ends in a faint human-head silhouette, the right branch ends in a faint octopus silhouette; a single blood-red #7A1B1B dot glows at the fork node. Abyssal void around. Upper 25% and lower 30% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bone-paper cream #D9C9A0 line work + bioluminescent teal #1FB6C9 + one blood-red #7A1B1B accent, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S3` · `end frame: still_S4`:
```
The two branches slowly draw outward from the red node; the octopus-side branch glows brighter and the camera drifts toward it; the red node pulses once. 9:16.
```
**CapCut:** тикер `~600 MILLION YEARS · LAST COMMON ANCESTOR` (22pt, opacity 55%). Число несёт расходящееся древо, не текст.

---

## SCENE 4 (0:15–0:20) — A MIND FROM SCRATCH
**Реплика:** *"It built a mind from scratch. Nothing like ours."*

**NBP (картинка):**
```
A full octopus suspended in abyssal black, body in soft focus, with a faint bioluminescent teal neural glow tracing diffusely through its whole form like a map; a single caustic key light from above. Upper 20% and lower 28% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bioluminescent teal #1FB6C9 + warm ochre #9C5A3C skin, chrome-glass highlights, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S4` · `end frame: still_S5`:
```
The teal neural glow slowly intensifies and concentrates, then begins migrating outward toward the arms; the octopus drifts and rotates a few degrees. Slow, awe. 9:16.
```
**CapCut:** кикер `a different kind of mind` (Inter Light italic 26pt, opacity 70%).

---

## SCENE 5 (0:20–0:25) — HALF A BILLION NEURONS
**Реплика:** *"Half a billion neurons. But two-thirds of them are not in its head."*

**NBP (картинка):**
```
An octopus arranged so the small central brain region glows a faint but DIM teal, while a vast diffuse cloud of teal points spreads down into the arms — visually obvious that most of the glow is NOT in the head. Austere, diagram-like. Upper 25% and lower 30% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bioluminescent teal #1FB6C9 + warm ochre #9C5A3C skin, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S5` · `end frame: still_S6`:
```
The dim head-glow holds; the arm-glow swells and brightens dramatically over 5 seconds; subtle camera push toward the arms. 9:16.
```
**CapCut:** тикер `~500,000,000 NEURONS · HOCHNER 2012` (22pt, opacity 55%). Долю несёт распределение свечения.

---

## SCENE 6 (0:25–0:30) — IN ITS ARMS (reveal)
**Реплика:** *"They're in its arms."*

**NBP (картинка):**
```
Extreme close-up of a single octopus arm curling toward camera, suckers in sharp focus, bright bioluminescent teal neural threads running visibly along the arm's length; the rest in void-black. Upper 18% and lower 28% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bioluminescent teal #1FB6C9 + warm ochre #9C5A3C skin, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S6` · `end frame: still_S7`:
```
The arm coils with independent, searching motion; teal threads pulse along it like firing neurons; a single sucker reaches toward a point of light. Confident reveal. 9:16.
```
**CapCut:** кикер `the arms think` (Inter Light italic 26pt, opacity 75%, kinetic type-in на "think").

---

## SCENE 7 (0:30–0:35) — TASTE BY TOUCH
**Реплика:** *"Each arm can taste what it touches. Each arm can decide on its own."*

**NBP (картинка):**
```
Macro of one octopus sucker pressed against a pale chrome-glass surface; from the contact point faint bone-cream concentric "taste" ripples bloom outward; a teal micro-glow inside the sucker rim. Upper 22% and lower 28% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bioluminescent teal #1FB6C9 + warm ochre #9C5A3C + chrome-glass #C7D0D4, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S7` · `end frame: still_S8`:
```
The sucker presses and releases; faint taste-ripples bloom at the contact point at 0:01 and 0:03; the touched surface begins shifting hue. Slow drift. 9:16.
```
**CapCut:** тикер `VAN GIESEN ET AL. · CELL · 2020` (22pt, opacity 55%).

---

## SCENE 8 (0:35–0:40) — COLOR IT CANNOT SEE
**Реплика:** *"It changes color to match a world it cannot even see in color."*

**NBP (картинка):**
```
A patch of octopus skin filling the frame, chromatophores mid-shift — ochre, violet and teal blooming across the surface in an organic stipple; soft caustic light. Upper 20% and lower 28% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bioluminescent teal #1FB6C9 + warm ochre #9C5A3C + chromatophore-violet #6E2A4D, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S8` · `end frame: still_S9`:
```
Waves of color ripple across the skin (chromatophores firing) over the full 5 seconds, mesmerizing and slow; near the end the color pattern resolves into thread-like lines. 9:16.
```
**CapCut:** кикер `colorblind` (Inter Light italic 26pt, opacity 70%).

---

## SCENE 9 (0:40–0:45) — REWRITING ITSELF
**Реплика:** *"It edits its own genetic code — rewriting its nervous system faster than evolution should allow."*

**NBP (картинка):**
```
An abstract bone-cream and teal double-helix-like strand floating in void, with several rungs glowing and visibly re-arranging (implied gene editing), abstract not literal, no real characters. Upper 25% and lower 30% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bioluminescent teal #1FB6C9 + bone-paper cream #D9C9A0, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S9` · `end frame: still_S10`:
```
Rungs of the strand flicker and swap positions (gene editing); the strand slowly coils tighter; near the end it dissolves toward a single point. Faint chromatic aberration. 9:16.
```
**CapCut:** тикер `LISCOVITCH-BRAUER ET AL. · CELL · 2017` (22pt, opacity 55%).

---

## SCENE 10 (0:45–0:50) — IT REMEMBERS YOU
**Реплика:** *"It opens jars. It solves mazes. It remembers your face."*

**NBP (картинка):**
```
The octopus pressed to the inside of aquarium glass, one eye fixed directly at camera; a soft human-face reflection ghosted faintly on the glass between viewer and octopus; one arm reaching toward a faint handprint smudge. Upper 18% and lower 25% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bioluminescent teal #1FB6C9 + warm ochre #9C5A3C + chrome-glass #C7D0D4, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S10` · `end frame: (НЕТ — хард-кат на S11, режем в CapCut)`:
```
The eye tracks slightly as if following the viewer; the reaching arm touches the glass at 0:03; the ghosted human-face reflection steadies. Hold the tension at the end (no transition). 9:16.
```
**CapCut:** кикер `it remembers your face` (Inter Light italic 28pt, opacity 80%, kinetic type-in) + тикер `FINN ET AL. · CURRENT BIOLOGY · 2009`.

---

## SCENE 11 (0:50–0:55) — BARELY TWO YEARS (the turn)
**Реплика:** *"And then — it lives barely two years."*

**NBP (картинка):**
```
The octopus small and alone in a vast empty abyss, a single caustic ray narrowing around it like a closing spotlight; most of the frame deep void-black. Upper 25% and lower 35% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + dim bioluminescent teal #1FB6C9 + warm ochre #9C5A3C, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S11` · `end frame: still_S12`:
```
The narrow caustic light slowly closes in; the octopus settles lower; the teal glow dims a notch. Very slow, heavy, lonely. 9:16.
```
**CapCut:** тикер `LIFESPAN · ~1–2 YEARS` (22pt, opacity 55%).

---

## SCENE 12 (0:55–1:00) — THE MOTHER
**Реплика:** *"The mother lays her eggs, stops eating, and guards them in the dark."*

**NBP (картинка):**
```
The octopus curled protectively over a hanging cluster of pearl-like translucent eggs glowing faint bone-cream; she is in soft shadow, one eye barely catching the light; tender, still. Upper 22% and lower 28% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bone-paper cream #D9C9A0 eggs + bioluminescent teal #1FB6C9 + warm ochre #9C5A3C, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S12` · `end frame: still_S13`:
```
The eggs shimmer faintly; the mother's body barely moves in vigil; her glow continues to dim slowly. Stillness as grief. 9:16.
```
**CapCut:** кикер `she stops eating` (Inter Light italic 26pt, opacity 70%).

---

## SCENE 13 (1:00–1:05) — SHE DIES AS THEY HATCH (death beat)
**Реплика:** *"She dies as they hatch. She will never meet them."*

**NBP (картинка):**
```
The egg cluster releasing tiny drifting paralarvae as specks of light rising upward; below, the mother's silhouette fades into void; a single blood-red #7A1B1B pulse glows once where her eye was. Dignified, never graphic. Upper 25% and lower 30% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bone-paper cream #D9C9A0 specks + bioluminescent teal #1FB6C9 + one blood-red #7A1B1B accent, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S13` · `end frame: (НЕТ — хард-кат на S14, режем в CapCut)`:
```
Tiny hatchlings drift upward as points of light; the mother's glow fades to black with one final blood-red pulse at 0:03. Dignified, never graphic. End on near-black. 9:16.
```
**CapCut:** тикер `WANG & RAGSDALE · J EXP BIOL · 2018` (22pt, opacity 55%). Без кикера — пусть дышит.

---

## SCENE 14 (1:05–1:10) — IT LEARNS ALONE
**Реплика:** *"So everything it learns, it learns alone. And takes with it."*

**NBP (картинка):**
```
A single small octopus alone in void, a faint teal knowledge-glow held entirely inside its own body, nothing passed outward; no parent, no others. Upper 25% and lower 30% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bioluminescent teal #1FB6C9 + warm ochre #9C5A3C, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S14` · `end frame: still_S15`:
```
The lone octopus's internal glow flickers as it learns, but none of it leaves its body; near the end the camera pulls back to reveal total emptiness around it. 9:16.
```
**CapCut:** кикер `no one taught it` (Inter Light italic 26pt, opacity 70%).

---

## SCENE 15 (1:10–1:15) — WE SHARE AN ANCESTOR
**Реплика:** *"We share an ancestor. That tiny, forgotten thing."*

**NBP (картинка):**
```
Extreme macro of a minuscule, simple worm-like ancient creature (soft, abstract, almost a smudge of light) centered in void, humble and primordial, with a faint bone-cream glow. Upper 25% and lower 30% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bone-paper cream #D9C9A0 + faint bioluminescent teal #1FB6C9, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S15` · `end frame: still_S16`:
```
The tiny primordial creature pulses faintly; two threads of light begin to grow out of it in opposite directions. Humble, quiet. 9:16.
```
**CapCut:** кикер `~600 million years ago` (Inter Light italic 24pt, opacity 65%).

---

## SCENE 16 (1:15–1:20) — A MIND, TWICE
**Реплика:** *"From the same beginning, the universe built a mind — twice."*

**NBP (картинка):**
```
Two glowing forms mirrored across the frame — on the left a faint human-brain glow, on the right a faint distributed octopus-glow — both grown from one shared point of light at center; symmetry. Upper 25% and lower 28% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bioluminescent teal #1FB6C9 + warm ochre #9C5A3C, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S16` · `end frame: (НЕТ — хард-кат на S17, режем в CapCut)`:
```
Both minds glow up in parallel; near the end the octopus side rushes forward toward camera, ending close on it. 9:16.
```
**CapCut:** кикер `twice` (Inter Light italic 28pt, opacity 80%, kinetic type-in).

---

## SCENE 17 (1:20–1:25) — IT WATCHED YOU (meta-twist)
**Реплика:** *"And one of them just watched you — through the glass."*

**NBP (картинка):**
```
An octopus eye filling the frame (callback to scene 1), now with a single blood-red #7A1B1B catch-light reflected in the pupil and a faint reflection of a human face on the aquarium glass between viewer and eye; intimate, unsettling. Upper 18% and lower 25% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + bioluminescent teal #1FB6C9 + warm ochre #9C5A3C + chrome-glass #C7D0D4 + one blood-red #7A1B1B accent, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S17` · `end frame: still_S18`:
```
The pupil contracts as if focusing on the viewer; the blood-red catch-light flares once at 0:02; the human-face reflection sharpens, then the camera drifts so eye and reflection nearly merge. 9:16.
```
**CapCut:** кикер `through the glass` (Inter Light italic 28pt, opacity 80%). Музыка обрывается на 0:02.

---

## SCENE 18 (1:25–1:30) — FINAL HOOK
**Реплика:** *"It will never know you wondered about it too."*

**NBP (картинка):**
```
The octopus slowly receding into abyssal black, one arm still resting against the aquarium glass over a faint human handprint, the eye dimming; almost the entire frame is deep void. Upper 25% and lower 35% empty for later text. Cinematic anamorphic 35mm, shallow depth of field f/1.4, deep void-black #03060A + dim bioluminescent teal #1FB6C9 + warm ochre #9C5A3C + chrome-glass #C7D0D4, single caustic god-ray from above, fine film grain, water-caustic shimmer, slight chromatic aberration at edges, low-key chiaroscuro, 9:16 vertical 1080x1920. Strict: do NOT generate any letters, glyphs, words, numbers or typography anywhere.
```
**Veo 3.1** — `start frame: still_S18` · `end frame: (нет — финал)`:
```
The octopus drifts back into darkness; the arm slips from the glass at 0:03; the last teal glow fades to void by 0:05; a final, barely-audible breath. 9:16.
```
**CapCut:** кикер `we were both wondering.` (Inter Light italic 26pt, opacity 75%, fade in 0:01 / fade out 0:04) + хэндл канала снизу.

---

## Памятка по связке
- `end frame` каждой сцены = `start frame` следующей → сцены перетекают без видимого стыка.
- **Хард-каты** (без end frame, режем в CapCut): **S10→S11, S13→S14, S16→S17**.
- Длина в Flow ~8 сек → подрезать каждый клип до **5 сек** в CapCut (итого 90 сек).
- В видео **только мелкие тикеры/кикеры** (строка CapCut у каждой сцены). Крупный текст — не используем.
</content>
