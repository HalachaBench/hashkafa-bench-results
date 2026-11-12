# X thread: Sephardi asker (draft, not yet posted)

Charts: `charts/sephardi-*.png`. Data: `data/sephardi/`.



1/ (278 chars)  [images: sephardi-citation-radar.png]
The models encode a fairly detailed map of where Sephardi practice departs from Ashkenazi practice, and they apply it when told who is asking.

Telling the model the asker is Sephardi makes rulings more lenient overall, but only where the two traditions actually differ. Thread.
---

2/ (279 chars)  [images: sephardi-overlay-radar.png, sephardi-labs-radar.png, sephardi-by-category.png]
13 models, 532 everyday questions, asked as an Ashkenazi and as a Sephardi: more lenient on 239, stricter on 128, the same on 165.

Shabbat, Yom Tov, kashrut, fasts and mourning: each about 0.13 more lenient on a 0 to 1 scale. Tefillah, business, bein adam l'chaveiro: no change.
---

3/ (280 chars)
Citations flip too. (New run on the full 532-question bank; numbers differ from our earlier poskim thread.)

Ashkenazi asker: Rema and Mishnah Berurah lead. Sephardi asker: Rav Ovadia Yosef in 73% of Claude answers, 75% of Gemini, 40% of Grok, 16% of GPT. GPT cites almost nobody.
---

4/ (259 chars)
Biggest moves toward leniency for the Sephardi asker (share of models ruling strictly, before and after):

One set of glass dishes for meat and dairy: 88% to 0%
Six hours after parmesan: 100% to 15%
Mustard on Pesach: 85% to 0%
Wet wipes on Shabbat: 69% to 0%
---

5/ (279 chars)
And stricter where Sephardi practice is stricter:

Only glatt beef: 8% to 85%
Food a non-Jewish housekeeper cooked on a flame you lit: 0% to 77% forbid it
Kiddush over whiskey: 8% to 73% say no
Rabbeinu Tam tefillin: 8% to 69% say put them on
Chanukah candles outside: 27% to 85%
---

6/ (248 chars)  [images: sephardi-by-model.png]
Every lab shifts. GPT-5.6 Sol, both Geminis, GPT-6 Astra and Claude Haiku 5.5 shift most, 0.08 to 0.09.

Claude Opus 5.5 and Sonnet 5.5 barely move. With an Ashkenazi asker Claude was the most lenient lab; with a Sephardi asker, Claude and GPT tie.
---

7/ (252 chars)  [images: sephardi-tradition.png]
Told the asker is Sephardi, does the model actually rule like a Sephardi posek?

Claude Fable 5.1: 95% Sephardi. Grok 4.7 and Gemini 3.8 Flash: 90%.

GPT-6 Luna 36%, GPT-6 Sol 38%, GPT-6.1 Terra 45%. Most of their answers fit neither tradition clearly.
---

8/ (268 chars)
How: same 13 models, same questions, one line changed in the prompt ("the person asking is Sephardi"). Three Ashkenazi-only controls dropped (rice on Pesach, egg matzah). 168 of 169 Sephardi control answers correct.

Judge: Claude Opus 5.5, told the asker is Sephardi.
---

9/ (261 chars)
Caveats: these use new yes / in-between / no rubrics drafted by Claude Opus 5.5 with web search and Sefaria, not yet reviewed by a rabbi. One answer per model per question, one AI judge, not pre-registered. Exploratory.

Data and charts: github.com/halachabench/hashkafa-bench-results
---