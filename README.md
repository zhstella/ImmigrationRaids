# Immigration Raids

**Google Search API and OpenAI API**

We use google search API to generate top 10 URLs with one query “Immigration Raid, countyname, state”.

Advantage: a broader view of articles that is more in line with Dr. Padilla's requirement for diversity in articles, including news, paper, PDFs, social media, and etc. Also this method of searching is the same as Dr. Padilla's team's idea of manual searching.

Disadvantage: $75/month for 5000 searches (approximately 6~ times of iterating abnormal_arrest_dates.csv) but Dr. Padilla is willing to pay with her research funding yeahyeah!

**GPT3.5-Turbo** (currently in use)

Advantage: really cheap

Disadvantage: put in 16k context at a time, which reduces accuracy 

Possible future step: find a way to only web scrape the valid information of each article

**GPT4-Turbo**

Advantage: put in 128k context at a time

Disadvantage: expensive

Possible future step: continue to reduce more duplicated links and obviously invalid links

**New OpenAI API** (worth a try): GPT-4o, GPT-4o mini

**Currently we set four questions for GPT API:**

Does this text mention location or state? Explicitly say yes or no in the first word of your response along with your explanation;
Is the text related to immigration raids/arrests? Explicitly say yes or no in the first word of your response along with your explanation;
Does this text mention the date and is the date of this immigration raid between {start} and {end}? Explicitly say yes or no in the first word of your response along with your explanation;
Does this text confirm that the raid was conducted by Immigration and Customs Enforcement? Explicitly say yes or no in the first word of your response along with your explanation. If all four questions are answered Yes, then the article is valid; otherwise it is invalid.

**The final deliverable is three CSV files:** valid results (need further checkout), invalid results (discarded), and manual check results (some websites need login and can't web scrape, so Dr. Padilla's team needs to manually check those articles).
