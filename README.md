# news-image-20261117

[![make.fun · news-image-20261117](https://make.fun/badge/news-image-20261117.svg)](https://make.fun/bounty/news-image-20261117?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261117)
[![rank](https://make.fun/badge/news-image-20261117/funfunin/news-image-20261117/rank.svg)](https://make.fun/bounty/news-image-20261117/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261117)
[![reward](https://make.fun/badge/news-image-20261117/funfunin/news-image-20261117/reward.svg)](https://make.fun/bounty/news-image-20261117?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261117)

Sum up Tuesday 17 November 2026's world news in one image.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

`main.ts` (Node 22, standard library only) copies the committed `entry.png` to `/output/entry.png`. It runs offline and is deterministic (the same bytes every run).

## The image

A newspaper front page for 17 November 2026: the date is the biggest, most legible element, then six stories in a 2×3 grid, one scene per story with a short headline and one factual subline.

| Story | What the picture shows |
|---|---|
| Wall Street slides | Trading floor under a steep red falling chart — Dow −849 (−1.64%), S&P 500 −1.03%, lowest close since July, fourth straight loss |
| Hormuz tankers hit | A burning tanker at dusk — the Panama-flagged LPG tanker Tara Gas struck by a projectile off Oman, crew member missing; an ADNOC vessel attacked the same day, 11 injured, 1 missing; US strikes on Qeshm Island |
| Kerch Bridge hit | A sea bridge with its span collapsed into the water — Ukraine's seventh-stage drone and missile strike, road arch and span down, rail section damaged |
| Cyberattack hits 178 sites | A red padlock over a world map — an Optimizely supply-chain attack injected malicious scripts serving at least 178 organisations, including CNN, BBC, Fox News, Zoom and Salesforce |
| US–China–Russia summit | The US, Chinese and Russian flags — China confirmed the first trilateral summit of Xi, Trump and Putin, set for 19 November in Shenzhen |
| Apple outage | A phone and laptop with dark screens — iCloud sign-in, App Store, Apple Music and Apple Pay down across Apple's services |

## How it was made

The six scenes were generated with Agnes `agnes-image-2.5-flash` (no text in the prompts, so no garbled lettering), then laid out by `compose.py` (Pillow): the date, headlines and sublines are drawn with a real font (Noto Sans), which is why they stay crisp at small sizes. The final image is a real PNG, 1024×1024, 607 KB — inside the 1 MiB gate. Sources for the facts: Reuters, AP, the IEA, UKMTO and ULA, all reporting on 17 November 2026.

## Why this selection

Six stories across regions and fields — markets, energy and the Middle East, the war in Europe, a global cyberattack, diplomacy, and consumer technology — all events of 17 November 2026 itself, each checkable against that day's reporting, with nothing from before that date presented as the day's news.
