# Spotify Review Analysis & Product Design

Data-driven product case study: mining Spotify's Google Play Store reviews for the biggest driver of negative sentiment, then designing a Figma fix for it.

**View the interactive prototype** → https://www.figma.com/proto/Ukq9xKpMbheNcCWLqmYBRz/Spotify-Analysis-Project?node-id=8-147&viewport=-1145%2C130%2C0.52&t=sAp22lbGbyWEtgZR-1&scaling=scale-down&content-scaling=fixed&starting-point-node-id=7%3A52&page-id=7%3A51

## Overview

I pulled and structured 500+ of Spotify's general app reviews from the Google Play Store, ran sentiment analysis, and built a keyword-based theme-tagging system to find recurring complaint patterns in the negative reviews.

**Key finding:** Crashes, freezes, and failures to load account for 31% of all negative reviews, the single largest complaint theme, well ahead of anything else.

Since a redesign can't fix the crash bug itself, the solution targets the moment of failure instead: a fallback screen with a quick retry, plus 3 recovery actions (Clear Cache, Report a Problem, Check Status) so a failure ends in a clear next step instead of a dead end.

## What's in this repo

- `Spotify_Data_Analysis.ipynb` — full analysis: data cleaning, sentiment scoring, theme tagging, and the design writeup
- `Spotify_Google_Play_Reviews.txt` — raw review text pulled from the Google Play Store
- `Spotify_Review_Data.xlsx` — the same reviews structured into a clean dataset (name, date, review, helpful count)
- Figma mockup images — exported screens from the prototype (also embedded directly in the notebook)

## Tools

Python (pandas, VADER), Excel/Power Query, Figma

## Process

1. Structured raw scraped reviews into a clean dataset
2. Scored sentiment on every review
3. Tagged negative reviews against defined complaint themes, refining the keyword rules against a manual read
4. Identified the leading theme and designed a Figma fix for it
