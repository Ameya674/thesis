## Event identification & geography

| Variable           | Phases          | What it is (1 line)                                   | Example value(s)                         |
|--------------------|-----------------|-------------------------------------------------------|------------------------------------------|
| `date`             | P1–P3           | Calendar date of the event.                           | `2020-06-01`                             |
| `locality`         | P1–P3           | City/town where the event took place.                 | `Minneapolis`                            |
| `state`            | P1–P3           | Two-letter state/territory code.                      | `MN`, `PR`                               |
| `resolved_locality`| P1–P3           | Standardized locality name used for analysis.         | `Minneapolis`                            |
| `resolved_county`  | P1–P3           | Standardized county name.                             | `Hennepin County`                        |
| `resolved_state`   | P1–P3           | Standardized state/territory name.                    | `Minnesota`                              |
| `lat` / `lon`      | P1–P3           | Latitude/longitude of the event location.             | `44.9780`, `-93.2650`                    |
| `fips_code`        | P1–P3           | County FIPS code for the event location.              | `27053`                                  |

---

## Event metadata / characterization

| Variable      | Phases          | What it is                                              | Example value(s)               |
|---------------|-----------------|---------------------------------------------------------|--------------------------------|
| `macroevent`  | P1–P3           | ID linking related events (e.g., protest + counter).    | `20200601-minneapolis-floyd`   |
| `online`      | P2–P3           | Indicates if event was online/virtual.                  | `0`, `1`                       |
| `valence`     | P1–P3           | Left/right/other orientation of the event.              | `0` (other), `1` (left), `2` (right) |

---

## Size

| Variable      | Phases          | What it is                                              | Example value(s)                       |
|---------------|-----------------|---------------------------------------------------------|----------------------------------------|
| `size_text`   | P1–P3           | Text description of crowd size.                         | `hundreds`, `about 50`                 |
| `size_low`    | P1–P3           | Lower numeric estimate of participants.                 | `50`, `200`                            |
| `size_high`   | P1–P3           | Upper numeric estimate of participants.                 | `100`, `500`                           |
| `size_mean`   | P1–P3           | Averaged point estimate used for analysis.             | `75`, `350`                            |
| `size_cat`    | P1–P3           | Binned size category (e.g., small/medium/large).        | `1` (small), `4` (very large)          |

---

## Organizers & participants

| Variable        | Phases          | What it is                                              | Example value(s)                               |
|-----------------|-----------------|---------------------------------------------------------|------------------------------------------------|
| `actors`        | P1              | Mixed list of orgs and participant types.              | `Women’s March; students; local residents`     |
| `organizations` | P2–P3           | Named organizations visibly involved.                   | `NAACP; Sunrise Movement`                      |
| `participants`  | P2–P3           | Types of people present.                                | `students; parents; teachers`                  |

---

## Claims (`claims_all` concept)

| Variable           | Phases          | What it is                                              | Example value(s)                                     |
|--------------------|-----------------|---------------------------------------------------------|------------------------------------------------------|
| `claims`           | P1–P2           | Coder-written summary of what the event was about.     | `for immigrant rights; against family separation`    |
| `claims_summary`   | P2–P3           | Structured summary phrases of main claims.             | `against police brutality; for racial justice`       |
| `claims_verbatim`  | P2–P3           | Verbatim slogans from signs/chants/etc.                | `Black lives matter; No justice, no peace`          |

---

## Issues / issue tags

| Variable              | Phases          | What it is                                              | Example value(s)                     |
|-----------------------|-----------------|---------------------------------------------------------|--------------------------------------|
| `issues`              | P1 & P3         | Canonical issue tags for the event.                     | `policing; racism`                   |
| `issue_tags`          | P2              | Union of all issue tags (summary + verbatim).           | `covid; labor; economy`              |
| `issue_tags_summary`  | P2–P3           | Issue tags triggered by `claims_summary`.               | `foreign affairs; war and peace`     |
| `issue_tags_verbatim` | P2–P3           | Issue tags triggered by `claims_verbatim`.              | `indigenous peoples; policing`       |

---

## Participant injuries & casualties

| Variable                    | Phases          | What it is                                              | Example value(s)                             |
|-----------------------------|-----------------|---------------------------------------------------------|----------------------------------------------|
| `injuries_crowd`            | P1–P2           | Text/number describing injured participants.            | `2`, `several`, `unspecified`                |
| `injuries_crowd_any`        | P1–P2           | Any participants injured? (binary flag).                | `0`, `1`                                     |
| `participant_injuries`      | P3              | Text/number describing injured participants.            | `more than 5`, `1`                           |
| `participant_deaths`        | P2–P3           | Text/number describing participant deaths.              | `0`, `1`, `at least 2`                       |
| `participant_casualties_any`| P3              | Any participants injured or killed? (binary flag).      | `0`, `1`                                     |

---

## Police injuries & casualties

| Variable                    | Phases          | What it is                                              | Example value(s)                        |
|-----------------------------|-----------------|---------------------------------------------------------|-----------------------------------------|
| `injuries_police`           | P1–P2           | Text/number describing injured police.                  | `1`, `several`, `unspecified`           |
| `injuries_police_any`       | P1–P2           | Any police injured? (binary flag).                      | `0`, `1`                                |
| `police_injuries`           | P3              | Text/number describing injured police.                  | `3`, `minor injuries`                   |
| `police_deaths`             | P2–P3           | Text/number describing police deaths.                   | `0`, `1`                                |
| `police_casualties_any`     | P3              | Any police injured or killed? (binary flag).            | `0`, `1`                                |

---

## Chemical agents

| Variable          | Phases          | What it is                                              | Example value(s)                          |
|-------------------|-----------------|---------------------------------------------------------|-------------------------------------------|
| `chemical_agents` | P1–P2           | Notes on tear gas / pepper spray or similar use.        | `tear gas`, `pepper spray; smoke grenades`|

*(In Phase 3, similar info usually appears in `police_measures`.)*

---

## Other phase-varying variables

| Variable              | Phases          | What it is                                              | Example value(s)                             |
|-----------------------|-----------------|---------------------------------------------------------|----------------------------------------------|
| `participant_measures`| P2–P3           | Narrative of what participants did.                     | `marched downtown; blocked highway`          |
| `police_measures`     | P2–P3           | Narrative of what police did.                           | `on scene; made arrests; used pepper spray`  |
| `title`               | P2              | Short descriptive title for the event.                  | `Teachers’ strike at City Hall`              |
| `conf`                | P3              | Coder confidence score for the record.                  | `0.9`, `0.6`                                 |
| `notables`            | P3              | Named high-profile attendees.                           | `Rep. Ilhan Omar; Mayor of Boston`           |
| `targets`             | P3              | Specific institutions/people protested against.         | `City Council; ICE; BlackRock`               |
