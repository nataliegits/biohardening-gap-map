# Biohardening Gap Map

An evidence map of the two main indoor air biohardening techniques, far-UVC light at 222 nm and glycol vapor disinfection. It codes the published literature by what was tested, in what setting, in what model system, and against what endpoint, so that the experiments nobody has run are visible as holes rather than as absences you have to notice for yourself.

**Live map: https://nataliegits.github.io/biohardening-gap-map**

Written up at [Bench Pressed](https://benchpressed.substack.com/).

## What's in it

Five matrices, 123 cells, 54 studies.

| Matrix | Rows | Columns |
|---|---|---|
| Far-UVC efficacy | organism class | suspension to human infection outcome |
| Far-UVC safety | model system | skin and eye, DNA damage and pathology |
| Far-UVC byproducts | ozone, OH radical, secondary organic aerosol | box model to occupied room |
| Glycol efficacy | organism class | suspension to human infection outcome |
| Glycol safety | model system | cytotoxicity, inflammation, barrier, systemic |

Click any cell to see the studies behind it, each with its citation, a link, and the finding that earned it the cell. The full reference list is at the bottom of the page, grouped by matrix.

## How to read it

- **The number in a cell** is how many studies this scan found for it.
- **Shading** is evidence density. Darker means more settled.
- **A pale cell with a dash** means this scan found nothing.
- **An outlined cell** is an experiment I designed in [Building for biosecurity](https://benchpressed.substack.com/p/building-for-biosecurity-two-tools) and have not run.

## Method, and its limits

The scan covers indexed literature reachable by search in November 2026. It is weighted toward English-language work and toward papers that name their organism and setting where a search can see them.

Density levels are a judgement, not a count. Level 4 means several independent groups with consistent results. Level 1 means one study, an indirect measurement, or evidence borrowed from a different exposure regime. Where a cell carries a caveat flag, the flag is doing more work than the colour.

Efficacy columns escalate in realism, so a filled cell on the left says nothing about the one to its right. Far-UVC safety is split by tissue because the skin argument and the eye argument rest on different penetration depths and have very different amounts of human data behind them.

**An empty cell means this scan found no study. It does not mean no study exists.** Treat every hole as a lead to check.

## Corrections

If a cell is wrong, or a paper is missing, or you think a shading is off, open an issue. Include the citation and which cell it belongs in. Corrections are the point of putting this in a repo rather than just on a page.

## Running it locally

One self-contained file, no build step, no dependencies.

```
git clone https://github.com/nataliegits/biohardening-gap-map.git
cd biohardening-gap-map
open index.html
```

The study data lives in a JavaScript object near the top of the script block in `index.html`. Each entry is one paper. The matrices reference those entries by key, so adding a study means adding one entry and putting its key in the right cell.

## Licence

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Reuse the coding, the structure, or the whole thing, with attribution.

## Citation

> Chen, N. (2026). Biohardening Gap Map: an evidence map of far-UVC and glycol vapor air disinfection. https://nataliegits.github.io/biohardening-gap-map
