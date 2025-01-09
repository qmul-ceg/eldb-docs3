# Lookup Tables

***
## Age Bands: `lu_ageband`
Age banded by a selection age band standards.

fieldname      | description
------------   | ------------
age            | patient age
five_year      | five-year age bands (A:0-4 \~ W:110-114)
five_year_term | five-year age bands text term
ten_year       | ten-year age bands (A:0-9 \~ L:110-119)
ten_year_term  | ten-year age bands text term
ons_a          | ONS A age bands (A:0-24 \~ D:65-119)
ons_a_term     | ONS A age bands text term
ons_b          | ONS B age bands (A:0-24 \~ E:75-119)
ons_b_term     | ONS B age bands text term
ons_c          | ONS C age bands (A:0-15 \~ I:85-119)
ons_c_term     | ONS C age bands text term
ons_d          | ONS D age bands (A:0-4 \~ R:85-119)
ons_d_term     | ONS D age bands text term
ons_e          | ONS E age bands (A:0-84 \~ F:105-119)
ons_e_term     | ONS E age bands text term
ons_f          | ONS F age bands (A:0-4 \~ S:90-119)
ons_f_term     | ONS F age bands text term
ons_g          | ONS G age bands (A:0-15 \~ C:65-119)
ons_g_term     | ONS G age bands text term
esp_1976       | European Std Population 1976 (A:0-4 \~ R:85-111)
esp_1976_term  | European Std Population 1976 text term
esp_2013       | European Std Population 2013 (A:0, B:1-4, C:5-9 \~ U:95-111)
esp_2013_term  | European Std Population 2013 text term
eth_band       | ethnicity report bands (A:0-4 \~ E:65-119)
eth_band_term  | ethnicity report band text term
profile_a      | population profiling a bands (A:16-18 \~ J:85-119)
profile_a_term | population profiling a bands text term
profile_b      | population profiling b bands (A:0-4 \~ K:85-119)
profile_b_term | population profiling b bands text term
ceg_piqi       | practice improvement quality indicators age bands (A:0-17 \~ D:65-119)
ceg_piqi_term  | practice improvement quality indicators age bands text term

### Age Bands Key: `lu_ageband_key`

fieldname | description
----------|-------------
age_std   | age banding standard
band      | banding letter used with the age band standard
term      | age band text term

***
## Deprivation (IMD): `lu_deprivation`
Lower Super Output Area (LSOA) defined in 2011 within northeast London with related Indices of Multiple Deprivation (IMD) based on 2015 and 2019 data. Quintiles (1 as most deprived) calculated within Local Authority, Integrated Care Partnership, east London region and nationally.

fieldname              | description
------------           | ------------------------
LSOA_code_2011         | ONS code (e-code) for LSOA 2011
LSOA_name_2011         | LSOA 2011 name (Local Authority name & identifier)
IMD_2015               | IMD score from 2015 IoD data
IMD_2019               | IMD score from 2019 IoD data
LA_code_2019           | ONS code (e-code) for local authority
LA_name_2019           | Local Authority name
LA_id                  | Local Authority identifier (CL, HK, NH, TH, WF, BD, HV, RB)*
LA_quintile_2015       | IMD_2015 quintile within Local Authority
LA_quintile_2019       | IMD_2019 quintile within Local Authority
ICP_id                 | Integrated Care Partnership identifier (CH, BHR, TNW)*
ICP_quintile_2015      | IMD_2015 quintile within Integrated Care Partnership
ICP_quintile_2019      | IMD_2019 quintile within Integrated Care Partnership
EL_id                  | east London region identifier (IEL, OEL)*
EL_quintile_2019       | IMD_2019 quintile within east London region
NEL_quintile_2019      | IMD_2019 quintile within northeast London
National_quintile_2019 | IMD_2019 quintile within England & Wales

identifier | area
-----------| ------------------------
CH         | City & Hackney
CL         | City of London
HK         | Hackney
TNW        | Tower Hamlets, Newham, & Waltham Forest
NH         | Newham
TH         | Tower Hamlets
WF         | Waltham Forest        
BHR        | Barking & Dagenham, Havering & Redbridge    
BD         | Barking & Dagenham
HV         | Havering
RB         | Redbridge
IEL        | Inner East London (CH, NH, TH)        
OEL        | Outer East London (WF, BD, HV, RB)

***
## LSOA: `lu_lsoa`
Lower Super Output Area (LSOA) defined in 2011 within England and Wales with associated local authorities.

fieldname      | description
------------   | ------------------------
LSOA_code_2011 | ONS code (e-code) for LSOA 2011
LSOA_name_2011 | LSOA 2011 name (Local Authority name & identifier)
LA_code_2019   | ONS code (e-code) for local authority
LA_name_2019   | Local Authority name

## LSOA 2021: `lu_lsoa2021`
Lower Super Output Area (LSOA) defined in 2021 within England and Wales with associated LSOA 2011, LAD 2022 + LAD 2019 (Local Authority), and IMD score 2019

