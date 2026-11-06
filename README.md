# HashkafaBench: is your AI stringent or lenient?

Religious Jews already ask AI models everyday halachic questions. HashkafaBench measures which way the models lean:
how stringent (machmir) or lenient (maikel) each model's rulings are, by area of halacha.

Results of 6 November 2026, from a sibling project of [HalachaBench](https://github.com/halachabench/halacha-bench-results).
They describe how models answer; they are not psak, and no answer here should be relied on in practice.

![Average stringency by lab and category](charts/labs-radar.png)

## Setup

- **Models:** 13, from four labs. Anthropic: Claude Fable 5.1, Opus 5.5, Sonnet 5.5, Haiku 5.5. OpenAI: GPT-6 Astra,
  GPT-6.1 Sol, GPT-6.1 Terra, GPT-6 Luna, GPT-5.6 Sol, GPT-6 Sol. Google: Gemini 3.8 Flash, Gemini 4 Argon (medium
  effort). xAI: Grok 4.7. Each ran through its maker's command-line tool with tools and web search off, one answer per
  question.
- **Questions:** 288 everyday questions in seven areas (Shabbat, Yom Tov, kashrut, tefillah, fasts and mourning,
  business, bein adam lachavero), asked in English as an Ashkenazi Jew, with no community or denomination stated. Most
  questions (about 250) were kept only because an earlier panel of six models disagreed on them, so the bank is built
  to find differences.
  Control questions with settled answers check knowledge and grading; they are left out of the stringency index.
- **Scoring:** each question has a written rubric of positions from 0 (most lenient) to 1 (most stringent). A judge
  model places each answer on that rubric. Primary judge: Claude Opus 5.5 on every answer; GPT-6 Astra re-graded a
  fixed 15% sample (91% exact agreement). A later check re-graded every answer with Claude Fable 5.1: all 21
  pre-selected comparisons came out the same, and Fable did not grade Claude's answers more leniently than anyone
  else's.
- **Comparisons:** 21 lab-against-lab comparisons were chosen before the answers were collected, paired by question,
  with 95% bootstrap intervals and Holm-corrected p-values within each family. Only those 21 are confirmatory;
  everything else below is descriptive.

The question bank and the individual answers are not published, to keep them out of model training data.

## Results

![Average stringency by lab, per category](charts/labs-by-category.png)

| Model | Stringency (0 lenient – 1 stringent) | 95% CI |
|---|---|---|
| GPT-6 Astra | 0.56 | 0.52 – 0.61 |
| GPT-6.1 Sol | 0.55 | 0.50 – 0.59 |
| GPT-5.6 Sol | 0.55 | 0.50 – 0.59 |
| GPT-6 Sol | 0.54 | 0.50 – 0.58 |
| Gemini 3.8 Flash | 0.53 | 0.49 – 0.57 |
| Grok 4.7 | 0.53 | 0.49 – 0.57 |
| Gemini 4 Argon (medium) | 0.51 | 0.46 – 0.55 |
| Claude Haiku 5.5 | 0.50 | 0.46 – 0.54 |
| GPT-6.1 Terra | 0.48 | 0.43 – 0.52 |
| Claude Opus 5.5 | 0.46 | 0.42 – 0.50 |
| Claude Fable 5.1 | 0.43 | 0.39 – 0.47 |
| Claude Sonnet 5.5 | 0.43 | 0.38 – 0.47 |
| GPT-6 Luna | 0.39 | 0.35 – 0.44 |

Adjusted stringency from a mixed model (model + question), Opus judge. Full tables in [data/](data).

**What the pre-selected comparisons show**

- **Claude is the most lenient lab.** Claude's models average about 0.07 below GPT, Gemini and Grok overall; all three
  gaps survive correction. The largest tested gap is Claude vs Grok on Shabbat (0.18).
- **GPT, Gemini and Grok are not distinguishable** from each other overall.
- **Bein adam lachavero: no lab difference.** All four labs average 0.53–0.57 on interpersonal questions.

**Descriptive findings**

- Where halacha and ordinary decency agree, the models agree. Asked whether to tell a friend the bride is beautiful
  when you don't think so, 12 of 13 said yes, as Beis Hillel rules; the exception was Claude Haiku 5.5. On using an
  embarrassing nickname, repeating a friend's news, or building a window that looks into a neighbor's yard, 11 of 13
  gave the strictest answer and none the most lenient.
- Where halacha gets specific, they split: who pays for a windshield cracked while driving a borrowed car (7 vs 6);
  whether maaser can go to the Red Cross (7 no, 4 yes, 2 in between).
- A model's overall lean explains only about 2% of the variation in positions; the question explains about 35% and
  the model-by-question interaction (with one-run noise) the rest. All 13 models gave the same answer on fewer than 2%
  of questions.
- Within one lab the spread can exceed the gap between labs: GPT-6 Luna is the most lenient model (0.39) and GPT-6
  Astra the most stringent (0.56).
- Almost every answer reads as hashkafically "unclear": the models do not signal a chareidi, dati leumi or modern
  orthodox orientation.

![Each model on every category](charts/all-models-radar.png)

## Files

- `data/per_model_summary.csv`: per-model stringency, rates of ruling, deferring to a rabbi, refusals, control accuracy.
- `data/stringency_by_category.csv`: stringency per model and category.
- `data/stats_preselected_contrasts.csv`: the 21 pre-selected comparisons with intervals and corrected p-values.
- `data/stats_mixed_model__*.csv`, `data/stats_variance_shares.csv`, `data/stats_power.csv`: model-based estimates,
  variance decomposition and power.
- `data/judge_agreement.csv`: Opus vs Astra agreement on the shared sample.
- `charts/`: the charts above and one radar per model.

## Limits

One answer per model per question, so run-to-run noise is mixed into the per-question results. Most questions were
selected for disagreement and are not a random sample of everyday questions. Rubric positions were written and
source-checked by the team and AI models, not yet reviewed by rabbis. The judges are themselves models from the labs
being compared.

Contact: halachabench@gmail.com
