---
title: "OpenAI trains models to ‘confess’ when they cheat"
date: 2026-06-22
tags: [Gaming, Image, LLM, OpenAI, Research]
source: https://elinke1c.daily.therundown.ai/ss/c/u001.eCbm_1zon7G0lMoXTECWa-IUY9yqSc2cx0km5OJXo-PT_UyHI-mZdy8lqBNseE7qj9HFV5JvJwWBYsv28zkORXbsnqqvSPwKnM7_MeJzdfpxYfgh2YPo6GAMyxroYQl7kJHBg2Ksv2Iv0wLtciHJFq3FjIOl5V8hPkwdtktbPylBWKhqLkCnb69q0aBS7OHl7a5uILfs1GQG9cW4mIhZLEy79mHbeQ7KOVFXfah0wcMveJbUia30f9-OQlbZ7F3XsxN4aK7G61pTllY9kNSDdP7cf5KB2KmJCCs3Djrz5SWwe3ENe4peg0cjAmwv73Rfthcn7RXTyq7nw6sn86D8Lw/4m6/sT9XRgZ4Twapv0vhp9nPBg/h11/h001.cn7zhlXq6bi9z2gYJ_t9gx_8XU3y_mNI2mkzqxc7Q7o
type: article
status: read
---
++**





|  | 
|---|
| *Image source: Nano Banana Pro / The Rundown* | 


**The Rundown:** OpenAI just **[published](https://elinke1c.daily.therundown.ai/ss/c/u001.a3gBHu6_kDRL6l3yEfNWAQEHmE4ZhsXPCMfIhFjtNJ9TJVSC8PIyr4US-X2cQ0UA3U9GKwHR7A3BV1-OkAyBKLSd_0vlgK3NUYhzsrFNEhIbWIF244Fl0CcXmV51aEZAip4EYldmhb6bT-6hTgfGm0X2enD8LkewPauvPyduEeyfk4qcYi_em7yO8RBcnaj9F7mh8eGG0YLr9i4h10_XKavnZBEBhKuS-65t_ql7FTpW-xVpdo2t8HtyNJS2w1c-ZmBktJeEf2mqxaC3uBQxrDvmMWwVFaai0EhFINrEs557N8TVe4UWPLow8-EZd9Vrog1mtXz7qL4uPYCYePGoEA/4m6/sT9XRgZ4Twapv0vhp9nPBg/h12/h001.FufWkdSalmtZEtxKXHjAN2TC-4cu-W-93I85EfBKtVM)** new research on a technique called “Confessions” that trains models to produce a second, honesty-only output — where the model reports rule violations, shortcuts, or deceptive workarounds.


**The details:**


- After generating a response, the model writes a separate confession report listing all instructions it received and whether it actually followed them.

- Admissions carry no penalty, with the model earning ‘rewards’ for truthful self-reporting even if the original answer was misleading or gamed the grader.

- In stress tests on GPT-5 Thinking, ‘false negative’ cases where the model broke rules and hid it occurred just 4.4% of the time.

- OpenAI said the Confessions research does not prevent misaligned behavior, but helps surface it as another tool to leverage in a stack of AI safety methods.


**Why it matters:** Visibility into model behavior is improving, but the systems themselves are improving faster. Confessions give researchers a way to catch shortcuts and deception early, though the real test is whether interpretability can keep pace as systems grow more sophisticated and subsequently harder to test and control.