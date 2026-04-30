# Excel Election Seat Allocation

Excel-based election seat allocation analysis using candidate vote data, sorting, comparative figures, and result ranking logic.

## Project purpose

This project studies how election results can be calculated from candidate vote data using spreadsheet methods. The main focus is data sorting, grouping, comparative figures, ranking, and seat allocation logic.

The project is intentionally method-focused instead of being named after one specific electoral district. Source documents are used as learning and reference material. The repository itself presents the calculation method as an independent data-analysis project.

## Source material

The calculation uses candidate vote data from an instructor-provided Excel file and is checked against official public election result material.

Official reference material:

- Ministry of Justice election result service / Eduskuntavaalit 2023
- Pirkanmaa electoral district candidate-specific results
- Inspection count status: ready / completed

## Current repository state

The uploaded source files are currently stored at the repository root. They are kept in place for now so that existing links and the project page do not break.

| Current file | Role |
|---|---|
| [`Elections.pdf`](Elections.pdf) | Original result/report PDF |
| [`chart-1.png`](chart-1.png) | Supporting chart screenshot |
| [`chart-2.png`](chart-2.png) | Supporting chart screenshot |
| [`chart-3.png`](chart-3.png) | Supporting chart screenshot |
| [`index.html`](index.html) | Project presentation page |

## Processed data files

| File | Description |
|---|---|
| [`data/raw/candidate-votes.csv`](data/raw/candidate-votes.csv) | Cleaned candidate vote data extracted from the provided Excel workbook |
| [`data/processed/dhondt-results.csv`](data/processed/dhondt-results.csv) | Calculated top 20 candidates by D'Hondt comparative figure |
| [`data/processed/party-seat-summary.csv`](data/processed/party-seat-summary.csv) | Party vote totals and calculated seat counts |

## Calculation method

The validated calculation uses D'Hondt-style comparative figures:

1. Sum votes by party/list.
2. Sort candidates inside each party/list by personal votes.
3. Assign a party-internal rank to each candidate.
4. Calculate each candidate's comparative figure:

```text
comparative figure = party total votes / party-internal candidate rank
```

5. Sort all candidates by comparative figure.
6. Select the top 20 candidates.

## Calculated seat summary

| Party | Votes | Seats |
|---|---:|---:|
| SDP | 80131 | 6 |
| KOK | 66545 | 5 |
| PS | 62496 | 5 |
| VIHR | 23241 | 1 |
| KESK | 22010 | 1 |
| VAS | 21307 | 1 |
| KD | 16912 | 1 |

## Calculated elected candidates

| Seat | Candidate | Party | Candidate votes | Comparative figure |
|---:|---|---|---:|---:|
| 1 | Marin Sanna | SDP | 35628 | 80131.00 |
| 2 | Ikonen Anna-Kaisa | KOK | 11428 | 66545.00 |
| 3 | Bergbom Miko | PS | 10525 | 62496.00 |
| 4 | Merinen Ville | SDP | 6274 | 40065.50 |
| 5 | Kiuru Pauli | KOK | 10982 | 33272.50 |
| 6 | Vigelius Joakim | PS | 10113 | 31248.00 |
| 7 | Nurminen Ilmari | SDP | 4781 | 26710.33 |
| 8 | Tynkkynen Oras | VIHR | 5401 | 23241.00 |
| 9 | Vikman Sofia | KOK | 7548 | 22181.67 |
| 10 | Ovaska Jouni | KESK | 6376 | 22010.00 |
| 11 | Kontula Anna | VAS | 4909 | 21307.00 |
| 12 | Puisto Sakari | PS | 6592 | 20832.00 |
| 13 | Asell Marko | SDP | 4540 | 20032.75 |
| 14 | Tanus Sari | KD | 6117 | 16912.00 |
| 15 | Satonen Arto | KOK | 6029 | 16636.25 |
| 16 | Lyly Lauri | SDP | 4533 | 16026.20 |
| 17 | Savio Sami | PS | 6012 | 15624.00 |
| 18 | Viitanen Pia | SDP | 4112 | 13355.17 |
| 19 | Jäntti Aleksi | KOK | 4157 | 13309.00 |
| 20 | Niemi Veijo | PS | 3135 | 12499.20 |

## Validation note

The earlier spreadsheet/export layout appeared to divide individual candidate votes by 1, 2, 3, and so on. The corrected calculation instead uses party/list total votes divided by each candidate's rank inside that party/list.

## License

MIT License
