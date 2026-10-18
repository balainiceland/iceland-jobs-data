# Iceland jobs data

Published daily by the [Startup Iceland](https://startupiceland.com) jobs
research database: the figures behind the "changing world of work" page, and
the listings on the Startup Iceland jobs board.

| File | What it holds |
|---|---|
| `data/summary.json` | What is collected, from where, and how much is classified |
| `data/market_now.json` | Open jobs by ISCO-08 occupation group, ILO generative-AI exposure gradient, and AI mentions (each job counted once across sites) |
| `data/ai_mentions_by_year.json` | Share of tech and creative job ads (Tvinna archive) mentioning AI, each year since 2010 |
| `data/coverage.json` | How much of Iceland's job market the database sees, against Statistics Iceland's vacancy survey |
| `data/jobs-data.json` | The jobs board: startup jobs in Iceland, open and past, with their advertisement text |

Served at `https://raw.githubusercontent.com/balainiceland/iceland-jobs-data/main/data/<file>`
(and `https://cdn.jsdelivr.net/gh/balainiceland/iceland-jobs-data@main/data/<file>`).

## Where the numbers come from

- **Postings:** Alfreð, Starfatorg (all public-sector vacancies), Tvinna, and the
  recruiters Hagvangur and Intellecta. Collected daily since 17 October 2026.
  Names, emails and phone numbers of contact people are removed before storage.
- **Occupations:** ISCO-08 unit groups, assigned to each posting by Claude
  (Anthropic) from the official ILO list.
- **Exposure to generative AI:** ILO 2025 Refined Global Index (Gmyrek, P., Berg, J.,
  Kamiński, K., et al. 2025. *Generative AI and Jobs: A Refined Global Index of
  Occupational Exposure*. ILO Working Paper 140). Data CC BY 4.0. Scores measure
  technical potential, not expected job loss.
- **Official vacancies:** Statistics Iceland, table JVS00001.

## Caveats

- Trends over time need time: daily collection began in October 2026. The long
  view comes from the Tvinna archive, which covers tech and creative roles only.
- On the jobs board a Tvinna job counts as open for 90 days after it was
  listed, because Tvinna never takes a job down.

## Licence

The figures (`summary`, `market_now`, `ai_mentions_by_year`, `coverage`) are
licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Please credit
"Startup Iceland jobs research database" and the ILO index above.

`jobs-data.json` is not covered by that licence: the advertisement texts belong
to the employers who wrote them, and are republished here only to list their
jobs on the Startup Iceland board.
