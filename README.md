# OSHA_300A_Reporting_Evaluation
OSHA 300A submission review 2016 - 2020.  Injury and Illness reporting.

Presentation of information associated with illness and injury reporting under OSHA  - OSHA Form 300A (Summary of Work-Related Injuries and Illnesses) from 2016 -2020.  

<u>OSHA 300A overview</u>
<p>On an annual basis, designated employers are required to submit their OSHA 300A information. https://www.osha.gov/recordkeeping </p>

<p>An OSHA recordable injury or illness is required to be included in the log.  OSHA defines a recordable injury or illness as:
<br>
 - Any work-related fatality
<br>
 - Any work-related injury or illness that results in loss of consciousness, days away from work, restricted work, or transfer to another job
<br> 
 - Any work-related injury or illness requiring medical treatment beyond first aid
<br> 
 - Any work-related diagnosed case of cancer, chronic irreversible diseases, fractured or cracked bones or teeth, and punctured eardrums
<br> 
 - There are also special recording criteria for work-related cases involving: needlesticks and sharps injuries; medical removal; hearing loss; and tuberculosis.</p>
<br>
<br>
First aid is defined below.
<br>

<u>Data Review</u>

<p>Link to Tableau: https://public.tableau.com/app/profile/troy.youngblood/viz/OSHA_Injury_Data_Evaluation/Dashboard32?publish=yes</p>
<br>
<p>Overall Statistics 2016 - 2020</p>
California has the most number of employers reporting during the period at 132,492.  Based on 2017-2020 data, California appears to have an under reporting value of approximately 23,000 in 2016. Taking that into account, California should actually be in the range of 162,000 employers reporting.  Wyoming has the least value at 2,127. 



<u>Data Extraction and Transformation</u>
<p>Information was pulled from two locations.  North American Industry Classification System (NAICS) codes and descriptions where obtained from https://www.naics.com/search/.  The NAICS codes are used to group injury and illness information under related work descriptions.  Injury and illness data was pulled from: https://www.osha.gov/Establishment-Specific-Injury-and-Illness-Data.  Data was availalbe for 2016, 2017, 2018, 2019, and 2020.  All avaialbe years of data are used in this evaluation.</p>
<br>
<p>Using Python in Jupyter Notebook, the OSHA data was merged into a single file. After the combined OSHA data file was created, the "initial" NAICS file was merged on the naics_code column in the OSHA data file.  The resulting file was approximately 431MB and over 1.3 million rows of data.  The data was evalauted to determine if there were any issues that would create problems during visualization and also identify opportunities to improve data review.    The primary issues identified were state abbreviations were incorrectly entered, industry_description was not consistently entered (missing from ~100k rows), and many errors with hours and or employee count data.   State abbreviations and missing industry_description data was corrected during cleanup steps in Python and OSHA data entry was corrected in excel after the Python work was complete.  Other minor cleanup in Python included dropping rows and filling some NaN with information from another column.</p>
<br>
<p>The data correction in excel required 





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

Using a non-prescription medication at nonprescription strength (for medications available in both prescription and non-prescription form, a recommendation by a physician or other licensed health care professional to use a non-prescription medication at prescription strength is considered medical treatment for recordkeeping purposes);
Administering tetanus immunizations (other immunizations, such as Hepatitis B vaccine or rabies vaccine, are considered medical treatment); Cleaning, flushing or soaking wounds on the surface of the skin
Using wound coverings such as bandages, Band-Aids™, gauze pads, etc.; or using butterfly bandages or Steri-Strips™ (other wound closing devices such as sutures, staples, etc., are considered medical treatment);
Using hot or cold therapy;
Using any non-rigid means of support, such as elastic bandages, wraps, non-rigid back belts, etc. (devices with rigid stays or other systems designed to immobilize parts of the body are considered medical treatment for recordkeeping purposes);
Using temporary immobilization devices while transporting an accident victim (e.g., splints, slings, neck collars, back boards, etc.). Drilling of a fingernail or toenail to relieve pressure, or draining fluid from a blister;
Using eye patches;
Removing foreign bodies from the eye using only irrigation or a cotton swab;
Removing splinters or foreign material from areas other than the eye by irrigation, tweezers, cotton swabs or other simple means;
Using finger guards;
Using massages (physical therapy or chiropractic treatment are considered medical treatment for recordkeeping purposes); or
Drinking fluids for relief of heat stress.
