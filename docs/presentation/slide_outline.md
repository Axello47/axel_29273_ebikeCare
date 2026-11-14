# Slide Outline (12 slides)

1. Title: EbikeCare, Axel Shema, ID 29273, INSY 8311, Eric Maniraguha, GitHub link
2. Background and problem: Kigali moto-taxi riders and cooperatives; electric-only registration since Jan 2025; unnoticed breakdowns cost income
3. Motivation: why this project (local relevance, real operational need)
4. Objectives: 1 main, 5 specific (see README)
5. Research: existing approaches and gaps (from research log)
6. Data source: Hugging Face EV battery telemetry, link, size, 3-5 sample records
7. Proposed solution and innovation: Option = User interface, Tool = Streamlit/Flask calling log_service
8. Planned database: main tables and relationships (mini ERD)
9. PL/SQL approach: a trigger blocks assigning a critical-health battery; a cursor lists bikes past service interval; battery_health_score scores each battery; ebike_pkg groups the logic; exceptions handle unknown bike IDs
10. Expected results: live demo of logging a service, blocked unsafe assignment, audit trail
11. Future improvements and limitations: dataset is EV-generic, not Rwandan field data; add SMS alerts, dashboard
12. References (APA)
