# 🐙 OTHER MINDS — «Инопланетный разум уже здесь. И он только что посмотрел на тебя сквозь стекло»

**Tagline:** *The universe built a mind. Twice.*

- **Duration:** 90 sec → **18 scenes × 5 sec each**
- **Format:** Vertical 9:16 (1080×1920, native TikTok / Reels / Shorts) — генерируется нативно в Veo 3.1
- **Voice:** Female contralto, hushed-intimate-confessional ~145 WPM, ElevenLabs v3
- **Visual references:** Denis Villeneuve "Arrival" (first contact, alien grammar) × James Cameron deep-sea documentary (abyssal bioluminescence) × Jonathan Glazer "Under the Skin" (cold alien intimacy) × Saul Bass title restraint (typographic minimalism) × archival cephalopod-cognition imagery (Godfrey-Smith, Bellono lab Harvard, Ragsdale lab UChicago)
- **Series position:** Video #14 in the science-thriller serialized channel (after Eyes / Brain / Mirror / Voice / Pope / Time / Dalai Lama / Tattoo / Tardigrade / Anesthesia / Crow / Voyager 1 / Inner Monologue)
- **Built on:** `CINEMATIC_SYSTEM_V2.md` — единый стиль через Style DNA Kit, связность через Veo 3.1 first/last-frame chaining, инфографика без крупных текстов.

---

## 🎨 GLOBAL STYLE LOCK

Cinematic anamorphic 35mm, shallow DOF f/1.4. Abyssal deep-ocean darkness pierced by a single caustic god-ray key light from the surface above; soft bioluminescent teal glow as the only secondary light; warm octopus-ochre skin midtones; chrome-glass aquarium highlights; deep void-black silence and negative space; occasional chromatophore-violet pulse across skin; rare blood-red brand accent. 9:16 vertical 1080×1920. Fine film grain, faint moving water-caustic shimmer over everything, very slight chromatic aberration at frame edges (lens-looking-through-water feel). Dim low-key chiaroscuro lighting. Aesthetic: peer-reviewed cephalopod-cognition lab crossed with "Arrival"-style first-contact awe. Mood: hushed, intimate, awe braided with unease — the feeling of meeting another mind that is nothing like yours.

**Color palette:**

| Name | Hex | Use |
|---|---|---|
| Abyssal void-black | `#03060A` | The deep, silence, negative space |
| Bioluminescent teal | `#1FB6C9` | Neural glow, the "alien signal", light in the dark |
| Octopus ochre-rust | `#9C5A3C` | The creature's skin, warmth, arms |
| Chromatophore violet | `#6E2A4D` | Color-change pulses, alien "emotion" |
| Glass-chrome pale | `#C7D0D4` | Aquarium glass, reflections, instruments |
| Bone-paper cream | `#D9C9A0` | Typography (micro-tickers), atlas line work |
| Blood-red accent | `#7A1B1B` | Series brand signature (used 2–3× across video) |

**Series red-accent consistency:** `#7A1B1B` appears in:
- SCENE 3 — single red node at the fork of the evolutionary family-tree line (the split point of lineages)
- SCENE 13 — single red pulse as the mother's last bioluminescent glow fades (the death beat)
- SCENE 17 — single red catch-light reflected in the octopus eye at the meta-twist (it is watching you)

---

## 🔒 STYLE DNA KIT (генерится ОДИН раз — подаётся референсами в каждую сцену)

> По системе v2: вместо повторения GLOBAL STYLE LOCK текстом в каждом промпте — лочим look набором эталонных изображений (NBP держит до 14 референсов, ~90% консистентности).

1. **`palette_plate`** — эталон цвета/контраста: abyssal black + teal glow + ochre skin + violet pulse + caustic shimmer + film grain.
2. **`lighting_plate`** — эталон света: единственный каустический god-ray сверху, низкий ключ, био-теал как вторичный источник.
3. **`creature_sheet`** — сам осьминог: текстура кожи с хроматофорами, один большой горизонтальный зрачок-глаз, рука с присосками крупно, 3–4 ракурса на одном листе. **Это «личность» героя — должна быть идентична во всех сценах.**
4. **`motif_sheet`** — повторяющиеся мотивы: присоска крупным планом, один глаз, био-люминесцентная нейронная нить, аквариумное стекло с отпечатком человеческой ладони, развилка эволюционного древа, кладка яиц-жемчужин.

**Шаблон промпта в каждой сцене:**
```
Reference images: [palette_plate, lighting_plate, creature_sheet (+ motif_sheet при нужде)]
Prompt: "Match the exact palette, grain, caustic light and depth-of-field of the references.
Keep the octopus identical to the creature sheet. Compose: <содержание сцены, 1–2 предложения>.
No text, glyphs, numbers or typography anywhere."
```

---

## 🔗 SCENE CHAINING MAP (Veo 3.1 first-frame → last-frame)

> `last_frame[N] == first_frame[N+1]` — сцены перетекают морфингом/движением камеры, а не кросс-фейдом.

