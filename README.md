Econ 3916 PS2: The Survey That Wasn't Random

A simulation study of how a survey redesign turned a true satisfaction improvement of 0.10 points into an apparent improvement of 0.70 points, and why neither a bigger sample nor covariate reweighting fixes it.

Notebook: Econ_3916_PS2.ipynb (seeded, reruns identically)

Key findings
Non-response bias: response depends on satisfaction itself; after the redesign, users who would score 5 answered 65% of the time and users who would score 2 answered 0.5% of the time.
Bootstrap intervals are precise but wrong: they cover the true mean 0% of the time across 2,000 repeated surveys, while covering it ~95% under random sampling.
More data doesn't help: a 100x larger survey cuts the noise by 10x but leaves the bias at ~0.61 points.
IPW on engagement and support tickets fails (gap 0.68 vs true 0.10), because response is missing not at random.
The rewritten slide

Satisfaction after the redesign: what the survey can and cannot tell us

What it supports: people who chose to answer were happier after the redesign. Their average rose from 3.60 to 4.30, +0.70 points (95% CI 0.68 to 0.73).

What it does not support: "users are 0.7 points happier." After the redesign fewer people answered (15% vs 27%), and the new prompt is answered mostly by satisfied users. The interval above covers sampling noise only, not who stayed silent. A simulation calibrated to our numbers, with a true improvement of just 0.10, reproduces this slide almost exactly. Reweighting on engagement and support tickets barely moves the gap (0.68), and a bigger survey would only tighten the interval around the same wrong number. The redesign may have helped a little; this survey cannot tell us how much.

The fix: send the same survey invitation to a random sample of users before and after, and follow up non-respondents until most of the sample has answered, so that whether someone responds no longer depends on how satisfied they are.
