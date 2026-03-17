# Cultural Adaptation Error Analysis for Japanese-English Literary MT

An analysis of how current machine translation systems handle cultural adaptation in Japanese fiction — comparing MT output against professional human translations to identify systematic cultural failure modes that standard automatic metrics miss.

## Motivation

Literary translation isn't just linguistic conversion — it requires cultural mediation. Translators make hundreds of decisions per text about when to preserve foreign cultural elements, when to adapt them for the target audience, and how to handle language that's deeply entangled with cultural meaning (wordplay, social register, genre conventions).

Current MT systems (GPT-4, Claude, TranslateGemma) produce increasingly fluent output, but their cultural adaptation ability remains poor. Standard evaluation metrics like COMET and MetricX were designed for news/general domain text and don't capture cultural adaptation quality.

This project investigates:
- **What kinds of cultural adaptation errors do MT systems make on Japanese fiction?**
- **Are these errors systematic and predictable by passage type?**
- **Do standard automatic metrics detect them?**

## Error Taxonomy

I'm developing a taxonomy of cultural adaptation failure modes:

| Category | Description | Example |
|----------|-------------|---------|
| **Reference flattening** | Culturally specific references stripped of connotation | *hanami* → "flower viewing" (loses associations with impermanence, seasonal awareness) |
| **Register collapse** | Loss of socially encoded speech levels | *keigo* hierarchy flattened to uniform English register, losing character relationship dynamics |
| **Pragmatic mistranslation** | Linguistically correct but culturally wrong | Indirect Japanese refusal rendered as genuine ambiguity rather than clear social signal |
| **Tonal drift** | Genre-inappropriate narrative voice | Light novel narrator rendered in formal literary English; VN dialogue losing its conversational register |

## Method

1. **Corpus selection**: Passages from professionally translated Japanese fiction — literary novels, light novels (e.g., Monogatari series, Spice and Wolf), visual novel scripts — chosen for cultural density (dialogue with social hierarchy, cultural references, humor, wordplay)

2. **MT generation**: Each passage run through GPT-4, Claude, Google Translate, and TranslateGemma (12B, open weights)

3. **Annotation**: For each passage, document:
   - Source cultural phenomenon (what's culturally loaded in the passage)
   - Professional translator's handling (what adaptation strategy they chose)
   - Each MT system's handling (what went wrong, which error category)

4. **Metric comparison**: Run COMET and BERTScore on MT outputs. Compare metric rankings against cultural adaptation quality judgments to test whether metrics are blind to cultural errors.

## Corpus

Passages are selected from works where cultural adaptation decisions are central:

- **Literary fiction**: Haruki Murakami novels (translations by Jay Rubin, Philip Gabriel)
- **Light novels**: Monogatari series (Ko Ransom), Spice and Wolf (Paul Starr)
- **Visual novels**: Steins;Gate, Fate/stay night (comparing fan and official localizations)

Focus on passage types where cultural adaptation is most challenging:
- Dialogue scenes with social hierarchy / register shifts
- Humor dependent on cultural knowledge or wordplay
- Narration with embedded cultural references or aesthetic sensibility
- Scenes where language itself carries the meaning (puns, double readings)

## Repository Structure

```
cultural-mt-analysis/
├── README.md
├── data/
│   ├── passages/          # Selected passages with source info
│   └── annotations/       # Error annotations per passage per system
├── analysis/
│   ├── error_taxonomy.md  # Detailed taxonomy with examples
│   └── metric_comparison/ # COMET/BERTScore vs cultural judgments
└── notes/
    └── observations.md    # Running notes and patterns
```

## Status

🟡 **In progress** — Currently in the passage selection and initial annotation phase.

## Related Work

- Karpinska & Iyyer (2023). "Large Language Models Effectively Leverage Document-level Context for Literary Translation, but Critical Errors Persist." WMT 2023.
- Karpinska et al. (2022). "Exploring Document-Level Literary Machine Translation with Parallel Paragraphs from World Literature." EMNLP 2022.
- Zhang et al. (2025). "How Good Are LLMs for Literary Translation, Really?" NAACL 2025.
- Google Translate Research (2026). "TranslateGemma Technical Report."

## Contact

Weidi Li — weidili92@gmail.com
