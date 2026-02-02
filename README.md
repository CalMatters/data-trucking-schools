# Data on trucking schools and state license status

This dataset compiles a list of 231 trucking schools in California. The list is based on the Federal Motor Carrier Safety Administration's [Training Provider Registry](https://tpr.fmcsa.dot.gov/Search). Providers self-register and self-certify they meet federal and state requirements.

CalMatters used the federal registry to estimate the number of trucking schools not regulated by California’s Bureau for Private Postsecondary Education (BPPE). In order to compile a comparable list of providers that may also be under the purview of the state bureau, we cleaned a list of 2,676 locations found in the federal database where providers self-registered they conducted training in California as of Jan. 8, 2026.

CalMatters first filtered out providers registered as “private enrollment only” (such as employer-based training programs). We then manually filtered out providers whose names and online presence indicated they were likely one of the following and not primarily a commercial driver license training school that charges tuition:

- Public school district; 
- Community college; 
- Municipal, utility, state or federal agency;
- Individual instructor; 
- Chauffeur, logistics or similar company. 

Because the federal database lists all locations separately, CalMatters consolidated branch locations of the same school based on name and contact information. We then matched schools to the state bureau’s list of approved private postsecondary educational institutions based on name, location and contact information. 

After compiling a comparable list, our analysis found at least 184 training providers listed on the federal registry that appear to be primarily operating as private trucking schools but were not approved by BPPE. To confirm whether a school is still operating, we used recent reviews and online listings, though some listings may be outdated, or we contacted the school directly.  

The dates we accessed each source are below. School information and status may have changed more recently.


## Data Sources
<table>
    <thead>
        <tr>
            <th>Source description</th>
            <th>Date accessed or received</th>
            <th>Notes</th>
            <th>Link to source</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Federal Motor Carrier Safety Administration Training Provider Registry</td>
            <td>2026-01-08</td>
            <td>The registry is intended to help drivers find training programs for operating commercial motor vehicles.</td>
            <td>https://tpr.fmcsa.dot.gov/Search</td>
        </tr>
        <tr>
            <td>BPPE list of licensed trucking schools</td>
            <td>2025-12-11</td>
            <td>Spokesperson Monica Vargas said the bureau ran a report based on program names to come up with an estimate and "exact numbers could not be known."</td>
            <td>email to CalMatters reporter</td>
        </tr>
        <tr>
            <td>BPPE School Search</td>
            <td>2025-01-08</td>
            <td>BPPE's public-facing search tool provides information about private postsecondary schools approved by the bureau.</td>
            <td>https://www.bppe.ca.gov/search/</td>
        </tr>
        <tr>
            <td>BPPE Exemption Verification Applications since March 2024</td>
            <td>2025-11-18</td>
            <td>A school can request official verification of exemption from BPPE inspection. Such verification is optional. A school may be exempt and not appear on the list.</td>
            <td>email to CalMatters reporter</td>
        </tr>
    </tbody>
</table>

## Data Dictionary
### `trucking-schools-status.csv`
Each row is a trucking school that appeared on the federal registry. The columns specify if the school also appeared on BPPE lists.

<table>
    <thead>
        <tr>
            <th>Field</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td>Name of trucking school as it appears in the federal registry</td>
        </tr>
        <tr>
            <td>bppe_approved_email</td>
            <td><code>TRUE</code> if school was matched to one in the list of BPPE-licensed trucking schools provided by the bureau via email. <code>FALSE</code> if no match was found</td>
        </tr>
        <tr>
            <td>bppe_approved_search</td>
            <td><code>TRUE</code> if school was matched to one in the list of BPPE-licensed schools on the bureau's public search. <code>FALSE</code> if no match was found</td>
        </tr>
        <tr>
            <td>bppe_exempt</td>
            <td><code>Approved</code> if school was matched to one on the BPPE-provided list of exemption verification applications and was verified exempt by the bureau. <code>Denied</code> if school was matched to one on the BPPE-provided list of exemption verification applications and was denied exemption verification by the bureau. <code>not on list</code> if no match was found</td>
        </tr>
    </tbody>
</table>

## List of trucking schools
Below is the same list of schools as in `trucking-schools-status.csv`, categorized whether they are licensed by BPPE or not. 

Notes:
- One school, International College, appeared on BPPE's list of approved schools but not in the federal registry, so it does not appear below.
- There are two separate licensed schools named “United Truck Driving School.” One has BPPE Institution Code 3707641 and the other 16825830.

