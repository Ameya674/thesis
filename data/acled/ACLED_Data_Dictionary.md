# ACLED Data Dictionary (auto-generated from your file's columns)

This document explains the meaning, units/encodings, and shows an example value for each column present in the uploaded dataset.

| variable | meaning | units_or_encoding | inferred_dtype | example_value |
|---|---|---|---|---|
| event_id_cnty | Unique event identifier by number and country acronym (updated annually). | Text ID | object | USA23310 |
| event_date | Calendar date on which the event took place. | Date (YYYY-MM-DD) | object | 2020-01-01 |
| year | Year in which the event took place. | YYYY | int64 | 2020 |
| time_precision | Temporal precision of the event date. | Code: 1=exact day; 2=week (midpoint used); 3=month (midpoint or first/last) | int64 | 1 |
| disorder_type | Top-level disorder classification associated with the event/sub-event type (e.g., Political violence, Demonstrations, Strategic developments). | Category label | object | Demonstrations |
| event_type | Event type per ACLED typology (e.g., Battles, Explosions/Remote violence, Protests, Riots, Strategic developments, Violence against civilians). | Category label | object | Protests |
| sub_event_type | Sub-event type per ACLED typology (e.g., Armed clash, Air/drone strike, Peaceful protest). | Category label | object | Peaceful protest |
| actor1 | Primary named actor involved in the event (no directionality implied). | Text | object | Protesters (United States) |
| assoc_actor_1 | Associated actor(s) for Actor1 (aliases/affiliations). | Text | object | Health Workers (United States) |
| inter1 | Actor type of Actor1. | Code/label: 1=State forces; 2=Rebel groups; 3=Political militias; 4=Identity militias; 5=Rioters; 6=Protesters; 7=Civilians; 8=External/Other forces | object | Protesters |
| actor2 | Secondary named actor involved in the event (no directionality implied). | Text | object | Protesters (United States) |
| assoc_actor_2 | Associated actor(s) for Actor2 (aliases/affiliations). | Text | object | Students (United States) |
| inter2 | Actor type of Actor2. | Code/label: 1=State forces; 2=Rebel groups; 3=Political militias; 4=Identity militias; 5=Rioters; 6=Protesters; 7=Civilians; 8=External/Other forces | object | Protesters |
| interaction | Actor interaction category combining inter1 and inter2 (two-digit code or text label, e.g., 12 = State vs Rebel). | Composite code/label | object | Protesters only |
| civilian_targeting | Indicator/label for whether civilians were directly targeted in the event. | Yes/No/Label | object | Civilian targeting |
| iso | Numeric country code (ISO 3166-1 numeric). | Integer code | int64 | 840 |
| region | ACLED region name where the event occurred. | Category label | object | North America |
| country | Country in which the event occurred. | Text | object | United States |
| admin1 | First-level administrative unit name (e.g., state/province). | Text | object | Ohio |
| admin2 | Second-level administrative unit name (e.g., county/district). | Text | object | Cuyahoga |
| admin3 | Third-level administrative unit name (e.g., sub-district). | Text | float64 |  |
| location | Named location of the event (town/city/neighborhood or natural feature). | Text | object | Cleveland |
| latitude | Latitude of the event location in decimal degrees. | Decimal degrees | float64 | 41.4822 |
| longitude | Longitude of the event location in decimal degrees. | Decimal degrees | float64 | -81.6697 |
| geo_precision | Spatial precision of the coded location. | Code: 1=exact location; 2=near/part of region (or near town/city); 3=region/provincial capital proxy | int64 | 1 |
| source | Source(s) used to code the event. | Text (semicolon-delimited) | object | WKYC Studios; Crowd Counting Consortium |
| source_scale | Scale of the source. | Category: local, regional, national, international | object | Other-Subnational |
| notes | Short description of the event. | Free text | object | On 1 January 2020, an unknown number of people associated with the Cleveland Association of Rescue Employees demonstrated at the City Hall in Cleveland (Ohio) to demand mental health benefits. This event was a part of an ongoing strike for new contra |
| fatalities | Number of reported fatalities associated with the event. | Persons (count) | int64 | 0 |
| tags | Tags associated with the event (ACLED metadata). | Text | object | crowd size=no report |
| timestamp | Data processing timestamp (numeric). | Numeric time code | int64 | 1612546518 |