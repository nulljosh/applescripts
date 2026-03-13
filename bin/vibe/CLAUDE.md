# vibe - Claude Notes

## Overview
Design token extractor. Scrapes a URL with Puppeteer, analyzes computed styles (color clustering by hue+lightness, dark mode detection), outputs CSS variables / Tailwind config / JSON.

## Stack
TypeScript, Puppeteer, tinycolor2, commander, Jest (33 tests, 76% coverage)

## Run
```bash
npm run dev -- https://stripe.com              # CSS variables
npm run dev -- https://stripe.com --format tailwind -o config.js
npm run dev -- https://stripe.com --format json
npm test
npm run build
```

## Files
```
src/
  index.ts          # CLI entry (commander)
  lib/
    scraper.ts      # Puppeteer: load page, extract computed styles
    analyzer.ts     # Color clustering (30deg hue / 20% lightness buckets), dark mode detection
    formatter.ts    # CSS vars / Tailwind / JSON output
  __tests__/        # 3 test files
```

## Status
v2.1.0 -- Stable.
