# Excel Election Seat Allocation

Excel-based election seat allocation analysis using candidate vote data, sorting, comparative figures, and result ranking logic.

## Project purpose

This project studies how election results can be calculated from candidate vote data using spreadsheet methods. The main focus is data sorting, grouping, comparative figures, ranking, and seat allocation logic.

The project is intentionally method-focused instead of being named after one specific electoral district. Source documents are used as learning and reference material. The repository itself presents the calculation method as an independent data-analysis project.

## Current repository state

The uploaded source files are currently stored at the repository root. They are kept in place for now so that existing links and the project page do not break.

| Current file | Role |
|---|---|
| [`Elections.pdf`](Elections.pdf) | Original result/report PDF |
| [`chart-1.png`](chart-1.png) | Supporting chart screenshot |
| [`chart-2.png`](chart-2.png) | Supporting chart screenshot |
| [`chart-3.png`](chart-3.png) | Supporting chart screenshot |
| [`index.html`](index.html) | Project presentation page |

## Planned clean names

When binary file renaming is performed safely, the preferred clean structure is:

```text
docs/original/election-results-source.pdf
assets/screenshots/party-vote-share.png
assets/screenshots/seat-allocation-chart.png
assets/screenshots/comparative-figures-chart.png
index.html
```

## Repository folders

```text
docs/original/        Original assignment or reference documents
data/raw/             Raw candidate vote data, if added later
excel/                Working Excel workbook and final spreadsheet version
assets/screenshots/   Screenshots used for documentation
index.html            Presentation-oriented project page
```

## Calculation idea

The calculation will likely include:

1. import candidate vote data
2. clean and sort the dataset
3. group candidates by party/list
4. calculate group vote totals
5. calculate comparative figures
6. rank candidates by comparative figures
7. select the number of elected candidates
8. optionally visualize results with charts

## Source-data note

Election data and assignment documents are source material. The spreadsheet structure, calculation logic, documentation, and possible HTML version are project work built in this repository.

## License

MIT License
