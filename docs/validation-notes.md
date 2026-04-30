# Validation notes

This project is currently in a validation phase.

## Important calculation warning

The current uploaded spreadsheet/export may not yet represent the final correct election-seat allocation method.

The visible spreadsheet logic appears to include:

- candidate vote totals
- candidate-specific division columns from 1 to 20
- a winner area that appears to use the largest personal vote totals

That is not necessarily the correct way to calculate seats under the D'Hondt method.

## Correct method to verify

For a D'Hondt-style election calculation, the calculation should be validated around this logic:

1. Sum votes by party/list.
2. Sort candidates inside each party/list by their personal votes.
3. Assign comparative figures from the party/list total votes:
   - highest candidate in the party gets party total / 1
   - second candidate gets party total / 2
   - third candidate gets party total / 3
   - and so on
4. Combine all candidates into one ranked list by comparative figure.
5. Select the top candidates according to the number of seats.

## Validation requirement

Before this project is presented as a finished result, the calculated elected candidates should be compared against an official public election result source or another trusted election result service.

## Current status

- Source material: uploaded spreadsheet/export and PDF/charts
- Seat count used in the task: 20
- Calculation status: needs verification before final presentation
- Portfolio status: should not be published as a finished portfolio project until the calculation is validated