fieldname          | description
------------       | ------------------------
id                 | table id
lsoa2021_code      | ONS (e-code) for LSOA 2021
lsoa2021_name      | LSOA 2021 name (Local Authority name & identifier)
changed            | relationship indicator for LSOA2011 to LSOA2021 (U, S, M, X)
lsoa2011_code      | ONS code (e-code) for LSOA 2011
lsoa2011_name      | LSOA 2011 name (Local Authority name & identifier)
lad2022_code       | ONS code (e-code) 2022 for local authority
lad2022_name       | Local Authority name 2022
lad2022_name_wales | Local Authority name 2022 (Welsh Language)
lad2019_code       | ONS code (e-code) 2019 for local authority
lad2019_name       | Local Authority name 2019
imd2019_score      | Indices of Multiple Deprivation score calculated by ONS
imd2019_quintile   | Indices of Multiple Deprivation quintile calculated for England

identifier | change action
-----------| ------------------------
U          | unchanged
S          | split
M          | merged
X          | fragmented

For more information, see the [ONS Open Geography Portal](<https://geoportal.statistics.gov.uk>).

***
## Ethnicity: `lu_ethnicity`

fieldname      | description
------------   | ------------------------
id             | row identifier
code           | code (SNOMED, Read2, CTV3, EMIS Local)
dbid           | database identifier for code
scheme         | code scheme identifier (71, 1040444, 1130062, 1335379)
scheme_id      |text code scheme identifier (SN, R2, CTV3, EMLOC)
Term           | code text description
ceg_16         | ethnicity categorisation using CEG 16+1
ceg_16_term    | CEG ethnicity categories text description
nhs_5          | ethnicity categorisation using NHS 5+1
nhs_5_term     | NHS 5+1 ethnicity categories text description
nhs_16         | ethnicity categorisation using NHS 16+1
nhs_16_term    | NHS 16+1ethnicity categories text description
sn_concept     | SNOMED concept id
sn_description | SNOMED description id
sn_term        | SNOMED code term

identifier | code scheme
-----------| ------------------------
71         | SNOMED
1040444    | Read 2
1130062    | CTV3
1335379    | EMIS Local
SN         | SNOMED
R2         | Read 2
CTV3       | CTV3
EMLOC      | EMIS Local

### Ethnicity Key: `lu_ethnicity_key`

fieldname  | description
-----------| ------------------------
ethnic_std | ethnicity standard
Category   | category letter used with ethnicity standard
Term       | category text term

## Ethnicity SDE: `lu_ethnicity_sde`

fieldname      | description
------------   | ------------------------
id             | row identifier
sn_code        | SNOMED concept id
sn_name        | SNOMED description id
sn_description | SNOMED code term
sde_5          | summary grouping of the 18+1 categories code value
sde_5_name     | summary grouping of the 18+1 categories text description
sde_18         | Self-Defined Ethnicity 18+1 code value
sde_18_name    | Self-Defined Ethnicity 18+1 text description

***
## GP Practice: `lu_practice`

fieldname       | description
------------    | ------------------------
area_id         | area identifier for GP Practice (CH, NH, TH, WF, BK, HV, RB). This equates to the former CCGs and current Place-Based Partnerships or Areas within the [North East London ICB](<https://northeastlondon.icb.nhs.uk/>).
area            | area name
ods_code        | ODS (Organisation Data Service) identifier for the GP Practice. <https://odsportal.digital.nhs.uk/>
practice_name   | GP Practice name, as defined for CEG reporting. This may differ from the name on ODS records.
listsize        | currently registered patient count for practice at the run date
status          | activity status for the practice at the run date (active, inactive)
start_date      | date the practice opened
end_date        | date the practice closed
pcn_ods         | ODS identifier for the Primary Care Network (PCN) associated with the practice
pcn_name        | name of associated PCN
clinical_system | clinical data system used by the practice (EMIS, SystmOne)
uprn            | Unique Property Reference Number (UPRN) identifier for the address of the practice. <https://uprn.uk/>

identifier | area
-----------| ------------------------
CH         | City & Hackney
NH         | Newham
TH         | Tower Hamlets
WF         | Waltham Forest        
BK         | Barking & Dagenham
HV         | Havering
RB         | Redbridge

***
## Smoking: `lu_smoking`

fieldname       | description
------------    | ------------------------
id              | row identifier
code            | code (SNOMED, Read2, CTV3, EMIS Local)
scheme          | code scheme identifier (71, 1040444, 1130062, 1335379)
name            | code text description
ndasmok_cod     | code inclusion in National Diabetes Audit (NDA) code cluster (NDASMOK_COD)
smok_cod        | code inclusion in Quality Outcomes Framework (QOF) code cluster (SMOK_COD, NULL)
smok_status_qof | Quality Outcomes Framework (QOF) code cluster associated with code (LSMOK_COD, EXSMOK_COD, NSMOK_COD, NULL)
smok_status     | smoking status based on code term and/or QOF code cluster (CSMOK, NONSMOK, EXSMOK, NSMOK, UNKNOWN)
dbid            | database identifier for code
sn_dbid         | database identifier for SNOMED code associated with code

identifier | code scheme
-----------| ------------------------
71         | SNOMED
1040444    | Read 2
1130062    | CTV3
1335379    | EMIS Local

identifier | smoking status
-----------| ------------------------
LSMOK_COD  | Smoker
EXSMOK_COD | Exsmoker
NSMOK      | Never Smoked
CSMOK      | Current Smoker
NONSMOK    | Current Non-Smoker
EXSMOK     | Exsmoker
UNKNOWN    | smoking status cannot be defined

### Smoking Key: `lu_smoking_key`

fieldname   | description
------------| ------------------------
Id          | numeric identifier to smoking status
smok_status | smoking status
name        | name term for smoking status
