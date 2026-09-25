# Domain module contract / 业务模块接口

Read this reference before applying a visa, university, licence, registration, or other specialist module.

## Minimum contents of a module

- precise trigger and excluded cases;
- jurisdiction, category, application location, and supported applicant profiles;
- intake questions that change the workflow;
- eligibility and disqualification logic;
- official source map with verification dates;
- task sequence, dependencies, costs, and deadlines;
- required, conditional, optional, and discouraged evidence;
- translation, certification, format, upload, naming, and retention rules;
- forms, portal stages, appointments, interviews, examinations, and post-submission steps;
- stage-specific pitfalls and recovery paths;
- explicit user-confirmation points;
- test scenarios and maturity level.

## Maturity levels

- `M0 DRAFT`: structure only; not for a live case.
- `M1 OFFICIAL_REVIEWED`: applicable first-party sources mapped and checked.
- `M2 DRY_RUN`: representative fictional cases pass end to end.
- `M3 OBSERVED_CASE`: at least one authorised real case observed under user supervision.
- `M4 PRODUCTION_HARDENED`: varied cases and rule-change regressions completed.

State maturity at the granularity actually tested. Never convert “one UK visitor case” into “all UK visas verified.”

## Extension rule

Keep shared case management in the core skill. Put volatile country, institution, category, and portal details in the domain module. Do not duplicate the same rule in several modules; link to its maintained source and define any narrower exception.