**Сквозные «якорные мотивы» (visual thread через весь фильм):**
- **Био-теал нейронная нить** — рождается в руке (S6), становится линией эволюционного древа (S3 reverse-echo), нитью РНК (S9), угасающим свечением матери (S13), катч-лайтом в глазу (S17).
- **Один глаз осьминога** — возвращается в S1, S10, S17, S18.
- **Аквариумное стекло + отпечаток ладони** — S1, S10, S17, S18 (граница между двумя разумами).
- **Blood-red accent** — S3, S13, S17.

**Хард-каты только на смысловых ударах:** S10→S11 (поворот к смертности), S13→S14 (смерть матери), S16→S17 (meta-twist). Всё остальное перетекает.

---

## 🛡️ MODERATION-SAFE BUILD

### ❌ Triggers to avoid
- «Осьминог умнее человека» / превосходство одного вида — нет (рамка: *другой*, не *лучше*)
- Графика смерти/страдания матери — никакой жести; смерть подаётся как природное чудо с достоинством
- Любые пищевые/кулинарные образы (живой осьминог, поедание) — строго избегать
- Переклеймы про сознание («у него есть душа», «он чувствует точно как мы») — держим «мы не знаем, каково это»
- «Инопланетяне реальны / он буквально с другой планеты» — это метафора независимой эволюции; земное происхождение проговаривается

### ✅ Safe alternatives
- Прямые ссылки на peer-reviewed источники (оверлеи-цитаты, см. ниже)
- Рамка «независимая эволюция сложного познания» (independent evolution of complex cognition)
- Стилизованный образ существа — без тревожных/натуралистичных деталей
- Смерть как **семельпария** (биология вида) — с тоном благоговения, не ужаса
- Твист — человеческое изумление («впервые мы не одни в способе быть умом»), не угроза

### Citation standards (display as small CapCut tickers — НЕ крупным текстом):
- `GODFREY-SMITH P (2016). OTHER MINDS. FARRAR, STRAUS & GIROUX.`
- `VAN GIESEN L ET AL. (2020). CELL 183(3), 594–604.` — taste-by-touch / chemotactile suckers
- `WANG ZY & RAGSDALE CW (2018). J EXP BIOL 221.` — optic gland / maternal senescence
- `LISCOVITCH-BRAUER N ET AL. (2017). CELL 169(2), 191–202.` — RNA editing in cephalopods
- `FINN JK ET AL. (2009). CURRENT BIOLOGY 19(23), R1069.` — defensive tool use
- `HOCHNER B (2012). CURRENT BIOLOGY 22(20), R887–R892.` — embodied nervous system
- `~500 MILLION NEURONS · ~2/3 IN THE ARMS (HOCHNER 2012)`

### Tone guardrails
- Never «smarter», never «better», never «alien invader». The wonder is *difference*, not hierarchy.
- Intimate-confessional — голос говорит *тебе*, тихо, на грани шёпота.
- Твист — благоговение: «разум возник дважды, независимо, и один из них смотрит на тебя».
- Death beat (S11–S14) — с достоинством, как у природы, без эксплуатации.

---

## 🎙️ ENG SCRIPT

### Voice design
Female contralto, late 30s, hushed-intimate confessional — as if telling you a secret in a dim room. Slightly slower than VOYAGER (~145 WPM effective) with longer pauses on the existential beats. Slight breathiness, intimate proximity, speaking almost into your inner ear. On the meta-twist (S17) the voice drops to a near-whisper. ASMR-adjacent — lean into it.

### ElevenLabs v3 settings
- **Model:** `eleven_v3`
- **Voice:** female contralto (same as VOYAGER / INNER MONOLOGUE for series consistency)
- **Stability:** 35
- **Style:** 40
- **Speed:** 1.0
- **Speaker boost:** ON

### Script (with v3 tags)

```
[whispered, intimate] There is an alien intelligence on Earth. [pause] You can visit it in an aquarium.

[soft] It didn't come from space. [pause] It came from the same place we did — [whispered] and then went the other way.

[narrator] Six hundred million years ago, our family tree split. [pause] On one side: us. [pause] On the other — this.

[soft] It built a mind from scratch. [whispered] Nothing like ours.

[narrator] Half a billion neurons. [pause] But two-thirds of them [whispered] are not in its head.

[narrator, dramatic] They're in its arms.

[soft] Each arm can taste what it touches. [pause] Each arm [whispered] can decide on its own.

[narrator] It changes color [pause] to match a world [whispered] it cannot even see in color.

[soft] It edits its own genetic code — [pause] rewriting its nervous system [whispered] faster than evolution should allow.

[narrator] It opens jars. [pause] It solves mazes. [whispered] It remembers your face.

[pause]

[soft, slow] And then — [pause] it lives barely two years.

[narrator] The mother lays her eggs, [pause] stops eating, [soft] and guards them in the dark.

[whispered] She dies [pause] as they hatch. [soft] She will never meet them.

[narrator, slow] So everything it learns, [pause] it learns alone. [whispered] And takes with it.

[soft] We share an ancestor. [pause] That tiny, forgotten thing.

[narrator, slow] From the same beginning, [pause] the universe built a mind — [whispered] twice.

[whispered, intimate] And one of them [pause] just watched you [breath] through the glass.

[whispered, almost imperceptible] It will never know [pause] you wondered about it too.
```

