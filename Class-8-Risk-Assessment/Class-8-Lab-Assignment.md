Class 8: Lab Assignment
Scenario 1: Quantitative Risk Assessment
You are a Security Analyst for "Global Logistics Corp." The company relies heavily on a central database server to track shipments worldwide. Management is considering purchasing a new security control—a specialized Intrusion Prevention System (IPS)—to protect this server, but they need you to justify the cost using quantitative risk analysis.

Current State Data:

Asset Value (AV) of the Database Server: $200,000
Exposure Factor (EF) of a successful attack: 25% (0.25)
Historical frequency of successful attacks: Once every 10 years (ARO = 0.1)

 
Proposed Control Data:
Cost of the IPS Control: $15,000 per year

Vendor Claim: The IPS will reduce the frequency of successful attacks to once every 100 years (New ARO = 0.01). The Exposure Factor remains the same.

Task 1: Calculate Current Risk
Calculate the current Single Loss Expectancy (SLE). Show your work.
Calculate the current Annualized Loss Expectancy (ALE). Show your work.

Task 2: Evaluate Proposed Control
Calculate the new Annualized Loss Expectancy (ALE) if the IPS control is implemented. Show your work.

Task 3: Cost-Benefit Analysis
Based on your calculations, is purchasing the $15,000 IPS control a sound financial decision for the company? Explain your reasoning.
 

Scenario 2: Data Classification and Privacy Frameworks
You are a Compliance Officer for "MediCare Plus," a regional healthcare provider in the US. The organization is launching a new telemedicine platform that will be available to international patients, including citizens of the European Union. Before launch, you must audit the data inventory, apply the correct privacy frameworks, and assign classification levels.

 Data Inventory:

Patient Medical Records: Diagnoses, prescriptions, treatment plans, and doctor's notes.
Patient Contact Information: Full names, physical addresses, email addresses, and phone numbers.
Payment Information: Credit card numbers, billing addresses, and insurance policy details.
Marketing Materials: Publicly available brochures, service descriptions, and pricing tiers.
 

Classification Levels Available:
Restricted: Highest level of protection required by law.
Confidential: PII that requires protection but is less sensitive than medical records.
Public: Intended for public distribution; no confidentiality risk.

Task 4: Apply Frameworks and Classify Data
For each data type in the inventory, identify the applicable regulatory framework(s) (HIPAA, GDPR, PCI-DSS, or N/A) and assign the appropriate internal classification level.
 

Patient Medical Records:
Framework(s): _______________________________________________________________________________________________________
Classification: ___________________________________________________________________________________________________________________________

Patient Contact Information:
Framework(s): _____________________________________________________________________________________________________
Classification: ______________________________________________________________________________________________________

Payment Information:
Framework(s): _____________________________________________________________________________________________
Classification: _______________________________________________________________________________________________________

Marketing Materials:
Framework(s): _____________________________________________________________________________________________
Classification: ___________________________________________________________________________________________________

Task 5: Scenario Application
Answer the following questions based on your classifications.

A developer wants to use real patient medical records in a testing environment to ensure the new platform works correctly. Based on the classification, is this allowed? Why or why not?

The marketing team wants to email a newsletter to all patients. Which privacy framework(s) must they consider before sending the emails, especially to European patients?
 

If the database storing payment information is breached, what specific regulatory standard has the organization likely failed to comply with?



Scenario 1 — Quantitative Risk Assessment

Task 1A — Calculate Current Single Loss Expectancy (SLE)
$50,000

Task 1B — Calculate Current Annualized Loss Expectancy (ALE)
$5000

Task 2 — Calculate New ALE with IPS
50k x 0.01 = 500 + 15k/yr (10yrs) =$150,500

Task 3 — Cost-Benefit Analysis
Recommend not investing $15k/yr for IPS because ALE is significantly less than IPS cost

--------------------------------

Scenario 2 — Data Classification & Privacy Frameworks

Task 4 — Patient Medical Records
HIPAA
Restricted

Task 4 — Patient Contact Information
HIPAA
Confidential 

Task 4 — Payment Information
PCI-DSS
Confidential

Task 4 — Marketing Materials
N/A
Public

Task 5A — Use of Real Medical Records in Testing
Not allowed. Patient info is restricted and should not be available for viewing or testing

Task 5B — Marketing Newsletter Privacy
GDPR, HIPAA

Task 5C — Payment Database Breach
PCI-DSS.  Cardholder data was not protected