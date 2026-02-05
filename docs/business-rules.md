## Core Business Rules

### Stock Decrement
- Stock is stored in the Medication entity as the single source of truth.
- When an intake is confirmed as TAKEN:
  - Stock is decreased automatically.
- When an intake is marked as MISSED:
  - Stock is not affected.
- Stock values can never become negative.

### Alerts
- A LOW_STOCK alert is triggered when remaining doses
  fall below the defined threshold.
- A MISSED_INTAKE alert is triggered when two consecutive
  intakes are missed.
- Alerts are persistent and must be explicitly resolved.

### Liquid vs Tablet Medications
- Tablet medications decrement stock by 1 unit per intake.
- Liquid medications decrement stock using a dose-per-intake value.
- Remaining doses are calculated as:
  quantity_available / dose_per_intake.
- Intake confirmation is rejected if remaining stock
  is insufficient for the required dose.
