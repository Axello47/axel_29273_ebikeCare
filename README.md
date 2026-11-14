# EbikeCare: E-Bike Fleet Maintenance and Battery Health Tracker

**Student:** Axel Shema | **ID:** 29273
**Course:** INSY 8311 Database Development with PL/SQL | **Instructor:** Eric Maniraguha
**Institution:** Adventist University of Central Africa (AUCA)

## Problem statement
Since January 2025, only electric motorbikes are registered for public transport in the City of Kigali. Moto-taxi cooperatives now depend on batteries and electric drivetrains, but service history, battery swaps and repairs are usually tracked on paper or in chat groups. Overdue servicing and degraded batteries go unnoticed until a bike breaks down and the rider loses income.

## Objectives
**Main objective:** Build an Oracle database with PL/SQL that tracks maintenance and battery health for a fleet of electric moto-taxis and enforces maintenance rules automatically.

**Specific objectives:**
1. Record bikes, riders, batteries, trips and maintenance jobs in a normalized (3NF) schema.
2. Score battery health from cycle count and temperature using a PL/SQL function.
3. Flag bikes that are overdue for service using cursors and a scheduled check.
4. Block unsafe actions (assigning a critical-health battery, double booking a bike) with triggers.
5. Audit every change to maintenance and battery records.

## Data source
EV Battery Degradation and Telemetry dataset (Hugging Face, `Jayan12321/ev-battery-health-telemetry`), 4,500+ records, listed as CC0. To be verified and mapped onto bikes and batteries in Phase II. Link: https://huggingface.co/datasets/Jayan12321/ev-battery-health-telemetry

## Innovation (planned)
**Option:** User interface. **Tool:** Python (Streamlit or Flask) connected to Oracle. A mechanic records a service in the app and the app calls the PL/SQL procedure `log_service`. Business rules stay in PL/SQL.

## Planned tables
`COOPERATIVE`, `RIDER`, `BIKE`, `BATTERY`, `TRIP_LOG`, `SERVICE_TYPE`, `MAINTENANCE_JOB`, `PART_USED`, `INSPECTION`, `AUDIT_LOG`

## Planned PL/SQL features
- Procedures: `log_service`, `assign_battery`, `record_trip`
- Functions: `battery_health_score`, `next_service_due`
- Cursor: loop over bikes past their service interval
- Package: `ebike_pkg` grouping the above
- Triggers: block critical-health battery assignment, block double booking, write to `AUDIT_LOG`
- Exceptions: unknown bike ID, invalid mileage

## Repository structure
```
docs/research/   research log
docs/proposal/   2-page proposal
docs/presentation/   slides
data/            dataset notes and raw files
```

## References
See `docs/research/research_log.md` (APA, only sources actually read).
