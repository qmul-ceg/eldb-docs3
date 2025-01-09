# CORE
The `CORE` table is the central table of the database, holding the details of all patients registered with a NEL GP Practice on the run date.

## CORE Table: `CORE`
Regular registration with a start date prior to the run date and an end date NULL or after the run date, at a currently active GP Practice, excluding patients with Date of Death \>= run date or with a record indicating patient has died, or is identifiable*[^1] *by patient's name as a Dummy/Test patient, or aged \>= 120 years.

fieldname      | description
----------     |------------
relrun_date    | relative run date for the database build
person_id      | identifier of person across multiple NHS organisations. Analogous to NHS Number.
patient_id     | identifier of patient at a practice. Analogous to EMIS number.
age            | age in years of patient on the run date
sex            | sex (Female, Male, Other, Unknown) for patient
ethnicity_code | latest ethnicity SNOMED concept id.
ceg_16         | CEG 16+1 ethnic categorisation, based on ethnicity_code
nhs_5          | NHS 5+1 ethnic categorisation, based on ethnicity_code
area_id        | area id for GP Practice (CH, NH, TH, WF, BK, HV, RB).
ods_code       | ODS (Organisation Data Service) identifier for the GP Practice.
practice_name  | GP Practice name, as defined for CEG reporting. This may differ from the name on ODS records.
reg_date       | calculated registration date for patient at practice
lsoa_2011      | LSOA (Lower Super Output Area) for 2011 relating to the patient's identified current address.
pt_area_id     | area_id based on patient's identified current address. NULL means the patient lives outside the North East London ICB area.

Because of the difficulties identifying some registrations, there are some persons (person_id) that appear as multiple patients (patient_id) at different practices. This may be due to patients moving practice; errors in the registration data held by a practice; or a patient deliberately registering and receiving healthcare with multiple practices. It is not possible to better define or clean the data. For most analyses, we recommend using patient_id.

## CORE Views
Views are virtual tables within a SQL database that provide a specified subset of the actual data. These Views appear as standard tables within MS Access and can be linked for use in queries in the same way. A series of Views are provided that filter the CORE table to each specific area.

### CORE Area: Registration
View based on area_id, which is defined by the location of the registered GP Practice.

- `CORE_BK`
- `CORE_CH`
- `CORE_HV`
- `CORE_NH`
- `CORE_RB`
- `CORE_TH`
- `CORE_WF`

### CORE Area: Residency
View based on pt_area_id, which is defined by patient's identified current address. These are the patients actually resident within the borough.

- `CORE_BK_pt`
- `CORE_CH_pt`
- `CORE_HV_pt`
- `CORE_NH_pt`
- `CORE_RB_pt`
- `CORE_TH_pt`
- `CORE_WF_pt`