**Word count:** ~225 words → ≈90 sec at 145 WPM × 1.0 speed = fits the 90 sec window.

---

## 🎬 18 SCENES

> Each scene runs exactly 5 sec. NBP generates the still **with Style DNA Kit references**; Veo 3.1 animates it via **first/last-frame chaining**. CapCut carries ONLY micro-typography (tickers/kickers ≤28pt) — no big text slabs. Смысл несут голос + анимированный визуал.

---

### SCENE 1 (0:00–0:05) — HOOK

**Line:** *"There is an alien intelligence on Earth. You can visit it in an aquarium."*

**NBP Still (refs: `palette_plate, lighting_plate, creature_sheet, motif_sheet`):**
> Match refs. Compose: extreme close-up of a single octopus eye (horizontal dumbbell pupil) filling the upper-mid frame, emerging from abyssal black; a faint sheet of aquarium glass between us and the eye, one human handprint smudge softly visible on the glass at lower-left; bioluminescent teal catch-light in the pupil. Lower 35% and upper 18% empty void-black for overlay. No text anywhere.

**Veo 3.1 (chaining):** `first=still_S1`, `last=still_S2`.
> The pupil slowly dilates; a single caustic ray drifts across the eye; at 0:03 the camera begins an almost imperceptible pull-back so the eye becomes one point in a wider darkness → preps S2. Faint chromatophore-violet pulse ripples once across surrounding skin.

**CapCut (minimal):** только моно-тикер снизу `GODFREY-SMITH · 2016` (JetBrains Mono 22pt, opacity 55%, lower 6%). ❌ Никакого крупного заголовка — хук несёт голос.

---

### SCENE 2 (0:05–0:10) — NOT FROM SPACE

**Line:** *"It didn't come from space. It came from the same place we did — and then went the other way."*

**NBP Still (refs: `palette_plate, lighting_plate`):**
> Match refs. Compose: deep abyssal field; a faint bone-cream hairline thread of light enters from the bottom and forks into two diverging paths heading to opposite top corners; the void around is empty. Upper 20% / lower 25% empty for overlay. No text.

**Veo 3.1 (chaining):** `first=still_S2`, `last=still_S3`.
> The single thread of light travels upward and, at 0:03, splits into two diverging lines that drift apart → morphs into the family-tree fork of S3. Slow lateral drift left-to-right.

**CapCut:** kicker сбоку `same origin` (Inter Light italic 26pt, opacity 70%). Один глиф.

---

### SCENE 3 (0:10–0:15) — THE SPLIT

**Line:** *"Six hundred million years ago, our family tree split. On one side: us. On the other — this."*

**NBP Still (refs: `palette_plate, motif_sheet`):**
> Match refs. Compose: a minimal Saul-Bass-style evolutionary fork — two thin bone-cream lines diverging from a single node low-center; left branch ends in a faint human-head silhouette, right branch ends in a faint octopus silhouette; at the fork node a single blood-red `#7A1B1B` dot. Abyssal void around. Upper 25% / lower 30% empty. No text, no numbers.

**Veo 3.1 (chaining):** `first=still_S3`, `last=still_S4`.
> The two branches slowly draw outward from the red node; the octopus-side branch glows brighter and the camera drifts toward it → preps S4. The red node pulses once.

**CapCut (инфографика как изображение):** число «600 млн лет» НЕ пишем крупно — его несёт расходящееся древо. Только моно-тикер `~600 MILLION YEARS · LAST COMMON ANCESTOR` (22pt, opacity 55%, lower 6%).

---

### SCENE 4 (0:15–0:20) — A MIND FROM SCRATCH

**Line:** *"It built a mind from scratch. Nothing like ours."*

**NBP Still (refs: `palette_plate, lighting_plate, creature_sheet`):**
> Match refs. Compose: the full octopus suspended in abyssal black, body soft-focus, faint bioluminescent teal neural glow tracing through its form like a diffuse map; single caustic key light from above. Upper 20% / lower 28% empty. No text.

**Veo 3.1 (chaining):** `first=still_S4`, `last=still_S5`.
> The teal neural glow slowly intensifies and concentrates; the octopus drifts and rotates a few degrees; at 0:03 the glow begins migrating outward toward the arms → preps S5.

**CapCut:** kicker `a different kind of mind` (Inter Light italic 26pt, opacity 70%).

---

### SCENE 5 (0:20–0:25) — HALF A BILLION NEURONS

**Line:** *"Half a billion neurons. But two-thirds of them are not in its head."*

**NBP Still (refs: `palette_plate, creature_sheet`):**
> Match refs. Compose: the octopus seen so the small central brain region glows faint teal but DIM, while a vast diffuse cloud of teal points spreads down into the arms (visually obvious that most of the glow is NOT in the head). Austere, diagram-like. Upper 25% / lower 30% empty. No text, no numbers.

**Veo 3.1 (chaining):** `first=still_S5`, `last=still_S6`.
> The dim head-glow holds; the arm-glow swells and brightens dramatically over 5 sec (the "2/3" lives here) → preps the S6 reveal. Subtle camera push toward the arms.

