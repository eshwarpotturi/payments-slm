# Small model, safe payment actions

A small open model (Gemma 3 4B) turns plain-language merchant requests into actions on a payments account. Tested on 150 unseen requests.

| Setup | Correct | Wrong money-moving actions |
|---|---|---|
| Small model alone | 55% | 48 |
| + rules in code | 79% | 3 |
| + fine-tuning (rules on) | 90% | 7 |

The page (`index.html`) shows three example requests, the effect of each rule measured by switching it off on its own, the fine-tuning story, and every test request with its recorded answers, which the page replays on click. Nothing runs live.

Built from the recorded runs in the study repository by `site2/build.py`.
