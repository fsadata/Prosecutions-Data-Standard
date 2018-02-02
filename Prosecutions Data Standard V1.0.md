# Prosecutions Data Standard 

### What Is This Document?

This document describes the data standard for submitting food sampling results data to the Food Standards Agency. It describes the fields, their data types and order as well as providing specific guidance on acceptable values and which fields use specific reference data values.

This document does not describe the mechanism by which data can be submitted to the Food Standards Agency (the FSA).

### Who Is This Document For?

This document is written for Local Authority users who need to submit sampling and results data to the FSA.

### How This Document Is Structured

- [Prosecutions Standard Overview](#Prosecutions-standard-overview) Contains a brief overview of all the fields in the standard.  
- [Field Definitions](#field-definitions) Complete definitions for each field in the standard, includes constraints and specific data type formatting requirements.  
 1. [FBO](#1-fbo)  
 2. [TA Name](#2-ta-name) 
 3. [Defendant](#3-defendant)
 4. [Prem Address1](#4-prem-address1)  
 5. [Post Town](#5-post-town)  
 6. [County](#6-county)  
 7. [Postcode](#7-postcode)  
 8. [Offence Category](#8-offence-category)  
 9. [Offence Provision](#9-offence-provision)  
 10. [EU Contravention](#10-eu-contravention)  
 11. [Nature_of Offence](#11-nature-of-offence)  
 12. [Date of Conviction](#12-date-of-conviction)  
 13. [Conviction Plea](#13-conviction-plea)  
 14. [Court Name](#14-court-name)  
 15. [Country](#15-country)  
 16. [Sentence](#16-sentence)  
 17. [Costs Awarded](#17-costs-awarded)  
 18. [Prosecution_Authority](#18-prosecution-auth)  
 19. [LA Reg](#19-la-reg)  
 20. [Company No](#20-company-no)  
 21. [Prohibited Order](#21-prohibited-order)  
 22. [Approval No](#22-approval-no)  
 23. [UPRN](#23-uprn)  
 24. [Individual](#24-individual)  
 25. [Date of Sentence](#25-date-of-sentence)  
 26. [Sentence Type](#26-sentence-type)  
 27. [Order Date](#27-order-date)  
 28. [Sentence Date](#28-sentence-date)  
 29. [Imprisonment](#29-imprisonment)   
 30. [Fine](#30-fine) 

- [Supported File Types](#supported-file-types)
- [Other Requirements](#other-requirements)
- [File Naming Conventions](#file-naming-conventions)

## Food Standard Overview

The following table lists the fields (name and description), their data types, whether they are optional, and whether they use a controlled vocabulary.

Index | Field Name | Description | Data Type | Optional | Controlled Vocabulary | Source
------|------------|-------------|-----------|----------|-----------------------|-------  
1|fbo|FBO|Text|No|No|LA
2|ta_name|Trading Name|Text|Yes|No|LA
3|defendant|Defendant's Name|Text|No|No|LA
4|prem_address1|First line of premises address|Text|No|No|LA
5|post_town|Postal Town|Text|No|No|LA
6|county|County of premises|Text|No|No|LA
7|post_code|Postal Code of the of the premises|Text|No|Yes|LA
8|offence_category|Category of the offence|Text|No|Yes|LA
9|offence_provision|Relevant offence provision|Text|No|Yes|LA
10|eu_contravention|EU regulation contravened|Text|No|Yes|LA
11|nature_of_offence|The nature of the offence|Text|No|No|LA
12|date_of_conviction|Conviction date|number|No|No|LA
13|conviction_plea|Conviction Plea|Text|No|Yes|LA
14|court_name|Name of the Court|Date|No|Yes|LA
15|country|Country|Number|No|Yes|LA
16|sentence|Resulting sentence|Text|Yes|Yes|LA
17|costs_awarded|Costs awarded|Text|Yes|No|LA
18|prosecution_auth|Prosecuting Local Authority|Text|No|Yes|LA
19|la_reg|Local Authority Regulation|Yes|Yes|LA
20|company_no|Company Number|text|Yes|Yes|LA
21|prohibited_order|If a prohibited order is applied|text|No|Yes|LA
22|approval_no|Unique approval number|Text|No|Yes|LA
23|uprn|UPRN address identifier|Text|Yes|Yes|LA
24|individual|Whether defendant is an individual|Text|No|Yes|LA
25|date_of_sentence|Date of sentence|Date|Yes|Yes|LA
26|sentence_type|Type of Sentence|Number|No|Yes|LA
27|order_date|Date of provisional order|date|Yes|Yes|LA
28|payment_date|Date of payment|Text|Yes|Yes|LA
29|imprisonment|imprisonment flag|Text|No|Yes|LA
30|fine|Value of fine|number|Yes|No|LA

## Field Definitions

### 1. FBO
**Field Name:** `fbo`  
**Data Type:** Text  
**Optional:** No  
**Source:** Local Authority  
**Comments:** This is the textual identifier of the defendant, name or company name.

### 2. TA Name
**Field Name:** `ta_name`  
**Data Type:** (255 character limit)  
**Optional:** Yes  
**Source:** Local Authority  
**Comments:** Trading name of the company if relevant.

### 3. Defendant
**Field Name:** `defendant`  
**Data Type:** Text (256 character limit)  
**Optional:** No  
**Source:** Local Authority  
**Comments:** Name of defendant, could be a trading name.  

### 4. Prem Address1
**Field Name:** `prem_address1`  
**Data Type:** Text (256 character limit)  
**Optional:** No  
**Source:** Local Authority  
**Comments:** First line of the premises address.

### 5. Post Town
**Field Name:** `post_town`  
**Data Type:** Text (255 character limit) 
**Optional:** No  
**Source:** Local Authority  
**Comments:** Postal town of the premises address.

### 6. County
**Field Name:** `county`  
**Data Type:** Text (255 character limit)  
**Optional:** No  
**Source:** Local Authority  
**Comments:** County of the premises address.  

### 7. Postcode
**Field Name:** `postcode`  
**Data Type:** Text (50 character limit)  
**Optional:** No  
**Source:** Local Authority  
**Comments:** Postal Code of the premises address.  

### 8. Offence Category
**Field Name:** `offence_category`  
**Data Type:** Text (controlled vocabulary)     
**Optional:** No  
**Source:** Local Authority  
**Comments:** Category of the Offence: 

 - `Food Hygiene` 
 - `Food Standards` 

### 9. Offence Provision
**Field Name:** `offence_provision`  
**Data Type:** Text (255 character limit)  
**Optional:** Yes  
**Source:** Local Authority  
**Comments:** Relevant regulation e.g. Regulation_19_1_Food_Safety_and_Hygiene_England_Regulations_2013.  

### 10. EU Contravention
**Field Name:** `eu_contravention`  
**Data Type:** Text (255 character limit)  
**Optional:** Yes  
**Source:** Local Authority  
**Comments:** Relevant EU Article contravened e.g. Article 4 (2) of Regulation 852/2004

### 11. Nature of Offence
**Field Name:** `nature_of_offence`  
**Data Type:** Text (255 character limit)   
**Optional:** No  
**Source:** Local Authority  
**Comments:** Brief textual description of the offence.
 
### 12. Date of Conviction
**Field Name:** `date_of_conviction`  
**Data Type:** Date (format: `YYYY-MM-DD hh:mm:ss`)  
**Optional:** Yes  
**Source:** Local Authority  
**Comments:** The date of conviction if applicable.

### 13. Conviction Plea
**Field Name:** `conviction_plea`  
**Data Type:** Text (controlled vocabulary)   
**Optional:** No  
**Source:** Local Authority  
**Comments:** The acceptable values for this field are:

 - 'Guilty Plea'
 - 'Not Guilty'
 - 'Guilty in Absentia'
 
### 14. Court Name
**Field Name:** `court_name`  
**Data Type:** Text (controlled vocabulary)   
**Optional:** No  
**Source:** Local Authority  
**Comments:** Name of Court.

### 15. Country
**Field Name:** `survey_id`  
**Data Type:** Text (controlled vocabulary)   
**Optional:** No  
**Source:** Local Authority  
**Comments:** Country of company (using set list).  

### 16. Sentence
**Field Name:** `sentence`  
**Data Type:** Text (255 character limit)  
**Optional:** No  
**Source:** Local Authority  
**Comments:** Brief textual description of sentence.  

### 17. Costs Awarded
**Field Name:** `costs_awarded`  
**Data Type:** Text (255 character limit)  
**Optional:** Yes  
**Source:** Local Authority  
**Comments:** Description and value of any costs awarded.  

### 18. Prosecution Authority
**Field Name:** `prosecution_auth`  
**Data Type:** Text (controlled vocabulary)   
**Optional:** No  
**Source:** Local Authority  
**Comments:** Name of the prosecuting Local Authority (set list).  

### 19. LA Reg
**Field Name:** `la_reg`  
**Data Type:** Text (controlled vocabulary)  
**Optional:** Yes  
**Source:** Local Authority  
**Comments:** LA regulations contravened.  

### 20. Company Number
**Field Name:** `company_no`  
**Data Type:** Text (50 character limit)  
**Optional:** Yes  
**Source:** Local Authority  
**Comments:** Company's House business company number if applicable.  

### 21. Prohibited Order
**Field Name:** `prohibited_order`  
**Data Type:** Text (255 character limit)  
**Optional:** No  
**Source:** Local Authority   
**Comments:** Whether a prohibited Order is applied. 

 The acceptable values for this field are:

 - 'Yes'
 - 'No'

### 22. Approval Number
**Field Name:** `approval_no`  
**Data Type:** Text (50 character limit)  
**Optional:** No  
**Source:** Local Authority  
**Comments:** Approval number, must be unique for entry and not left blank.  

### 23. UPRN
**Field Name:** `uprn`  
**Data Type:** Text (2000 character limit)  
**Optional:** Yes  
**Source:** Local Authority  
**Comments:** A Unique Property Reference Number (UPRN) for premises.  Is a unique alphanumeric identifier for every spatial address in Great Britain.  

### 24. Individual
**Field Name:** `individual`  
**Data Type:** Text (controlled vocabulary)  
**Optional:** No  
**Source:** Local Authority  
**Comments:** Whether prosecution is for a business or individual, is essential for calculating spent convictions.  

 The acceptable values for this field are:

 - 'Yes'
 - 'No'

### 25. Date of Sentence
**Field Name:** `date_of_sentence`  
**Data Type:** Date (format: `YYYY-MM-DD hh:mm:ss`)  
**Optional:** Yes  
**Source:** Local Authority  
**Comments:** Date of Sentence if applicable.

### 26. Sentence Type
**Field Name:** `sentence_type`  
**Data Type:** Text (controlled vocabulary)  
**Optional:** No  
**Source:** Local Authority  
**Comments:** Type of sentence received.  

 The acceptable values are:
 
 - `Conditional Discharge`
 - `Absolute Discharge`
 - `Compensation Order`  
 - `Community Order` 
 - `Not Applicable` 
 
### 27. Order Date
**Field Name:** `order_date`  
**Data Type:** Date (format: `YYYY-MM-DD hh:mm:ss`)  
**Optional:** Yes  
**Source:** Local Authority  
**Comments:** Date of any Provisional Orders if applicable, essential for spent conviction calculations.

### 28. Payment Date
**Field Name:** `payment_date`  
**Data Type:** Date (format: `YYYY-MM-DD hh:mm:ss`)  
**Optional:** Yes  
**Source:** Local Authority  
**Comments:** Date of any payments if applicable, essential for spent conviction calculations.

### 29. Imprisonment
**Field Name:** `imprisonment`  
**Data Type:** Number (decimal, two decimal places)  
**Optional:** Yes  
**Source:** Local Authority  
**Comments:** The length of any sentence in years to two decimal places, essential for spent conviction calculations.

### 30. Fine
**Field Name:** `fine`  
**Data Type:** Test (255 character limit)  
**Optional:** No  
**Source:** Local Authority  
**Comments:** Whether a fine has been applied.  

 The acceptable values for this field are:

 - 'Yes'
 - 'No'



## Supported File Types

Currently we are supporting the standard for comma separated values (CSV), Json and XML files.

The [current standard for CSV](https://tools.ietf.org/html/rfc4180) gives a detailed explanation of the common format for CSV files. It's concise and clear and we recommend reading it.

## Other Requirements

### Text Fields

The majority of the fields in the standard are text, which needs to be treated carefully when stored in a CSV file. All text fields must be enclosed within double quotes `"this is the text"`. You should try to avoid using double quotes within a text field as this can cause the field to be misread, but the RFC4180 standard allows it if handled appropriately.

>If double-quotes are used to enclose fields, then a double-quote appearing inside a field must be escaped by preceding it with another double quote. For example: `"aaa","b""bb","ccc"`

### Encoding

Where possible please use `UTF-8` encoding.

## File Naming Conventions

In order to make it easy for us to manage the files longer term, it will be important to name files so that we can tell who has submitted them and the time period that each file covers. The format will be the laboratory code from the laboratories register, and the date of submission in `YYYYMMDD` format.