**CapCut (данные-визуал):** долю несёт распределение свечения. Только тикер `~500,000,000 NEURONS · HOCHNER 2012` (22pt, opacity 55%).

---

### SCENE 6 (0:25–0:30) — IN ITS ARMS  *(reveal)*

**Line:** *"They're in its arms."*

**NBP Still (refs: `palette_plate, creature_sheet, motif_sheet`):**
> Match refs. Compose: extreme close-up of a single octopus arm curling toward camera, suckers in sharp focus, bright teal neural threads running visibly along the arm's length. Rest in void-black. Upper 18% / lower 28% empty. No text.

**Veo 3.1 (chaining):** `first=still_S6`, `last=still_S7`.
> The arm coils with independent, searching motion; teal threads pulse along it like firing neurons; a single sucker reaches toward a point of light → preps S7 (touch/taste). Hard, confident motion — this is a reveal beat.

**CapCut:** kicker `the arms think` (Inter Light italic 26pt, opacity 75%). Kinetic type-in on "think".

---

### SCENE 7 (0:30–0:35) — TASTE BY TOUCH

**Line:** *"Each arm can taste what it touches. Each arm can decide on its own."*

**NBP Still (refs: `palette_plate, creature_sheet, motif_sheet`):**
> Match refs. Compose: macro of one sucker pressed against a pale glass-chrome surface; from the contact point, faint bone-cream concentric "taste" ripples bloom outward (sensing); teal micro-glow inside the sucker rim. Upper 22% / lower 28% empty. No text.

**Veo 3.1 (chaining):** `first=still_S7`, `last=still_S8`.
> The sucker presses and releases; taste-ripples bloom at contact (0:01, 0:03); the surface it touches begins shifting hue → preps S8 (color change). Slow drift.

**CapCut:** тикер `VAN GIESEN ET AL. · CELL · 2020` (22pt, opacity 55%). No headline.

---

### SCENE 8 (0:35–0:40) — COLOR IT CANNOT SEE

**Line:** *"It changes color to match a world it cannot even see in color."*

**NBP Still (refs: `palette_plate, creature_sheet`):**
> Match refs. Compose: a patch of octopus skin filling the frame, chromatophores mid-shift — ochre, violet and teal blooming across the surface in organic stipple. Soft caustic light. Upper 20% / lower 28% empty. No text.

**Veo 3.1 (chaining):** `first=still_S8`, `last=still_S9`.
> Waves of color ripple across the skin (chromatophores firing) over the full 5 sec — mesmerizing, slow; at 0:04 the color pattern resolves into thread-like lines → preps the RNA strand of S9.

**CapCut:** kicker `colorblind` (Inter Light italic 26pt, opacity 70%) — единственное слово, контраст с буйством цвета.

---

### SCENE 9 (0:40–0:45) — REWRITING ITSELF

**Line:** *"It edits its own genetic code — rewriting its nervous system faster than evolution should allow."*

**NBP Still (refs: `palette_plate, motif_sheet`):**
> Match refs. Compose: an abstract bone-cream + teal double-helix-like strand floating in void, with several "letters"/rungs glowing and visibly re-arranging (implied editing) — abstract, not literal text. Upper 25% / lower 30% empty. No actual letters/numbers.

**Veo 3.1 (chaining):** `first=still_S9`, `last=still_S10`.
> Rungs of the strand flicker and swap positions (RNA editing); the strand slowly coils tighter; at 0:04 it dissolves toward a single point → preps S10. Faint chromatic aberration.

**CapCut:** тикер `LISCOVITCH-BRAUER ET AL. · CELL · 2017` (22pt, opacity 55%).

---

### SCENE 10 (0:45–0:50) — IT REMEMBERS YOU

**Line:** *"It opens jars. It solves mazes. It remembers your face."*

**NBP Still (refs: `palette_plate, lighting_plate, creature_sheet, motif_sheet`):**
> Match refs. Compose: the octopus pressed to the inside of aquarium glass, one eye fixed directly at camera; a soft human-face reflection ghosted faintly on the glass between us; one arm reaching toward the handprint smudge. Upper 18% / lower 25% empty. No text.

**Veo 3.1 (chaining):** `first=still_S10`, `last=still_S11`.
> The eye tracks slightly as if following the viewer; the reaching arm touches the glass at 0:03; the ghost-reflection of a human face steadies. **Hold tension** → hard cut to S11.

**CapCut:** kicker `it remembers your face` (Inter Light italic 28pt, opacity 80%, kinetic type-in). Тикер `FINN ET AL. · CURRENT BIOLOGY · 2009`.

---

### SCENE 11 (0:50–0:55) — BARELY TWO YEARS  *(the turn — HARD CUT in)*

**Line:** *"And then — it lives barely two years."*

**NBP Still (refs: `palette_plate, lighting_plate, creature_sheet`):**
> Match refs. Compose: the octopus small and alone in a vast empty abyss, the single caustic ray narrowing around it like a closing spotlight; most of the frame deep void-black. Upper 25% / lower 35% empty. No text.

**Veo 3.1 (chaining):** `first=still_S11`, `last=still_S12`.
> The light slowly narrows; the octopus settles lower; the teal glow dims a notch → preps S12. Very slow, heavy motion. Music drops here (see audio).