### Schools on the federal registry that appeared on BPPE’s list of licensed trucking schools and/or BPPE’s verified school search
- 160 California, LLC dba 160 Driving Academy
- A-1 Truck Driving School Inc
- AAA Academy, LLC
- Academy of Truck Driving
- Advance Bus & Truck Driving School
- Advanced Career Institute
- AGT Trucking School
- America Truck Driving School, Inc.
- American Career Training
- C. R. England, Inc. DBA Premier Truck Driving School
- Center for Employment Training
- Central Valley Opportunity Center, Inc.
- Coastal Trucking Institute, LLC
- College of Instrument Technology, dba CIT, dba Heavy Equipment Driver College, dba HED College
- Dave School of Truck Driving
- Delancey Street Academy
- Domestic Truck Driving School
- East Valley College
- Easy Truck Rental, Repair, & Towing
- Edison Truck and Bus Driving School, Inc.
- Empire Trucking School LLC
- Green Valley Truck School
- GSF Driving & Truck Training School
- Hi-Desert Truck Driving School
- J&R Trucking School
- Jiffy's Truck School, LLC
- Jose G. Campos Truck Driving Training
- Masters Trucking Academy
- MTS Training Academy
- Nixon College
- Northwest Lineman College
- P. Steve Ramirez Vocational Training Centers
- Performance Trucking Academy, LLC
- Pilot Trucking School
- Roadmaster Drivers School of Fontana, Inc.
- Sergio School of Trucking
- Skyway Trucking School
- Transportation Guidance & Assistance Truck Driving School
- Truck Driver Institute
- United Truck Driving School
- United Truck Driving School
- Universal Truck Driving School, Inc
- Valencia Training Solutions, Inc. dva Valencia Trucking School
- Western Pacific Truck School
- Western Truck School
- William M. Maguy School of Education A Division of Proteus, Inc.

