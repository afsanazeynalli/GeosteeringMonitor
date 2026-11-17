# Geosteering Statistics Research Pack

A self-contained research and demo package for trajectory-to-target visualization and descriptive geosteering statistics.

## Quick start

Open `tools/geosteering_statistics_v4.html` in a modern browser. The local demo and CSV import work without installing software or connecting to the network. To load the included synthetic data, choose **Use your own data → Import CSV file** and select `data/geosteering_example.csv`.

## Contents

- `tools/geosteering_statistics_v4.html` — standalone browser tool.
- `data/geosteering_example.csv` — synthetic example only; not a well observation.
- `docs/geosteering_tool.md` — features, use, data modes, and limitations.
- `docs/geosteering_research_brief.md` — research questions and validation plan.
- `docs/geosteering_data_dictionary.md` — schema, units, and conventions.

The tool visualizes target position, trajectory, and optional logs; summarizes sampled footage above/within/below target; and offers distribution, crossplot, and user-cutoff net-pay exploration. It does not make steering recommendations, infer geological uncertainty, determine reserves, or certify net pay.

## Live data

A simulated feed is available for demonstration. WebSocket and REST modes only connect when a user enters an endpoint and starts the connection; REST requires a CORS-enabled endpoint. Use only approved gateways. Do not embed credentials in the HTML file.

## Licensing

The supplied HTML has no identified author or license notice. This pack includes it at the user's request, but does not grant redistribution rights for that source file. Confirm rights before public upload. The accompanying synthetic CSV and research documentation are original pack materials; see `LICENSE.md`.