**CapCut:** тикер `LIFESPAN · ~1–2 YEARS` (22pt, opacity 55%). One quiet glyph.

---

### SCENE 12 (0:55–1:00) — THE MOTHER

**Line:** *"The mother lays her eggs, stops eating, and guards them in the dark."*

**NBP Still (refs: `palette_plate, lighting_plate, creature_sheet, motif_sheet`):**
> Match refs. Compose: the octopus curled protectively over a hanging cluster of pearl-like translucent eggs glowing faint bone-cream; she is in soft shadow, one eye barely catching the light. Tender, still. Upper 22% / lower 28% empty. No text.

**Veo 3.1 (chaining):** `first=still_S12`, `last=still_S13`.
> The eggs shimmer faintly; the mother's body barely moves (vigil); her glow continues to dim slowly → preps S13. Almost no motion — stillness as grief.

**CapCut:** kicker `she stops eating` (Inter Light italic 26pt, opacity 70%).

---

### SCENE 13 (1:00–1:05) — SHE DIES AS THEY HATCH  *(death beat)*

**Line:** *"She dies as they hatch. She will never meet them."*

**NBP Still (refs: `palette_plate, lighting_plate, motif_sheet`):**
> Match refs. Compose: the egg cluster now releasing tiny drifting paralarvae (specks of light rising), while below, the mother's silhouette fades into void; a single blood-red `#7A1B1B` pulse glows once where her eye was. Upper 25% / lower 30% empty. No text. Dignified, never graphic.

**Veo 3.1 (chaining):** `first=still_S13`, `last=still_S14`.
> Tiny hatchlings drift upward as points of light; the mother's glow fades to black with one final red pulse at 0:03 → **hard cut** to S14. Music cuts to near-silence here.

**CapCut:** тикер `WANG & RAGSDALE · J EXP BIOL · 2018` (22pt, opacity 55%). No kicker — let it breathe.

---

### SCENE 14 (1:05–1:10) — IT LEARNS ALONE  *(HARD CUT in)*

**Line:** *"So everything it learns, it learns alone. And takes with it."*

**NBP Still (refs: `palette_plate, creature_sheet`):**
> Match refs. Compose: a single small octopus alone in void, faint teal knowledge-glow held entirely inside its own body (nothing passed outward); no parent, no others. Upper 25% / lower 30% empty. No text.

**Veo 3.1 (chaining):** `first=still_S14`, `last=still_S15`.
> The lone octopus's internal glow flickers — learning — but none of it leaves its body; at 0:04 the camera pulls back to reveal total emptiness around it → preps S15.

**CapCut:** kicker `no one taught it` (Inter Light italic 26pt, opacity 70%).

---

### SCENE 15 (1:10–1:15) — WE SHARE AN ANCESTOR

**Line:** *"We share an ancestor. That tiny, forgotten thing."*

**NBP Still (refs: `palette_plate, motif_sheet`):**
> Match refs. Compose: extreme macro of a minuscule, simple worm-like ancient creature (soft, abstract, almost a smudge of light) centered in void — humble, primordial. Faint bone-cream glow. Upper 25% / lower 30% empty. No text.

**Veo 3.1 (chaining):** `first=still_S15`, `last=still_S16`.
> The tiny creature pulses faintly; two threads of light begin to grow out of it in opposite directions → preps the "mind built twice" of S16.

**CapCut:** kicker `~600 million years ago` (Inter Light italic 24pt, opacity 65%).

---

### SCENE 16 (1:15–1:20) — A MIND, TWICE

**Line:** *"From the same beginning, the universe built a mind — twice."*

**NBP Still (refs: `palette_plate, motif_sheet`):**
> Match refs. Compose: two glowing forms mirrored across the frame — left a faint human-brain glow, right a faint distributed octopus-glow — both grown from one shared point of light at center. Symmetry. Upper 25% / lower 28% empty. No text.

**Veo 3.1 (chaining):** `first=still_S16`, `last=still_S17`.
> Both minds glow up in parallel; at 0:04 the octopus side rushes forward toward camera → **hard cut** to the eye of S17 (the meta-twist).

**CapCut:** kicker `twice` (Inter Light italic 28pt, opacity 80%, kinetic type-in). One word.

---

### SCENE 17 (1:20–1:25) — IT WATCHED YOU  *(META-TWIST — HARD CUT in)*

**Line:** *"And one of them just watched you — through the glass."*

**NBP Still (refs: `palette_plate, lighting_plate, creature_sheet, motif_sheet`):**
> Match refs. Compose: the octopus eye filling the frame again (callback to S1), now with a single blood-red `#7A1B1B` catch-light reflected in the pupil, and a faint reflection of a human face (the viewer) on the glass between. Intimate, unsettling. Upper 18% / lower 25% empty. No text.

**Veo 3.1 (chaining):** `first=still_S17`, `last=still_S18`.
> The pupil contracts as if focusing on YOU; the red catch-light flares once at 0:02; the human-face reflection sharpens then the camera drifts so eye and reflection nearly merge → preps S18. **All music cuts at 0:02** — voice + faint hiss only.

**CapCut:** kicker `through the glass` (Inter Light italic 28pt, opacity 80%). Тикер off.

