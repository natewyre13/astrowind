# Window Cleaning Quote Calculator — Project Plan

## What we are building
A free, mobile-first quote calculator for solo window cleaners and small crews.
No login. No database. Everything runs in the browser. The cleaner sets their
own rates, the tool does the math the same way every time.

Built on AstroWind (MIT License). Keep the LICENSE file and attribution in
this repo. Do not delete it.

## Why this niche
- Math is counting, not guessing: windows x price per window, plus height,
  add-ons, and a minimum.
- Buyers already pay for calculators, price lists, and kits in this niche.
- Current free tools either require signup to send a quote or are blog
  lead magnets. Ours is free, no signup, phone-first, with copy-paste
  quote text.

## V1 calculator spec (one page)

### Inputs (all editable, defaults are EXAMPLES only)
1. Window count (number)
2. Window type: Standard / Large-Picture / French-divided / Skylight /
   Storefront pane (each with its own default price per window)
3. Service: Both sides / Exterior only (exterior-only is about 40% less,
   factor 0.6, editable)
4. Stories: 1 / 2 / 3+ (height multipliers below, editable)
5. Add-ons (checkboxes, per window unless noted):
   - Screens
   - Tracks and sills
   - Hard-water / mineral stain removal
6. Your settings (saved in the browser with localStorage):
   - Price per window by type
   - Minimum job fee
   - Minutes per window (for time estimate)

### Starting example defaults (user MUST replace with their own rates)
- Standard window, both sides: $10 (common range $8-$15)
- Large/picture: $16 (range $12-$20)
- French/divided-lite: $14 (range $10-$18)
- Skylight: $22 (range $15-$30)
- Storefront pane, one side: $4.50 (range $3-$6)
- Height: 1 story x1.00, 2 stories x1.25, 3+ stories x1.50
  (some cleaners use x1.35 / x1.75 — make it editable)
- Screens: $2/window. Tracks/sills: $1.50/window.
  Hard-water removal: $10/window.
- Minimum job fee: $125 (common $100-$150)
- Time: 12 minutes per standard window (editable)

### Formula (show it on the page)
1. Base = window count x price per window x height multiplier x service factor
2. Add-ons = sum of checked add-ons x window count
3. Total = max(minimum fee, base + add-ons), rounded to nearest $5
4. Quote range = total x 0.90 to total x 1.10, rounded to nearest $5
5. Time estimate = window count x minutes per window, shown as hours/minutes

Never show one firm number. Always show a range plus the line breakdown.
Add a clear note: estimate only, confirm condition in person, prices are
the cleaner's own rates, not market rates. This is not legal, tax, or
business advice.

### Outputs
- Quote range (low / target / high) with line breakdown
- Time estimate
- Copy button: plain-text quote for SMS/email
- Print button: clean one-page quote
- Settings panel: edit and save rates in the browser

## Pages (v1)
- `/` — the calculator (the product)
- `/how-pricing-works` — plain-English explainer, SEO page, same formula
- `/privacy` — short page: runs in your browser, nothing is sent anywhere

## How it makes money (after the free tool is live)
- Free tool brings traffic and trust.
- Pro pack ($19-$29, one-time, Gumroad): spreadsheet version with job log,
  printable price list, quote template, follow-up and review-request
  scripts, AI prompt pack. Do NOT build the pack until the free tool works.
- Later v2 only: saved quotes / branding. Not in v1.

## Build order
1. Setup: clone, install, run locally, deploy a blank site (START-HERE.md)
2. Calculator page working with the formula above, mobile-first
3. Copy/print buttons, settings save, line breakdown
4. Explainer + privacy pages, basic SEO titles
5. Test on a real phone, fix layout, launch
6. Pro pack outline and listing (only after launch)

## Rules for this project
- Keep it to ONE tool. Do not add logins, payments, or a database in v1.
- Every default rate must be labeled as an example.
- Every price the user sees must show its math. No black-box numbers.
