# Clinics Ground Truthing (Pilot)

Version: 0.2

Date: 13-Dec-2024

## General information
### Facility name

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
| text          | name  | What is the name of the facility? | | | yes | |

### Facility address

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
| text          | address  | What is the address of the facility? | | | yes | |

### Facility state or county

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
| select_one          | state  | What state is this facility in? | | | yes | |

*Is this needed? The form will be specific for pilot and main study.  If so, what are the options?*

### Facility sub-county or local government area

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
| select_one          | state  | What sub-county or local government area is this facility in? | | | yes | |

*What are the options?*

### Facility location

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
| geopoint          | location  | What is the location of the facility? | | | no | |

### Registration number

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
| integer         | reg_no  | What is the registration number of the facility? | | | yes | |

*Is this required? What does the number look like?*

### Landmark

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|           |   | What is the address of the facility? | | | yes | |

*What does this question mean? What does the response look like?*

### Contact details of the manager - name

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     text      | manager_name  | What is the name of the health facility manager? | | | yes | |

*Is this required? (Required means the question cannot be skipped)*

### Contact details of the manager - contact number

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     integer      | manager_number  | What is the contact phone number of the health facility manager? | | | yes | |

*Is this required? (Required means the question cannot be skipped)*

### Contact details of the manager - contact number

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     select_one      | current_services  | Is the facility currently providing services? | | | yes | |

Options: yes, no

## Status of the health facility and services

### Ownership

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     select_one      | ownership  | What is the ownership status of the facility? | | | yes | |

*Does this need a don't know option?*

Options: government, non-governmental organization, faith-based organization, private

### Clinic size

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     select_one      | size  | What is the category of this facility in terms of size? | | | yes | |

*Is the question text correct?*

Options: consulting clinic (no inpatient facilities), health centre (outpatients and inpatients, ten or fewer beds), hospital (outpatients and inpatients, more than ten beds)

### Consulting fees

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     select_one      | user_fees  | Do patients pay a consultation or user fee to see a health provider? | | | yes | |

Options: yes, no

### Structure

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     select_one      | structure  | What type of structure is the facility in? | | | yes | |

Options: bungalow, multi-storey building, multiple buildings in premises

### Walk-in services

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     select_one      | walkin_services  | Does this clinic offer walk-in care for diagnosis, treatment, and/or referral? | | | yes | |

Options: yes, no

### Type of walk-in services

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     select_multiple      | walkin_services_spy  | What type of walk-in services does this clinic offer? | walkin_services == "yes" | | yes | |

Options: prevention, diagnosis, treatment, rehabilitation, palliative

## Staffing

### Clinical staff strength

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     integer      | total_staff  | What is the total number of clinical staff providing services? | | | yes | |

*Is this unique number of staff regardless of amount of time?*

Add check - does this total match the total of the next seven questions?

### Number of doctors

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     integer      | total_doctors  | What is the total number of doctors providing services? | | | yes | |

*Is this unique number of staff regardless of amount of time?*
*Is this question redundant given that we collect the number of sessions per staff member below?*

### Number of nurses and midwives

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     integer      | total_nurse  | What is the total number of nurses and midwives providing services? | | | yes | |

*Is this unique number of staff regardless of amount of time?*
*Is this question redundant given that we collect the number of sessions per staff member below?*

### Number of pharmacists

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     integer      | total_pharmacist  | What is the total number of pharmacists providing services? | | | yes | |

*Is this unique number of staff regardless of amount of time?*
*Is this question redundant given that we collect the number of sessions per staff member below?*

### Number of laboratory scientists

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     integer      | total_lab  | What is the total number of laboratory scientists providing services? | | | yes | |

*Is this unique number of staff regardless of amount of time?*
*Is this question redundant given that we collect the number of sessions per staff member below?*

### Number of community health officers

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     integer      | total_cho  | What is the total number of community health officers providing services? | | | yes | |

*Is this unique number of staff regardless of amount of time?*
*Is this question redundant given that we collect the number of sessions per staff member below?*

### Number of community health extension workers

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     integer      | total_chew  | What is the total number of community health extensions workers providing services? | | | yes | |

*Is this unique number of staff regardless of amount of time?*
*Is this question redundant given that we collect the number of sessions per staff member below?*

### Number of other clinical staff

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|     integer      | total_cho  | What is the total number of other clinical staff providing services? | | | yes | |

*Is this unique number of staff regardless of amount of time?*
*Is this question redundant given that we collect the number of sessions per staff member below?*

## Sessions of service provision

Repeated block of two questions

### Sessions of service provision - type

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|    select_multiple      | sessions_type  | What is the cadre of the staff members? | | | yes | yes |

Options: Doctor, nurse/midwife, pharmacist, laboratory scientist, community health officer, community health extension worker, other

### Sessions of service provision - number

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|    integer      | sessions_count  | How many sessions does this staff member provide per week? | | | yes | yes |

## Services provided

### Services provided

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|    select_multiple      | services  | What services are provided at the clinic? | | | yes |  |

Options: Inpatient admissions, surgical operations, labour and delivery, laboratory tests, X-ray services, ultrasound, mammography, pap smear, visual inspection of cervix, other

### Services provided - other

| type          | name   | text                 | relevance | constraints | required | repeated |
|---------------|--------|-----------------------|-----------|----------|-----------|---------|
|    text      | services  | What services are provided at the clinic? | services includes "other" | | yes |  |
