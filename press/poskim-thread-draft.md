# X thread: poskim analysis (posted 9 Nov 2026)

Posted as a standalone thread from @HalachaBench: https://x.com/HalachaBench/status/2119842194148430254
Tweet ids: 2119842194148430254, 2119842198623568362, 2119842203300433966, 2119842208870441180, 2119842212880298416, 2119842216109920659.

## 1 — attach charts/citations-radar.png
Who do AI models cite when asked halacha?

Share of 288 answers naming Rav Moshe Feinstein: Gemini 33%, Claude 30%, Grok 14%. Every GPT model: 7% or less.

Same gap for R. Shlomo Zalman and Shemiras Shabbos. GPT's poskim stop at Shulchan Aruch, Rema, Mishnah Berurah. Thread.

## 2 — attach charts/poskim-map.png
And on the rulings themselves? Every rubric position in HashkafaBench is anchored to the poskim who hold it. That puts R. Moshe Feinstein, R. Ovadia Yosef, R. Shlomo Zalman, the Mishnah Berurah and others in the same space as the 13 models. Here is the map.

## 3 — attach charts/poskim-heatmap.png
Closest model to each posek's positions:

Mishnah Berurah: GPT-6 Astra
Shulchan Aruch, Rema: GPT-6 Sol
R. Moshe Feinstein: Claude Opus 5.5
R. Shlomo Zalman, R. Ovadia: Claude Fable 5.1
Shemiras Shabbos: Gemini 3.8 Flash = GPT-6.1 Terra

Claude/Gemini: lenient poskim. GPT: codes.

## 4 — attach charts/style-dendrogram.png
One more, no LLM anywhere: Burrows's Delta, the classic authorship-attribution test, on the 150 most common words of each model's answers.

The models cluster perfectly by lab. GPT-6 Astra and GPT-6.1 Sol are nearly the same writer. Grok sits nearest the Claude branch.

## 5 — no image
Caveats:
- Descriptive, not pre-registered.
- One answer per model per question.
- A posek's position comes from the questions where our rubric names him. R. Ovadia and R. Shlomo Zalman are mostly at lenient anchors, so "close to R. Ovadia" partly means "lenient where he is".

## 6 — no image
Nobody cites R. Ovadia Yosef (under 5% for every model), consistent with the Ashkenazi asker.

Data, charts and the per-model distances with bootstrap intervals: github.com/HalachaBench/hashkafa-bench-results

Not psak. Rubric anchors not yet reviewed by rabbis.
