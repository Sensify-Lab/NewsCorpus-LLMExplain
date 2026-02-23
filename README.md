# NewsCorpus-LLMExplain

We introduce **NewsCorpus** covering contemporary events curated from [AllSides](https://www.allsides.com) from **July 21, 2012** – **July 23, 2024**.The dataset contains **17,166 articles** grouped into **5,722 news round-ups** across **64 topical categories**.

Data were collected using a [public scraping tool](https://github.com/csinva/news-title-bias/tree/master). The scraping script was adapted due to updates in the AllSides HTML structure.

Each row/ roundup contains three parallel news stories representing different political perspectives:
- Left or Left-leaning media  
- Center media  
- Right-leaning or Right media  

## Citation
If you use this dataset or build upon it in your research, please cite the following paper:

TBD

```bibtex
TBD
```

## 📄 [NewsCorpus17k.csv](NewsCorpus17k.csv)
### 👉 Checkout preview: [NewsCorpus17K_sample100.csv](NewsCorpus17K_sample100.csv)

### Core Metadata
- `Date` — publication date of the roundup
- `Topic` — categorical topic label
- `Title of Headline Roundup` — AllSides roundup headline
- `url_story` — AllSides roundup link

### Left/Left-Leaning Story
- `left_story_title` — article headline
- `left_story_url` — article URL
- `left_story_source` — publisher name
- `left_story_leaning` — political bias label
- `left_story_text` — preview or snippet text

### Center Story
- `center_story_title` — article headline
- `center_story_url` — article URL
- `center_story_source` — publisher name
- `center_story_leaning` — political bias label
- `center_story_text` — preview or snippet text

### Right-Leaning/Right Story
- `right_story_title` — article headline
- `right_story_url` — article URL
- `right_story_source` — publisher name
- `right_story_leaning` — political bias label
- `right_story_text` — preview or snippet text


## Major topic groups include:

- **Elections and Democracy:** 2024 Presidential Election, Elections, Voting Rights and Voter Fraud, Campaign Finance, Polarization  
- **US Politics and Law:** Politics, Supreme Court, Civil Rights, Federal State and Tribal Powers, Free Speech, Privacy  
- **Justice and Safety:** Criminal Justice, Violence in America, Gun Control and Gun Rights, Terrorism, Sexual Misconduct  
- **Health and COVID:** Healthcare, Public Health, Coronavirus, Life During COVID-19, COVID-19 Misinformation, Safety and Sanity During COVID-19  
- **Economy and Business:** Economy and Jobs, Business, Banking and Finance, Taxes, Trade, Housing and Homelessness  
- **International Affairs:** World, Foreign Policy, The Americas, Middle East, China, Russia, Ukraine War, Defense and Security  
- **Society and Rights:** Race and Racism, LGBTQ Issues, Abortion, Education, Family and Marriage, Religion and Faith, Inequality  
- **Science and Technology:** Science, Technology  
- **Environment and Energy:** Environment, Climate Change, Sustainability, Energy, Water and Oceans  
- **Media and Information:** Media Industry, Media Bias, Fake News, Facts and Fact Checking, Common Ground  
- **Culture and Sports:** Culture, Arts and Entertainment, Sports  
- **People and Figures:** Joe Biden, Donald Trump  

Political bias is assigned at the **publisher level** using AllSides ratings. Each article inherits the political leaning of its publisher. Prior work shows approximately 97% agreement between publisher-level and article-level bias.

---
## LLMExplain
We selected **60 recent news articles** across **20 headline round-ups** from [NewsCorpus17k.csv](NewsCorpus17k.csv). Each record includes aligned left, center, and right news perspectives enriched with GPT-generated political ideology predictions and two types of explanations (**brief** and **detailed**). The explanations are intended to provide transparent reasoning behind the model’s predicted labels. This subset is designed for use in human annotation tasks and evaluation studies.
### 📄 [Brief Condition: LLMExplanationSubset-Brief.csv](LLMExplanationSubset-Brief.csv)
### 📄 [Detailed Condition: LLMExplanationSubset-Detailed.csv](LLMExplanationSubset-Detailed.csv)

### Additional Features
- `left_story_GPT_pred` — GPT-predicted political leaning
- `left_story_GPT_explanation` — GPT-generated explanation of prediction
- `center_story_GPT_pred` -— GPT-predicted political leaning
- `center_story_GPT_explanation` — GPT-generated explanation of prediction
- `right_story_GPT_pred`  — GPT-predicted political leaning
- `right_story_GPT_explanation` — GPT-generated explanation of prediction

---

## Notes

This dataset contains publicly available news metadata collected for research purposes.  
Users should respect original publisher copyright and terms of service.

For questions, contact: **kylewang@udel.edu**


## License

This project is licensed under the MIT License. See [LICENSE.md](./LICENSE) for details.


