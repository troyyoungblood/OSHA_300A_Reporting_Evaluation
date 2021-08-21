# OSHA_300_Log_Reporting_Evaluation
OSHA 300 log data review 2016 - 2020.  Injury and Illness reporting.

Purpose of activity was to evaluate and identify trends associated with services provided under Medicare Part B during the calendar year 2018 in Houston, Texas. 

<u>Brief Medicare overview</u>
<p>Original Medicare is a fee-for-service health plan with a Part A (Hospital Insurance) and a Part B (Medical Insurance).  After a person pays a deductible, Medicare pays its Medicare-approved amount and the patient pays the remainder.  Medicare Part D is drug insurance.  Medicare Advantage Part C is type of Medicare health plan offered by a private company that contracts with Medicare.</p>

<p>The Medicare Part B data was obtained from data.cms.gov, a federal government website managed by the Centers for Medicare & Medicaid Services, 7500 Security Boulevard, Baltimore, MD 21244</p>

<p>Link to data: https://https://www.osha.gov/Establishment-Specific-Injury-and-Illness-Data</p>

<u>Data Extraction and Transformation</u>
<p>The original dataset was downloaded as a csv file and it contained information from all locations providing Medicare Part B services in 2018.  The file size was approximately 2.2 GB and was to large to be effectively manage using a spreadsheet.  Python in Jupyter Notebook was used to amend column titles and create a subset of data containing only records of services provided in Houston, Texas.  The Houston only dataframe was exported to a csv file which could then be used to create charts for analysis in Tableau.</p>

<u>Data Review</u>

<p>Link to Tableau: https://public.tableau.com/app/profile/troy.youngblood/viz/OSHA_Injury_Data_Evaluation/Dashboard32?publish=yes</p>

Overall Statistics <br>

The total number of providers (discrete charging locations) is 10,436.  This number includes Clinical Laboratories that provide a wide range of services and specialty doctor's offices.<br>
<br>
The number of individuals that recieved different types of care was 14,390,509. An individual would get counted each time they received a different typr of care such as vaccine, eye exam, etc.  As noted below in the snip, a person (distinct Medicare Beneficiary) receiving multiple cardiac stints in a day would be counted as 1 to remove double-counting. <br>
<br>
The total Medicare Part B payments to Houston area providers in 2018 was $750,066,174.<br>
<br>
<br>
<p>Data Highlights (values are rounded for reporting ease)</p>
<br>
<br>
<p>The Top 5 Medical Provider Types by number of providers are:</p>
<p>Nurse Practitioners with 959 providers identified in the data set supporting 332,000 patients.  Note - Nurse Practitioners were not broken out by specialty in the raw data set.  They were included becuase of the total number responsible for providing care and the total number of patients supported.</p>
<p>Internal Medicine with 848 providers identified supporting 945,000 patients.</p>
<p>Anesthesiology with 613 providers identified supporting 132,000 patients.</p>
<p>Diagnostic Radiology with 562 providers supporting 1,215,000 patients.</p>
<p>Family Practice with 555 providers supporting 417,000 patients.</p>
<br>
<br>
<p>The Top 5 Medical Provider Types by number of patients supported are:</p>
<p>Clinical Laboratories - 5,514,000 patients supported</p>
<p>Diagnostic Radiology - 1,215,000 patients supported.</p>
<p>Internal Medicine - 945,000 patients supported.</p>
<p>Cardiology - 681,000 patients supported.</p>
<p>Ophthalmology - 469,000 patients supported.</p>
<br>
<br>
<p>The Top 5 Receiving Medicare Part B payments</p>
<p>Clinical Laboratories - $87M</p>
<p>Internal Medicine  - $62M</p>
<p>Cardiology - $51M</p>
<p>Ophthalmology - $49</p>
<p>Diagnostic Radiology - $42M</p>
<br>
<br>
<p>The top 15 medications by units administered are:</p>
<p>Ferumoxytol to treat iron-deficiency anemia.</p>
<p>Onabotulinumtoxina to control muscle spasms and reduce wrinkles.</p>
<p>Certolizumab Pegol to reduce pain and swelling due to specific inflammatory conditions.</p>
<p>Darbepoetin Alfa to treat anemia in individuals with chronic kidney failure.</p>
<p>Denosumab to offset bone loss in cancer patients resulting from treatment.</p>
<p>Testosterone Cypionate to address testosterone deficiency.</p>
<p>Filgrastim used in individulas with chronic neutropenia, to prepare blood for leukapheresis or for individuals undergoing bone marrow transplants.</p>
<p>Ferric Carboxymaltose to treat iron-deficiency anemia.</p>
<p>Abatacept is used to reduce pain, swelling and other issues associated with rheumatoid arthritis.</p>
<p>Immune Globulin is blood collected from many individuals that is adminstered to reduce severity of certain infections in at risk patients.</p>
<p>Ranibizumab is used to treat certain serious eye condicitons.</p>
<p>Dexmathasone Sodium Phosphate is used the treat inflammation associated with many different disorders.</p>
<p>Tocilizumab is used for certainb types of arthritis treatment.</p>
<p>Daptomycin is used to treat certain blood or serious skin infections.</p>
<p>Influenza virus vaccine.</p>

<p>Link to Tableau with additonal charts and data: https://public.tableau.com/app/profile/troy.youngblood/viz/medicare_Houston_CY2018/Story1?publish=yes</p>
<br>
<br>
<p>Snips of Data</p>
<br>
<img src="images/intro.PNG" width = "675"><br>
<br>
<br>
<br>
<br>
<img src="images/2_provider1.PNG" width = "675"><br>
<br>
<br>
<br>
<br>
<img src="images/3_provider2.PNG" width = "675"><br>
<br>
<br>
<br>
<br>
<img src="images/4_noclprovider.PNG" width = "675"><br>
<br>
<br>
<br>
<br>
<img src="images/5_providerpayment.PNG" width = "675"><br>
<br>
<br>
<br>
<br>
<br>
<img src="images/6_deltacharge.PNG" width = "675"><br>
<br>
<br>
<br>
<br>
<img src="images/7_chargecodes1.PNG" width = "675"><br>
<br>
<br>
<br>
<br>
<img src="images/8_drugsissued1.PNG" width = "675"><br>
<br>