### Schools on the federal registry that did not appear on either BPPE source of licensed trucking schools
- 10-4 trucking
- 101 School of trucking
- A class truck driving school
- A Plus Trucking Academy Inc
- A.B.C. Schooling LLC
- A&B Truck & Bus Driving School
- A&J Truck Driving School
- A2Z TRUCK DRIVING SCHOOL INC
- AB TRUCK TRAINING LLC
- Abylex Inc Truck Driving School
- Akal Truck Driving School, LLC
- Ali's Truck Driving School LLC
- All In Cdl Training
- American Driving Club
- American Skilled Trade University (ASTU)
- American Tech Logistics / Las Americas
- american truck and bus driving school
- Antelope Truck Driving School
- Apache Truck Training Service
- Apex Truck Driving School
- Apna truck driving school
- Arjuna Global Transportation
- ASD Logistic Services, Inc.
- Atkar Truck Driving School
- Avon Truck Driving School Inc
- AZTLAN TRUCKING SCHOOL
- Bajwa Truck Driving School
- Bakersfield Truck Driving School
- Banderas Rental LLC
- beaumont school of trucking
- bestway truck & bus cdl driving school
- Big Daddi Trucking LLC
- Big Rig Truck Driving School
- Brigght life trucking school
- BSC Truck Driving School INC
- California Human Development Corporation - ASET Center
- CALIFORNIA TRUCK DRIVING SCHOOL
- CAMINO REAL CAREER SCHOOL
- CDL Basic Training, LLC
- Cdl instructor trucking LLC
- CDL TRANSPORT
- CENTRAL BUS & TRUCK SCHOOL / Central Bus & Truck Driving School
- Central Valley Trucking School
- Certified Safe Driver, Inc.
- Chayka Truck Driving LLC
- Chosen 2 Trucking School
- Coast to Coast Trucking School
- COMMERCIAL DRIVER'S ACADEMY, LLC
- Commercial Drivers License of California
- Commercial Transportation Services, Inc
- Commercial Trucking School
- Concrete Rose Correspondence School
- COURAGE CDL TRAINING
- Covenant Truck School
- CP TRUCKING
- CTDS Truck Driving School / Centro truck driving school
- Dashmesh Trucking School
- Dasmesh truck driving school
- Diamond Truck Driving School
- DM Truck Driving School
- DOABA TRUCK DRIVING SCHOOL INC
- Donna's Instruction Hub, LLC
- Double tap truck driving academy
- Drive Safe Trucking
- DTL Truck Driving School
- dynasty trucking school
- Easy Affordable Truck Academy
- Easy CDL Truck Driving School
- Economy Truck School
- el monte truck driving school
- ELDT Academy, LLC - Online & Travelling CDL Training
- ELDT Solutions
- ELITE EAGLE TRAINING LLC
- Empire Freight Group LLC
- Empire Truck Driving School
- Empowered Women Transportation Inc
- Fc CDL Inc.
- Felipe's Truck Driving School
- fifth wheel trucking
- Flex Trucking School LLC
- Flexible Truck Driving School
- FlyFreight CDL ACADEMY
- Freeway LLC
- Fremont Truck Driving School
- Fresno Truck Driving School, Inc.
- Fresno Truck Training
- GHOLIA TRUCK DRIVING SCHOOL LLC
- GO4CDL LLC
- Gobind truck driving school
- GOLDEN CDL RENTAL YUBA CITY
- Golden Frame Inc. dba National Truck Driving
- Golden Pacific Truck Driving School
- Golden Truck Driving School Inc.
- Gurmit truck academy inc
- Halpin Transportation LLC DBA Halpin Trucking School
- Hannas truck driving school
- Harbor Trucking School
- Harvest Training and Consulting
- Haryana Truck Driving School
- HB CDL Driving Academy
- High Desert Truck School, LLC
- HIGH IMPACT ACADEMY INC
- Hot Shots Driving Clinics - CA
- I-5 Trucking Academy LLC
- in Motion Trucking School
- indus truck school inc
- International truck driving school
- International truck school
- Jager Trucking School
- Junan Truck Driving School
- king truck school
- Local Driving School CDL
- Lopez & Lopez Trucking LLC
- Lopez Trucking
- Los Angeles Trucking College
- M&M logistic Trucking Inc
- Maatson Trucking School
- MAJOR EXPRESS TRUCK SCHOOL
- Mejor Express
- MERCURY TRUCK DRIVING SCHOOL LLC
- Mid Valley Truck School, LLC
- Mid-California Truck School
- MISSION TRUCK DRIVING SCHOOL, LLC
- MM Commercial Training Services
- Moga Truck School Inc.
- Multipurpose Driving School, LLC
- NASTRUCK CDL School, LLC
- NEW LEGEND TRUCK DRIVING SCHOOL
- New Look Truck Driving School Inc
- NorCal CDL Academy
- NS Truck Driving School INC
- Number 1 truck and car driving school llc
- NUMERO 1 TRUCKING
- On the move trucking school
- Pacific Truck Driving School Inc.
- Pacific Truck school
- Perfect Truck School Inc
- Performing Solutions
- PJ Trucking Academy
- premier trucking school
- PRIME TRUCK SCHOOL LLC
- Progress Trucking School
- R and C trucking
- Red Line Trucking School LLC
- Red Zone Trucking
- Right Lane Trucking School
- Saber Trucking School
- SAC TRUCK DRIVING SCHOOL INC
- SAFEWAY TRUCK DRIVING SCHOOL
- San Diego Truck Driving School
- San Joaquin Truck Driving School
- San Jose Trucking School
- School of Trucking
- Simmon's Trucking School Inc
- SKILLED CDL TRAINING
- SoCal Truck Driver Academy LLC.
- Socal Trucking School
- south bay truck driving school inc
- SPCDL Truck Driving School
- Stockton Truck Driving School LLC
- SUTTER POINT DRIVING SCHOOL INC
- TEOFT (Training & Employment Of Truckers)
- The Truck Master School
- Toro School of Truck Driving
- Train 4 Less
- Tresser's Trucking School / Able Transportation
- Tri Counties Truck Driving School
- Truck Driving Academy
- Truck Nation School
- Truckmaster CDL School LLC
- Twin Cities Equipment Rentals
- UNION TRUCK SCHOOL
- UNITED DRIVING SCHOOL INC
- US Truck Driving School
- VALLEY TRUCK DRIVING SCHOOL
- ventura county trucking academy llc
- VTS LLC
- WEST COAST TRUCK SCHOOL INC.
- West Coast Trucking School LLC
- Xpert Trucking School LLC
- YG TRUCK DRIVING SCHOOL INC
- YUBA SUTTER TRUCK DRIVING SCHOOL INC
- YUBA TRUCK DRIVING SCHOOL INC
- Zone 1 Trucking School

## Examples of use
- [Is your California career college or training program legit? Check its license or violations ](https://calmatters.org/data/2025/04/career-college-trade-school-training-program-database-lookup/)

## Data Use

While the contents of this repo are shared under an Apache 2.0 license, CalMatters/The Markup would appreciate any credit or attribution you're willing to give. We're also interested to learn how you used it, so feel free to [send us a message](<mailto:john@calmatters.org>) if you do. If you have any questions, feel free to [contact us](<mailto:john@calmatters.org>) as well.

CalMatters is a nonpartisan, nonprofit journalism venture committed to explaining how California’s state Capitol works and why it matters.

## License

Copyright 2026 CalMatters

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