---

### SCENE 18 (1:25–1:30) — FINAL HOOK

**Line:** *"It will never know you wondered about it too."*

**NBP Still (refs: `palette_plate, lighting_plate, creature_sheet, motif_sheet`):**
> Match refs. Compose: the octopus slowly receding into abyssal black, one arm still resting against the glass over the human handprint, eye dimming; almost all frame is void. Upper 25% / lower 35% empty. No text.

**Veo 3.1 (chaining):** `first=still_S18`, `last=still_S18` (gentle settle, no next scene).
> The octopus drifts back into darkness; the arm slips from the glass at 0:03; the last teal glow fades to void by 0:05. Final breath in audio at 0:04.5.

**CapCut:** kicker `we were both wondering.` (Inter Light italic 26pt, opacity 75%, fades in 0:01, fades out 0:04). Sub-handle/CTA per channel template, lower 8%, opacity 60%.

---

## 🎚️ CAPCUT AUDIO MIX

### 7-track layout

| Track | Content | Level (dB) | Notes |
|---|---|---|---|
| 1 | Voice (ElevenLabs v3 narration) | –6 dB | Primary; intimate close-mic; side-chains all other tracks –5 dB during speech |
| 2 | Music bed (cello + glass-harmonica/waterphone + ambient pad) | –20 dB (–25 under voice) | Sparse; cello drone from S2; glass-harmonica shimmer on wonder beats; piano on S11–S18 |
| 3 | Sub-bass / abyssal pressure drone (28–30 Hz) | –28 dB | Deep-ocean pressure; intimate psychological weight |
| 4 | Foley (hydrophone ambience, water movement, soft bubbles, glass tap, sucker release) | –24 to –28 dB | Per-scene cheat sheet below |
| 5 | Bioluminescent "signal" bed (soft alien chimes, continuous, very low) | –30 dB | The "alien presence" bed; cuts entirely in S11 and S13 |
| 6 | Sharp punctuation beats (glass tap, sucker pop, chime, red-pulse tone) | –14 to –22 dB | The "syntax" of the video — intentional, startling |
| 7 | Voice processing return (ASMR-binaural reverb on whispered passages) | –6 dB | Whispered v3 tags only |

### Side-chain ducking
- **Music (T2)** ducks –5 dB under voice, releases 0.4 s after.
- **Sub-bass (T3)** does not duck.
- **Foley (T4)** ducks –6 dB under voice.
- **Signal bed (T5)** ducks –4 dB under voice; **cuts entirely during S11 and S13**.
- **Punctuation (T6)** does NOT duck — cuts through.

### Reveal beats (silence / drop moments)

| Beat | Treatment |
|---|---|
| S6 (`They're in its arms.`) | At 0:00, a single sucker-pop punctuation (–14 dB) + signal bed swells — the reveal |
| S11 (`barely two years`) | Music drops –10 dB, signal bed (T5) cuts — sudden loneliness |
| S13 (`She dies as they hatch`) | 0:00–0:04 near-silence; only sub-bass + one red-pulse tone at 0:03; all foley/signal cut |
| S17 (whispered `through the glass`) | At 0:02 the red-pulse tone cuts ALL music; voice + faint hiss only for remaining 3 sec |
| S18 (final) | At 0:04.5 all audio fades to near-silence; only a barely-audible final breath |

### Mastering specs
- **Integrated loudness:** −14 LUFS (TikTok standard)
- **True peak:** −1 dBTP max
- **Limiter:** −2 dB threshold, 3:1, slow release
- **Stereo:** Voice mono-centered w/ subtle ASMR-binaural on whispers; music stereo-wide; sub-bass mono-summed <80 Hz
- **Compression:** Voice gentle 2:1 to preserve breath

### Per-scene SFX cheat sheet

| Scene | Primary SFX (T4) | Punctuation (T6) |
|---|---|---|
| S1 | Hydrophone room tone, faint distant whale-ish low moan (–30 dB) | Soft glass tap at 0:02 |
| S2 | Deep water movement | Single low chime at 0:02.5 |
| S3 | Abyssal ambience | Soft "split" chime at 0:03 (the fork) |
| S4 | Water shimmer | — |
| S5 | Signal bed swell | Faint neural-tick pings |
| S6 | Signal bed peak | **Sucker-pop at 0:00 (–14 dB)** — the reveal |
| S7 | Sucker contact/release, taste-bloom whoosh | Soft pop at 0:01 + 0:03 |
| S8 | Smooth tonal sweep as colors ripple | — |
| S9 | Faint digital-organic flutter (RNA editing) | Tick-swaps at 0:01, 0:02.5 |
| S10 | Glass resonance, arm-on-glass squeak at 0:03 | Glass tap at 0:03 |
| S11 | (music drop, signal bed cut) — room pressure only | — |
| S12 | Very quiet vigil ambience | — |
| S13 | (near-silence) sub-bass only | **Red-pulse tone at 0:03 (–18 dB)** |
| S14 | Faint lone ambience | — |
| S15 | Primordial low hum | Single soft pulse at 0:02 |
| S16 | Two mirrored tonal swells | Chime at 0:04 (rush forward) |
| S17 | (music cuts at 0:02) faint hiss | **Red-pulse tone at 0:02 (–16 dB, prominent)** |
| S18 | Final breath at 0:04.5, water settle | Piano note at 0:01 |

