# Iceland's changing world of work: data

Aggregated figures on jobs advertised in Iceland, published daily by the
[Startup Iceland](https://startupiceland.com) jobs research database for its
"changing world of work" page. **No posting text and no personal data are
published here**: only counts and shares.

| File | What it holds |
|---|---|
| `data/summary.json` | What is collected, from where, and how much is classified |
| `data/market_now.json` | Open job postings by ISCO-08 occupation group, ILO generative-AI exposure gradient, and AI mentions |
| `data/ai_mentions_by_year.json` | Share of tech and creative job ads (Tvinna archive) mentioning AI, each year since 2010 |

Served at `https://cdn.jsdelivr.net/gh/balainiceland/iceland-work-trends@main/data/<file>`.

## Where the numbers come from

- **Postings:** Alfreð, Starfatorg (all public-sector vacancies), Tvinna, and the
  recruiters Hagvangur and Intellecta. Collected daily since 17 October 2026.
- **Occupations:** ISCO-08 unit groups, assigned to each posting by Claude
  (Anthropic) from the official ILO list.
- **Exposure to generative AI:** ILO 2025 Refined Global Index (Gmyrek, P., Berg, J.,
  Kamiński, K., et al. 2025. *Generative AI and Jobs: A Refined Global Index of
  Occupational Exposure*. ILO Working Paper 140). Data CC BY 4.0. Scores measure
  technical potential, not expected job loss.

## Caveats

- Counts are postings seen, not unique jobs: a job advertised on two sites is
  counted twice until duplicates are merged.
- Trends over time need time: daily collection began in October 2026. The long
  view comes from the Tvinna archive, which covers tech and creative roles only.

## Licence

These figures are licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
Please credit "Startup Iceland jobs research database" and the ILO index above.
