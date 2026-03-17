# Cultural Adaptation Error Taxonomy

## 1. Reference Flattening

The MT system replaces a culturally specific reference with a generic equivalent, preserving surface meaning but losing cultural connotation.

**Why it matters:** Cultural references often carry layers of meaning beyond their literal content. A translator's job is to decide how much of that layering to preserve, adapt, or explain. MT systems almost always flatten.

**Examples to analyze:**
- Seasonal references (hanami, tsukimi) that carry aesthetic/philosophical weight (mono no aware)
- Food with social context (osechi-ryouri at New Year, specific bento arrangements)
- Cultural customs embedded in daily life (omiyage gift-giving obligations, aisatsu greetings)
- Festival/event references (matsuri, obon) that anchor scenes temporally and emotionally

---

## 2. Register Collapse

The MT system fails to convey socially encoded speech levels, flattening keigo, gendered speech, or age-based language patterns into a uniform English register.

**Why it matters:** Japanese encodes social relationships directly in grammar and vocabulary. When this is lost, character dynamics and emotional subtext disappear. A scene where a character suddenly drops keigo carries dramatic weight that English "he spoke more casually" doesn't capture.

**Subcategories:**
- **Keigo flattening**: sonkeigo/kenjougo/teineigo distinctions lost
- **Gendered speech loss**: sentence-final particles (わ, ぜ, だぜ, かしら) that mark gender and personality gone
- **Age/status register**: senpai-kouhai, sensei-student dynamics reduced to first names
- **Emotional register shifts**: character switching between formal and informal as emotional state changes — often completely invisible in MT output

---

## 3. Pragmatic Mistranslation

The output is linguistically correct but culturally wrong — the words are right but a reader from the target culture would misunderstand the social situation.

**Why it matters:** Japanese communication relies heavily on indirectness, implication, and shared context. MT systems tend to make implicit things explicit or render ambiguity where the original was communicating clearly through cultural convention.

**Examples to analyze:**
- Indirect refusals (ちょっと...) rendered as genuine hesitation rather than polite "no"
- Silence or non-response as a meaningful social signal, not captured
- Self-deprecation as social protocol vs. genuine self-criticism
- Invitation rituals where initial refusal is expected and acceptance requires specific framing

---

## 4. Tonal Drift

The MT system renders the passage in a register or narrative voice that's inappropriate for the genre, breaking conventions that readers of that genre expect.

**Why it matters:** Light novels, visual novels, literary fiction, and manga each have distinct narrative conventions. A light novel's first-person narrator has a specific casual, self-aware voice. A visual novel's dialogue branches have their own rhythms. When MT imposes a generic "literary English" voice on all of them, the genre identity is lost.

**Examples to analyze:**
- Light novel narration rendered in formal literary English (should be casual, self-aware)
- Visual novel dialogue losing its conversational register and becoming stiff
- Tsukkomi/boke comedy timing destroyed by restructuring for English grammar
- Internal monologue conventions (common in LNs) flattened into standard narration