---

## 🎞️ CAPCUT TIMELINE BUILD ORDER

1. **Import 18 Veo 3.1 chained clips** (each 5 sec, 9:16 1080×1920, 30 fps) → V1, sequential. 90 sec total. *Because scenes are chained (last/first frame match), most cuts are invisible morphs.*
2. **Import ElevenLabs v3 voice WAV** → A1. Align each line to its 5-sec window; trim head/tail silence.
3. **Apply LUT:** "Abyss" — crush deep blacks, push teal into shadows, keep ochre skin warm, slight desaturation overall. Apply uniformly to V1.
4. **Cuts:** scenes are designed to flow (Veo chaining). Apply **hard cuts** only at S10→S11, S13→S14, S16→S17. Everywhere else: let the chained motion carry; optional 2-frame dissolve only if a seam shows.
5. **S13 death beat:** verify near-silence 1:00–1:04 in the loudness meter.
6. **One global film-grain pass** (10%) + **caustic-shimmer overlay** (subtle, 8%) on V1 — applied ONCE across the whole timeline (not per clip) so grain/shimmer don't jump between scenes.
7. **Subtle vignette** (15% corners) as one adjustment layer.
8. **Chromatic aberration** (1.5%) on S9 (RNA) and S17 (meta-twist) only.
9. **Layer micro-typography** on V2 — tickers/kickers per scene (≤28pt, low opacity). Kinetic type-in on S6/S10/S16. **No big text slabs anywhere.**
10. **Audio mix:** 7 tracks per spec; side-chain ducking; verify S11/S13/S17 drops.
11. **Master:** 1080×1920, 30 fps, H.264, −14 LUFS, −1 dBTP, AAC 256 kbps, ≤50 MB.

---

## 🪝 HOOK VARIANTS (5 — A/B TEST FIRST 3 SEC)

1. **DEFAULT** (intimate): *"There is an alien intelligence on Earth. You can visit it in an aquarium."*
2. **DIRECT** (self-implicating): *"Something in the ocean remembers your face. And it thinks with its arms."*
3. **STAT-FORWARD** (number shock): *"Five hundred million neurons. Two-thirds are in its arms. Meet the closest thing to an alien."*
4. **DARK / EXISTENTIAL**: *"The universe built a mind twice. One of them is not human — and it's watching you."*
5. **META-TWIST UPFRONT**: *"An octopus just watched you through the glass. It will never know you wondered about it too."*

**A/B strategy:** Day 1 → DEFAULT (monitor 3-sec retention). <65% → Day 2 DIRECT. <70% → Day 3 STAT-FORWARD. DARK / META reserved for Reels / YT Shorts reposts. Target: 3-sec retention ≥72%, full-view ≥45%, CTR ≥7%.

---

## 🖼️ TIKTOK COVERS (9:16 1080×1920) — 4 VARIANTS + 1 HERO

> A–D: NBP composition only (NO text in image), typography layered in CapCut/Photoshop. HERO: headline rendered in-frame by NBP.

### 🅰️ COVER A — DEFAULT — "The Eye"
**NBP (refs: `palette_plate, lighting_plate, creature_sheet`):** single octopus eye filling mid-frame from abyssal black, teal catch-light, faint handprint on glass at lower-left; upper 25% / lower 22% empty void for overlay. No text.
**Overlay:** Upper `IT IS WATCHING` / `YOU BACK.` — bone-cream `#D9C9A0`, Druk Wide Bold 104pt, 2 lines, upper third. Lower marker `THE OCTOPUS PARADOX` — chrome-silver `#C8CED2`, JetBrains Mono 26pt, lower 8%.

### 🅱️ COVER B — DIRECT CHALLENGE — "It Remembers You"
**NBP (refs: `palette_plate, creature_sheet, motif_sheet`):** octopus pressed to glass, one eye locked at camera, ghost human-face reflection; empty bands top/bottom. No text.
**Overlay:** `IT REMEMBERS` / `YOUR FACE.` — bone-cream, Druk Wide Bold 100pt, upper third. Marker `CEPHALOPOD COGNITION` — chrome-silver, JetBrains Mono 24pt, lower 8%.

### 🅲 COVER C — STAT-SHOCK — "Two-Thirds"
**NBP (refs: `palette_plate, creature_sheet`):** octopus with dim head-glow and bright arm-glow (the "2/3 in the arms" visual); empty bands. No text.
**Overlay:** `2/3 OF ITS MIND` / `IS IN ITS ARMS.` — bone-cream, Druk Wide Bold 92pt, upper third. Tiny `~500,000,000 NEURONS` — chrome-silver, JetBrains Mono 22pt, below headline.

