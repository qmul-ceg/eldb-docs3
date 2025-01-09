# Registers

The register tables contain all patients with a specified diagnosis or long term condition. The business rules syntax used to create the table is provided with cluster_id(s) and date ranges.

## Standard Fields
Each table has the following fields:

fieldname   | description
----------  |------------
label       | descriptive label of the table contents. Be 'diabetes'
area_id     | area id for GP Practice
ods_code    | ODS (Organisation Data Service) identifier for the GP Practice.
person_id   | identifier of person
patient_id  | identifier of patient at a practice

Additional fields specific to the table are described below.

***
## Anxiety: `anxiety`
Anxiety code (ANX_CEG) recorded \>= last 24 months.

fieldname   | description
----------  |------------
latest_date | latest date of code for register
latest_code | SNOMED concept id for latest code
latest_name | code term for latest code

Anxiety covers a range of Common Mental Health disorders, including

-   Generalised Anxiety and Panic Attacks
-   Anxiety associated with specific behaviours or situations
-   Phobias
-   Obsessive-Compulsive behaviour (OCD)
-   Post-Trauma Stress (PSTD)
-   Occupation-related Stress
  
***
## Asthma: `asthma`
Asthma code (AST_COD) excluding patients with a more recent resolved code (ASTRES_COD), and include Asthma Treatment meds code (ASTTRT_COD) recorded \>= last 12 months. (QOF)

fieldname     | description
----------    |------------
earliest_date | earliest, ie diagnosis, date of code for register
earliest_code | SNOMED concept id for earliest code
earliest_name | code term for earliest code

***
## Atrial Fibrillation: `atrial_fibrillation`
Atrial Fibrillation code (AFIB_COD) excluding patients with a more recent resolved code (AFIBRES_COD)

fieldname     | description
----------    |------------
earliest_date | earliest, ie diagnosis, date of code for register
earliest_code | SNOMED concept id for earliest code
earliest_name | code term for earliest code

***
## Autism: `autism`
*Autism code (AUTISM_COD) recorded ever*

fieldname     | description
----------    |------------
earliest_date | earliest, ie diagnosis, date of code for register
earliest_code | SNOMED concept id for earliest code
earliest_name | code term for earliest code

***
## Cancer: `cancer`
*Cancer code (CAN_COD) recorded \>= 2003-04-01*

fieldname     | description
----------    |------------
earliest_date | earliest, ie diagnosis, date of code for register
earliest_code | SNOMED concept id for earliest code
earliest_name | code term for earliest code

***
## Chronic Heart Disease: `chd`
*CHD code (CHD_COD) recorded ever*

fieldname     | description
----------    |------------
earliest_date | earliest, ie diagnosis, date of code for register
earliest_code | SNOMED concept id for earliest code
earliest_name | code term for earliest code

***
## Chronic Kidney Disease: `ckd`
*Aged \>= 18 years, and CKD code (CKD_COD) excluding patients with a more recent resolved code (CKDRES_COD) or a more recent CKD 1 or 2 code (CKD1AND2_COD)*

fieldname     | description
----------    |------------
earliest_date | earliest, ie diagnosis, date of code for register
earliest_code | SNOMED concept id for earliest code
earliest_name | code term for earliest code

***
## Chronic Obstructive Pulmonary Disease: `copd`
COPD code (COPD_COD) excluding patients with a more recent resolved code (COPDRES_COD), and where patients have a previous resolved code (COPDRES_COD), COPD code (COPD_COD) after the latest resolved code (COPDRES_COD)

fieldname     | description
----------    |------------
earliest_date | earliest, ie diagnosis, date of code for register
earliest_code | SNOMED concept id for earliest code
earliest_name | code term for earliest code

***
## Dementia: `dementia`
Dementia code (DEM_COD) recorded ever

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Depression

**depression**
*Aged \>= 18 years, and Depression code (DEPR_COD) recorded \>= 2006-04-01 excluding patients with a more recent resolved code
(DEPRES_COD)*

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code
-   latest_date -- latest, ie diagnosis, date of code for register
-   latest_code -- SNOMED concept id for latest code
-   latest_name -- code term for latest code

## Diabetes Mellitus (DM)
**diabetes**
*Aged \>= 18 years, and Diabetes code (DM_COD) excluding patients with a more recent resolved code (DMRES_COD). Selecting most recent Diabetes Type code (DMTYPE1_COD, DMTYPE2_COD) to define diabetes type.*

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code
-   dm_type - diabetes type (TYPE_1 or TYPE_2) for each patient.

## Eating Disorder
**eating_disorder**
*Eating disorder code (EATINGDIS_CEG) recorded \>= last 24 months*

-   latest \_date -- latest date of code for register
-   latest_code -- SNOMED concept id for latest code
-   latest_name -- code term for latest code

