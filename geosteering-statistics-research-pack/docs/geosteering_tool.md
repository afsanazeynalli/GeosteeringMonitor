# Geosteering Statistics Tool

## What it does

This standalone HTML application visualizes a measured-depth trajectory against a moving target window, optionally shows gamma ray, porosity, density, resistivity, and rate of penetration, and calculates descriptive summaries from the imported samples. It reports drilled interval lengths and percentages above, within, and below target; zone medians; target runs; distribution and crossplot views; and a cutoff-based net-pay check.

It is an exploratory descriptive tool. It does not estimate uncertainty in the geological interpretation, make steering recommendations, calculate reserves, or certify net pay. Results depend on sample spacing, provided target boundaries, units, missing-data handling, and chosen cutoffs.

## Run locally

Open `tools/geosteering_statistics_v4.html` in a modern browser. No build step, Python, package install, or network is required for the local demo or CSV import. Choose **Load built-in sample** or open the page with `#csv-sample` at the end of the local file URL. To use field data, open **Use your own data** and import a CSV matching `data/geosteering_example.csv`.

## Input columns

Required: `md,tvdss,top,base`. Optional: `gr,phi,rhob,rt,rop`; the page also accepts optional `inc,azi`. Header names are case-insensitive and columns can be in any order. CSV, semicolon, and tab separators are accepted. Depths are metres, TVDSS is negative downward, gamma ray is API, porosity is fraction (v/v), density is g/cc, resistivity is ohm·m, and ROP uses the source tool's log units. At least four valid rows are required. Rows are sorted by MD; nonnumeric required values are skipped. See `docs/geosteering_data_dictionary.md`.

## Live connections

The tool includes simulated streaming, WebSocket, and REST polling modes. Use simulated mode for a safe local demonstration. WebSocket/REST modes contact only the URL entered by the user and require network access; REST requires a CORS-enabled endpoint. Do not place credentials or API keys in the HTML file. Never connect operational systems without an approved gateway and authorization. The page is not a rig integration or control system.

## Known interpretation limits

- Output is descriptive of the supplied sampled trajectory and logs; it is not an inferential statistical model.
- The zone classification uses row-wise TVDSS compared with top/base values. It does not represent uncertainty or interpolation between samples.
- Net-pay results are conditional on user-selected cutoffs and input log quality; they are not a reserves or economic determination.
- Sample values in both the embedded demo and the repository CSV are invented for software illustration; they are not observations from a well.