### 🅳 COVER D — INSTITUTIONAL / CATALOG — "Case File"
**NBP (refs: `palette_plate, motif_sheet`):** aged bone-paper parchment; fine teal line-art octopus diagram center; one arm region warm-glow highlighted; chrome seal upper-right (empty); faint red `#7A1B1B` stamp oval lower-left (empty). No text.
**Overlay:** Header `CASE FILE · OTHER MINDS` — cold teal `#1FB6C9`/`#1E3A5F`, Druk Wide Bold 60pt, top 8%. Red stamp `NON-HUMAN COGNITION` — `#7A1B1B`, JetBrains Mono 24pt. Handwritten `~2 yr lifespan` — Caveat 36pt, 2° tilt. Lower `THE MIND BUILT TWICE` — Druk Wide Bold 54pt. Citation `GODFREY-SMITH (2016)` — JetBrains Mono 18pt, lower 4%.

### 🅷 COVER HERO — HEADLINE RENDERED IN-FRAME
**NBP (refs: `palette_plate, lighting_plate, creature_sheet`):** lower 55% = octopus eye emerging from abyssal black, teal catch-light, faint handprint on glass; upper-mid = a large bold English headline in pure bone-cream `#D9C9A0`, heavy condensed sans (Druk Wide / Anton), all uppercase, crisp, centered, 3 lines:
> THE ALIEN
> IS ALREADY
> HERE
> Tight letter-spacing, flat opaque cream type, no glow. One faint blood-red `#7A1B1B` ember at the bottom edge.
**Headline variants:** 2-line `IT THINKS / WITH ITS ARMS.` · 3-line number `500 MILLION / NEURONS · / NOT HUMAN.` · meta `IT WATCHED / YOU BACK.`
**RU (если нужна кириллица):** `ЧУЖОЙ РАЗУМ / УЖЕ / ЗДЕСЬ` (3 строки); в промпте `bold English headline` → `bold Cyrillic Russian headline`; NBP хуже рендерит кириллицу — 5–6 попыток.

---

## 📲 TIKTOK CAPTION + HASHTAGS

### Primary caption (EN, ~280 chars):
```
The closest thing to meeting an alien isn't in space. It's in the ocean. 🐙
500 million neurons — two-thirds in its arms. It tastes by touch, edits its own
genes, remembers your face… and lives barely two years. We split 600M years ago.
The universe built a mind twice. Which one are you?
```

### Alternative captions
- *(self-test)* "Read this, then look at an octopus. It's looking back — and its mind is nothing like yours. 🐙"
- *(stat)* "2/3 of its brain is in its arms. It thinks with the things it touches. Meet Earth's other mind."
- *(emotional)* "The mother guards her eggs in the dark, stops eating, and dies as they hatch — never meeting them. Everything it learned, it takes with it."

### Hashtags — 5 for launch
`#octopus #ocean #didyouknow #science #fyp`

### Hashtag rotation stacks (follow-up posts)
- Stack B: `#cephalopod #marinebiology #animals #wildlife #fyp`
- Stack C: `#consciousness #evolution #aliens #nature #learnontiktok`

### Pinned comment (post immediately after upload)
> Sources: Godfrey-Smith, *Other Minds* (2016) · van Giesen et al., *Cell* (2020) · Wang & Ragsdale, *J Exp Biol* (2018) · Liscovitch-Brauer et al., *Cell* (2017). Not "smarter" than us — *different*. Intelligence evolved at least twice. 🐙

---

## ✅ PRODUCTION CHECKLIST

- [ ] Generate **Style DNA Kit** (palette / lighting / creature_sheet / motif_sheet) — lock the look once
- [ ] Generate 18 stills via NBP **with references** (no big text in any still)
- [ ] Animate via **Veo 3.1 first/last-frame chaining** (verify `last[N]==first[N+1]`)
- [ ] Verify the 4 anchor motifs travel (neural thread / eye / glass+handprint / red accent)
- [ ] ElevenLabs v3 voice — contralto, stability 35 / style 40, whisper on S17–S18
- [ ] CapCut: micro-tickers/kickers only (≤28pt) — NO Druk Wide slabs in-video
- [ ] Audio: 7 tracks, side-chain, verify S11/S13/S17 drops, S13 near-silence
- [ ] One global grain + caustic pass (not per clip); LUT "Abyss" uniform
- [ ] Hard cuts only S10→S11, S13→S14, S16→S17
- [ ] Master: 1080×1920, 30 fps, −14 LUFS, −1 dBTP, ≤50 MB
- [ ] Covers A–D + HERO; caption + 5 hashtags + pinned comment
- [ ] Moderation pass: no "smarter", no graphic death, no food framing, sources cited

---

## 📚 SERIES CONSISTENCY

- **Format:** 9:16, 90 sec, 18×5 sec, female contralto v3, intimate-confessional.
- **Brand signature:** blood-red `#7A1B1B` exactly 2–3× (S3 / S13 / S17). Bone-cream `#D9C9A0` typographic micro-accent. Fine grain + vignette + single LUT.
- **Per-video signature color:** bioluminescent teal `#1FB6C9` (this is the "Octopus" episode's hue, like neural-blue was Inner Monologue's).
- **Twist DNA:** every video ends with a meta-twist that turns on the viewer. Here: *"one of them just watched you — and it will never know you wondered too."*
- **Restraint guardrails (every video):** all typography is micro (tickers/kickers), the visual carries the data, the voice carries the meaning. Never a wall of on-screen text.
