# MAF Home Page — UI/UX Craft Pass Notes

> **Status:** Deployed but needs visual craft layer
> **Date:** 2026-07-24
> **Repo:** garrybuilds/maf-homepage
> **Live:** https://malwaassetfirm.com

## Current State

The home page passes all structural checks:
- 39/39 structural verification
- 0/10 slop score (no AI design tells)
- 4-agent QA swarm passed (all CRITICAL/HIGH/MEDIUM fixed)
- WCAG AA contrast in both light and dark modes
- Responsive at 900px/768px/480px
- Full a11y (skip link, aria labels, focus-visible, reduced-motion)

**Garry's verdict:** "Still looks like slop to me, it will work for now but we will need to fix the ui/ux"

## The Gap

Per the Web Design Playbook (`/opt/data/home/brain/3_Resources/web-design-playbook.md`), the $500→$5,000 jump is NOT about more features or pages. It's about:

1. **Typography refinement** — letter-spacing, optical sizing, baseline grid alignment, smart fallback fonts
2. **Custom hero imagery** — a real visual element, not just a radar chart card. Real photography or custom illustration.
3. **Motion tuning** — staggered scroll reveals (0.3s with 50ms stagger), scroll-triggered depth, button hover that "breathes"
4. **Section rhythm** — more intentional background alternation, generous whitespace that signals confidence
5. **Content in founder's voice** — every headline tested: "Would Garry say this?"

## What's Working (Don't Touch)

- Split hero layout (text left, chart right) — correct surface choice
- Bento grid with size hierarchy (Deploy > Consulting > M&A) — not identical cards
- 6-vector radar chart as "star of the show" — tells the product story
- Journey flow with connected dots — not numbered 1-2-3
- Georgia serif + Inter body two-font system
- Warm cream background (#faf9f7) — not cold white
- Gold/bronze accent (#8b6914 light / #d4a017 dark) — replaced brown terracotta per Garry
- Purple (#533afd) for CTAs only — separated from editorial accent

## Accent Color History

- Original: #c47a38 (terracotta/amber from scorecard) — failed WCAG AA (3.3:1)
- QA fix: #a86228 (darkened terracotta) — passed AA but looked brown, Garry rejected
- Current: #8b6914 (warm gold-bronze, 4.83:1 AA pass) / #d4a017 (bright gold dark mode, 7.51:1 AAA pass)

## Next Steps When Ready

1. Generate custom hero imagery via FAL (technician with tablet, dispatcher screen, or abstract operations visual)
2. Refine typography: optical kerning, baseline grid, variable font weights
3. Add staggered scroll reveals (0.3s, 50ms stagger, first-view-only)
4. Tune section backgrounds for visual rhythm (white → cream → white → dark)
5. Run `maf-design-qa` swarm again after craft pass
6. Have Garry review before deploying