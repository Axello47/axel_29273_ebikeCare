# EbikeCare: E-Bike Fleet Maintenance and Battery Health Tracker

Axel Shema (29273) | INSY 8311 | Instructor: Eric Maniraguha

## Problem Statement
Since January 2025, only electric motorbikes are registered for public transport in Kigali. Moto-taxi cooperatives now depend on batteries and electric drivetrains, yet service history, battery swaps and repairs are commonly tracked on paper or in chat groups. Missed servicing and degraded batteries go unnoticed until a bike fails, costing riders daily income.

## Proposed Solution
An Oracle database with PL/SQL that records bikes, riders, batteries, trips and maintenance jobs, scores battery health, flags overdue servicing and enforces maintenance rules automatically.

## Data Source
EV Battery Degradation and Telemetry dataset (Hugging Face, CC0, 4,500+ records), mapped onto bikes and batteries. No personal data. (Verify before submission.)

## Planned Tables
COOPERATIVE, RIDER, BIKE, BATTERY, TRIP_LOG, SERVICE_TYPE, MAINTENANCE_JOB, PART_USED, INSPECTION, AUDIT_LOG.

## Planned PL/SQL Features
Procedures log_service, assign_battery, record_trip; functions battery_health_score, next_service_due; a cursor over bikes past their service interval; package ebike_pkg; triggers that block assigning a critical-health battery, block double booking of a bike, and write to AUDIT_LOG; named exceptions for unknown bike IDs and invalid mileage.

## Innovation
User interface option: a Python (Streamlit or Flask) app where a mechanic records a service and the app calls log_service. Rules remain in PL/SQL.

## References (APA)
To be completed from docs/research/research_log.md after reading each source.

Note: convert to Word with Times New Roman 12 pt, headings 13-16 pt bold, 1.15 spacing, justified, max 2 pages.