## Epilepsy
**epilepsy**
Epilepsy code (EPIL_COD) excluding patients with a more recent resolved code (EPILRES_COD), and include Epilepsy Drug meds code (EPILDRUG_COD) recorded \>= last 6 months

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Familial Hypercholesteremia (FH)
**f_hypercholesterolemia**
Familial Hypercholestelemia code (FHYP_COD) recorded ever

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Gestational Diabetes
**gestational_diabetes**
Gestational diabetes code (GESTDIAB_COD) recorded ever

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Heart Failure (HF)

**heart_failure**
Heart failure code (HF_COD) excluding patients with a more recent resolved code (HFRES_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Hepatitis B
**hepatitis_b**
*Hepatitis B code (HBV_CEG) recorded ever*

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code
-   latest_date -- latest, ie diagnosis, date of code for register
-   latest_code -- SNOMED concept id for latest code
-   latest_name -- code term for latest code

## Hepatitis C
**hepatitis_c**
*Hepatitis C code (HCV_CEG) recorded ever*

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code
-   latest_date -- latest, ie diagnosis, date of code for register
-   latest_code -- SNOMED concept id for latest code
-   latest_name -- code term for latest code

## Human Immunodeficiency Virus (HIV)
**hiv**
HIV code (HIV_CEG) recorded ever

-   latest_date -- latest date of code for register
-   latest_code -- SNOMED concept id for latest code
-   latest_name -- code term for latest code

## Hypertension (HT)
**hypertension**
Hypertension (HYP_COD) excluding patients with a more recent resolved code (HYPRES_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Learning Disabilities (LD)
**learning_disabilities**
Learning Disabilities code (LD_COD) recorded ever

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Motor Neurone Disease (MND)
**motor_neurone_disease**
Motor Neurone Disease code (MND_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Multiple Sclerosis (MS)
**multiple_sclerosis**
Multiple Sclerosis code (MS_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Non-Diabetic Hyperglycaemia (NDH)
**non_dm_hyperglycaemia**
Aged \>= 18 years, and Non-Diabetic Hyperglycaemia code (NDH_COD) or IGT code (IGT_COD) or Pre-Diabetes code (PRD_COD) excluding patients with a Diabetes code (DM_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Obesity
**obesity**
Aged \>= 18 years, and BMI Value code (BMIVAL_COD) \>=30 recorded \>= last 12 months, or Non-Value BMI Indicating \>= 30 code (BMI30_COD) recorded \>= last 12 months

-   latest12m_date -- latest date of code for register in the last 12 months
-   latest12m_code -- SNOMED concept id for latest code in the last 12 months
-   latest12m_name -- code term for latest code in the last 12 months
-   bmi30plus_latest12m_date -- latest date of code for register in the last 12 months with BMI \>=30
-   bmi30plus_latest12m_code -- SNOMED concept id for latest code in the last 12 months with BMI \>=30
-   bmi30plus_latest12m_name -- code term for latest code in the last 12 months BMI \>=30

## Osteoporosis
**osteoporosis**
Osteoporosis code (OSTEO_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Palliative Care
**palliative_care**
Palliative Care code (PALCARE_COD) excluding patients with a more recent not indicated code (PALCARENI_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Parkinson's Disease
**parkinsons_disease**
Parkinson\'s Disease code (PD_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Peripheral Arterial Disease (PAD)
**pad**
PAD code (PAD_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Personality Disorder
**personality_disorder**
Personality Disorder code (PERSONALITYDIS_CEG)

-   latest_date -- latest date of code for register
-   latest_code -- SNOMED concept id for latest code
-   latest_name -- code term for latest code

## Psoriasis
**psoriasis**
Psoriasis code (PSORIASIS_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Rheumatoid Arthritis
**rh_arthritis**
Aged \>= 16 years, and Rheumatoid Arthritis code (RARTH_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Severe Mental Illness (SMI)
**severe_mental_illness**
Mental Health code (MH_COD) excluding patients with a more recent remission code (MHREM_COD), and include Lithium meds code (LIT_COD) recorded \>= last 6 months excluding patients with a more recent Lithium Stopped code (LITSTP_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code
-   lithium_latest_date -- latest, ie prescription, date of code for medication recorded \>= last 6 months
-   lithium_latest_code -- SNOMED concept id for latest code medication recorded \>= last 6 months
-   lithium_latest_name -- code term for latest code medication recorded \>= last 6 months

Mental Health excluding remission + Lithium (6m) excluding Lithium Stopped

MH includes both schizophrenia and bipolar disorder and anyone on lithium who is not also coded having these conditions.

## Sexually Transmitted Infection (STI)
**sti**
Sexually Transmitted Infection code (STI_COD)

-   latest_date -- latest date of code for register
-   latest_code -- SNOMED concept id for latest code
-   latest_name -- code term for latest code

## Sickle Cell Disease (SCD)
**sickle_cell**
Sickle Cell code (SICKLE_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code

## Stroke or Transient Ischaemia Attack (TIA)
**stroke_tia**
Stroke code (STRK_COD) or TIA code (TIA_COD)

-   earliest_date -- earliest, ie diagnosis, date of code for register
-   earliest_code -- SNOMED concept id for earliest code
-   earliest_name -- code term for earliest code