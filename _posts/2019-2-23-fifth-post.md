---
layout: article
title: "Eviction and Code Violations"
category: ilpr
link: https://public.tableau.com/views/NearWestSideLicenses-/ExisitingNWSLicenses-?:embed=y&:display_count=yes
text: Go to Viz
share: False
image:
  feature:
  teaser: eviction_violations_90.png

---
<iframe src="https://public.tableau.com/shared/DQWR8N63F?:showVizHome=no&:embed=true&:display_count=yes" allowfullscreen="true" width="1015" height="835"></iframe>


## About Evictions and Code Violations

Landlords have an obligation to keep properties up to code and are prohibited from evicting a tenant for reporting building code violations. This interactive tool allows a user to identify evictions filed within 90 days of a building code violation and parcels with open orders upon eviction filing. At this point, data is not regularly updated like other visualizations on this site. Data was last updated in December 2018.

#### Map Filter and Selection

<dl> This visualization allows a user to apply a variety of filters to refine the map. Each filter automatically updates the count of evictions filed in the upper right corner. Violation categories filter based on whether a DNS violation contained at least one offense in the selected category. When multiple violation filters are selected, the DNS order that occurred within 90 days before the eviction filing contains each violation type.</dl>

<dt> <strong>Sanitary Conditions: </strong> DNS violations issued under subchapter 275-81: Sanitary Conditions.</dt>

<dt> <strong>Electrical Facilities: </strong> DNS violations issued under  subchapter 275-62: Electrical Facilities.</dt>

<dt> <strong>Interior Structure: </strong> DNS violations issued under subchapter 275-33: Interior Structure.</dt>

<dt> <strong>Plumbing: </strong> DNS violations issued under subchapter 275-53: Plumbing and Plumbing fixtures.</dt>

<dt> <strong>Heat Issues: </strong> DNS violations issued under subchapter 275-61: Heating Facilities.</dt>

<dt> <strong>Heat Restoration: </strong> ordinance 275-61 -repair or replace defective heating system. restore heating system to a safe and operable condition capable of adequately heating all habitable rooms, bathrooms and toilet rooms to a temperature of at least 67 degrees Fahrenheit continuously during periods of occupancy.</dt>

<dt> <strong>Pests: </strong> DNS ordinances related to pests, rodents, bed bugs, and roaches.</dt>

<dt> <strong>Bed Bugs: </strong> DNS ordinances related to bed bug.</dt>

<dt> <strong>Open DNS Violations When Eviction is Filed: </strong> DNS order is still unresolved at the time of eviction filing.</dt>

<dt> <strong>Evt 60 days: </strong>DNS order occurred within 60 days before the eviction filing .</dt>

<dt> <strong>Evt 30 days: </strong> DNS order occurred within 30 days before the eviction filing.</dt>


#### Map Tooltip Definitions

<dt>All metrics are calculated at the parcel level and link on Taxkey. Each violation order ID and proximate eviction is provided in the tooltip. Large multi-families evict at a higher rate relative to single and two family homes. </dt>

<dl>
  <dt> <strong> Proximate Eviction: </strong> The distance in days between when a DNS order is issued and eviction is filed.</dt>
    
  <dt> <strong>Lead Plaintiff : </strong> Lead plaintiff  is the first name in an eviction filing. The owner of a property is not always who is listed as the lead plaintiff  in an eviction filing. Commonly filed evictions taken the most frequent lead plaintiff  from the previous year.</dt>
    
  <dt> <strong>Primary Land Use: </strong> The City of Milwaukee's Master Property File maintains the primary land use for each parcel. Example categories include single or two family.</dt>
    
  <dt> <strong>Number of Units: </strong> Number of units listed for each parcel.</dt>
    
  <dt> <strong>Taxkey: </strong> Taxkey is a unique ten-digit number assigned to each City of Milwaukee parcel.</dt>

  </dl>
  
#### Data Sources

 <strong>Master Property File </strong> 

Information on current land use and listed property owners retrieved from the City of Milwaukee's Master Property File (MPROP). MPROP as it is commonly called, is a table containing a record for each property in the city. It contains more than 90 elements of data describing each of the approximately 160,000 properties in the city. More information can be found [here.](https://data.milwaukee.gov/dataset/mprop)

 <strong> Eviction Records </strong> 

Eviction data is pulled from the WCCA REST Interface — programmatic access to Wisconsin Circuit Court records. Small claims cases in Milwaukee County with a case type of small claims eviction are pulled down and stored on a weekly basis. CCAP provides no warranties as to the accuracy or timeliness of the information contained in the WCCA Data.

 <strong> DNS Code Violations  </strong> 


Data is provided via an API that allows a user to regularly pull code violations and service request complaints from DNS record management system accela.

---

##### Categorizing Code Violations

<dt> Code violations against a property can range from external violation relating to upkeep of a lawn and more serious violations affecting the habitability of a home such as heat not functioning. In the data available there are over 912 different state statutes and ordinances listed. To provide overall categories of ordinance/statutes, the violation subchapter categories were extracted. For example, Milwaukee ordinance 275-82.1 is related to bed bugs. This is reworked to get the subchapter "275-82" named Extermination. This method categorized 95% of ordinances/statutes with 62 sub chapters.

</dt>

##### How An Eviction Filing is is Matched to a Parcel

<dt> Defendant address is selected to represent an eviction location. Where multiple addresses exist with a single case, the earliest Milwaukee address in the case is given preference. The court record of events is reviewed to check if any address change took place during the case. If a change is present, the original listed address is parsed from the text and selected. 
The address information is then cleaned and separated into appropriate columns. Data is filtered to only include records that fell into the City of Milwaukee. We preprocessed the data to improve MAI/DIME match accuracy. This includes steps around converting street to st and removing apt or unit numbers from the address data. Addresses were then validated using the City of Milwaukee's MAI/DIME address locator.</dt>


<dl>
<dt> ProPublica’s searchable mapping tool exploring eviction against rent stabilized units influenced our decision to move pass only identifying where an eviction took place. We linked eviction addresses to a City of Milwaukee parcel using an addresse's Taxkey. Taxkey is a unique ten-digit number assigned to each parcel. This allows us to merge additional information around property, ownership, unit size, and building code violations maintained by the City of Milwaukee. Overall, this process produces a 94.8% parcel match rate. This can be benchmarked to Eviction Lab's 93% geocoding match rate — which includes street center line and census tract geocoding. </dt> </dl>
