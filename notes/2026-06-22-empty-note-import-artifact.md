---
title: "Empty Note (import artifact)"
date: 2026-06-22
tags: [Nvidia, AI Agent, LLM, Business, Research]
source: https://elinke1c.daily.therundown.ai/ss/c/u001.Q334NVcZU4O6L6VKRz8ijAGTSgI3UhEczlMUzFFS743szowoztjRSgCxw9MInJGXcM4f1x6opHhNRDr2LFRAu3sam_7TyqUPtp0MNXZxJ2nsomjtVnUFxr68YdtS1879v8CtEOwOy5shN56qtbeoI07gbohbEmDimgqNrG01XaTJLlRmTwyNQxLYn-vPw-DTC1RtyeHcia4_t5iJbNqpYJCmW1B9Kc45D13vouwkDxl-DrzjuTjuFo2Pt0oql9bpj9xDP6DBzMru8B0d3NqBGA/4lz/EGCDO8GoR_Wj8aMTuCOjkg/h19/h001.\_PDXQ56axAdpHDI68gf0C1IYt1hOwqRRhjKynOhFW4c
type: article
status: read
---
1|
2|
3|###### AI RESEARCH
4|
5|
6|#### **📈 ++[NVIDIA’s case for scale isn’t everything in AI](https://elinke1c.daily.therundown.ai/ss/c/u001.Q334NVcZU4O6L6VKRz8ijAGTSgI3UhEczlMUzFFS743szowoztjRSgCxw9MInJGXcM4f1x6opHhNRDr2LFRAu3sam_7TyqUPtp0MNXZxJ2nsomjtVnUFxr68YdtS1879v8CtEOwOy5shN56qtbeoI07gbohbEmDimgqNrG01XaTJLlRmTwyNQxLYn-vPw-DTSzigMp7jufxKEBGjBC5rnkdO9VdsWO-vCl-cYmDzgeYHvhJoEyO2I9TycmZpY_cFkSxBthVUhlEG4A6BYMgQrg/4lz/EGCDO8GoR_Wj8aMTuCOjkg/h18/h001.w_EkdNC5nlfsfn8846vF6vl6PT_jHmZqgb0SU0lgBYo)++**
7|
8|
9|
10|
11||  | 
12||---|
13|| *Image source: NVIDIA* | 
14|
15|
16|**The Rundown:** NVIDIA and the University of Hong Kong published a **++[paper](https://elinke1c.daily.therundown.ai/ss/c/u001.Q334NVcZU4O6L6VKRz8ijAGTSgI3UhEczlMUzFFS743szowoztjRSgCxw9MInJGXcM4f1x6opHhNRDr2LFRAu3sam_7TyqUPtp0MNXZxJ2nsomjtVnUFxr68YdtS1879v8CtEOwOy5shN56qtbeoI07gbohbEmDimgqNrG01XaTJLlRmTwyNQxLYn-vPw-DTC1RtyeHcia4_t5iJbNqpYJCmW1B9Kc45D13vouwkDxl-DrzjuTjuFo2Pt0oql9bpj9xDP6DBzMru8B0d3NqBGA/4lz/EGCDO8GoR_Wj8aMTuCOjkg/h19/h001.\_PDXQ56axAdpHDI68gf0C1IYt1hOwqRRhjKynOhFW4c)++**suggesting that the future of AI might not come from scaling but from smarter orchestration, with their new tool training small models that can surpass frontier AI at a fraction of the cost.
17|
18|
19|**The details:**
20|
21|
22|- ToolOrchestra trains an “orchestrator” model that decides when to reason internally and when to call specialized tools and models, based on the task.
23|
24|- An 8B model trained with the system surpassed GPT-5 and Claude Opus 4.1 on Humanity’s Last Exam, scoring 37.1% while being 2.5x more efficient and faster.
25|
26|- Even when tested with unseen tools, the orchestrator adapted well — showing its ability to work with changing toolsets and pricing structures.
27|
28|- Prior agents overused the strongest (and most expensive) tools and models, but ToolOrchestra avoided this by orchestrating targeted model and tool usage.
29|
30|
31|**Why it matters:** In line with Ilya Sutskever’s recent **++[comments](https://elinke1c.daily.therundown.ai/ss/c/u001.dSnm3kaGd0BkNqLYPjeMf75St_4h4uVDlb2B1USeB_FItljbHo5xv72nPmD5PN8otD5-4VzDQSeutF2rIewqhhzZOOrLkl1eozJXbUAimKZwjMqICghLrPzKanPVPk6hRrwPzA1WYJJjMcBMV8trZgInXZBmK19owHMdGf1RYYCGfltKUKqWY7rzmmHRMynmJ7nkjVXnUBnX1IkRKZolLacxqmo4M3pxSWFzDlrSlxaqJqD52XSJ-nCSq8MXICuztt97Ai7NEMsSIcjB5fFZFvxXWFKrhXd6_EmUCDoUu1E9hlmr8gDYq2A9hCiQJLc-C-DgwUN9f_dRN2ipZfgqJaTOHOp-GSCbY4kL2N6zLT2rRKK2N5YNUbHbujlqcvTqkGouVM3zAlJdYp8K-wkA3JJ6K5dUIO3k6O0TGCdbb-kXbhwCRHWy1tXGGa3a3AszuWKKxHwkhzdnwlFrvdDLqrWLjC8WbJhA2oVcrS0-SzILHgIue2dln6iKAdnXwUZ8PbW_TSW_3-9Vt2bWMBQzCxd_AbPLkh2XgNEn-r-n4I0ZhmHjIHtsP7TOQLFPapdv-2PXw8lrkkM2zdpLKLfdyp3DK21CdYRAUHQwwu3QJpNVi7REvoKxQx5-RP1FjHV5TdprAF8dv6LNYQlfmqFYYuo1QtKBtIQNe8R4RqSeFjc1DvHmBgWLCnoJL7mcG4450UWX_p2P5lciyaMEMHqrkUphN6VoAiS0vHD75vjuLKb2KDP4bQpBKNxSrvjQOyRPoQmbNUscMnYFOVNh95ak39ESUzDpPVYdq752hrlwuwbqIGhTjFTXWXFrXnHdaEA1J-YRgziBdAgqlGmIrpUH2xc__Rt1u3E9FLWZRT6JG2w/4lz/EGCDO8GoR_Wj8aMTuCOjkg/h20/h001.fKx-8pv_AxK2XYAzePWiE1ATqLJ4IgGgjUTEK5h2EAQ)++**, ToolOrchestra challenges the “bigger is better” ideology. Instead of one giant system, NVIDIA shows how small models coordinating tools may be the path forward. If orchestration beats scaling, the smartest model/tool conductor will be the next big AI breakthrough.
32|
33|
34|
35|
36|