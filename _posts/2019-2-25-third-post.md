---
layout: article
title: "Track Milwaukee Evictions"
category: sda
link: https://public.tableau.com/views/NearWestSideLicenses-/ExisitingNWSLicenses-?:embed=y&:display_count=yes
text: Go to Viz
share: False
image:
  feature:
  teaser: eviction_parcel.png

---


<iframe src="https://public.tableau.com/views/TrackingMilwaukeeEvictions/TrackMilwaukeeEvictionFilings?:showVizHome=no&:embed=true&:display_count=yes" allowfullscreen="true" width="1015" height="835"></iframe>


## About Track Milwaukee Evictions

This map displays eviction filings at the parcel level. For a visual depiction on the difference between a parcel, unit, or address click [here](https://datasmart.ash.harvard.edu/sites/default/files/styles/max_650x650/public/2019-04/Kat%20Hartman%20address_visual%20%281%29_0.png?itok=jzKJhM02) or read a more detailed description [here.](https://datasmart.ash.harvard.edu/news/article/meet-designer-who-leading-data-innovation-detroit-one-story-time) Each point on the map is scaled according to the total number of evictions filed since 2016. The larger the circle the more evictions were filed at a given parcel.

---

#### Map Filter and Selection

<dl> This visualization allows a user to apply a variety of filters to refine the map. Each filter with the exception of evicting filing rate and total evictions filed will automatically update the count of evictions filed in the upper right corner. Icons can be used to toggle each filter card on and off. Apply a filter to more quickly zoom and explore evictions at a parcel level.</dl>

<dl>    
    <dt> <strong>3 Year Eviction Filing Rate: </strong> apply this filter to view a selecterange of parcels with a 3 year eviction filing rate i.e. 100%.</dt>
    
    <dt> <strong>Eviction Filings: </strong> filter parcels by the number of evictions filed at a given property.</dt>
    
    <dt> <strong>Eviction Year: </strong> only view eviction filings by a given year.</dt>
    
    <dt> <strong>Eviction Month: </strong> view eviction filings by a given month.</dt>
    
    <dt> <strong>Landowner: </strong> search by current owner. Deselect all, search for a given plantiff name, and click apply.</dt>
    
    <dt> <strong>Lead Plantiff: </strong> search by the lead plantiff in each court record. Deselect all, search for a given plantiff name, and click apply.</dt>
    
    <dt> <strong>1-2 Family: </strong> filter map to include properties whose land use is single or two family residential.</dt>
    
    <dt> <strong>Multi-Family: </strong> filter map to include properties whose land use is multi-family.</dt>
    
    <dt> <strong>Unit Size: </strong> select properties based on unit size category.</dt>
    
    <dt> <strong>Alderperson: </strong> select evictions within a given aldermanic district. Alderperson names are derived from the most recent City of Milwaukee aldermanic shapefiles.</dt>
    
    <dt> <strong>Zip Code: </strong> select evictions within a Milwaukee Zip Code boundary.</dt>
    
    <dt> <strong>Police District: </strong> select evictions within a Milwaukee Police District boundary.</dt>    


</dl>

#### Map Tooltip Definitions

<dt>All Metrics Are Calculated at the Parcel Level. </dt>

<dl>
  <dt> <strong> Eviction filing: </strong> represents a court action typically filed by a landlord or property manager to begin eviction proceedings.</dt>
    
  <dt> <strong>Eviction Judgement: </strong> represents a court granting the plantiff a judgement for eviction.</dt>
  
  <dt> <strong>Eviction Filing Rate: </strong> represents the number of evictions filed per year divided by the number of units at the parcel. Rates are calculated at 1 and 3 year intervals. A parcel can have an eviction filing rate over 100% in a given year. This can be due to month-to-month tenancy or multiple evictions against the same tenant.</dt>
  
  <dt> <strong>Current Owner: </strong> ownership is taken from the City of Milwaukee's Master Property File record and is updated monthly.</dt>
  
  <dt> <strong>Lead Plantiff: </strong> Lead plantiff is the first name in an eviction filing. The owner of a property is not always who is listed as the lead plantiff in an eviction filing. Commonly filed evictions taken the most frequent lead plantiff from the previous year.</dt>
    
  <dt> <strong>Primary Land Use: </strong> The City of Milwaukee's Master Property File maintains the primary land use for each parcel. Example categories include single or two family.</dt>
    
  <dt> <strong>Current Owner: </strong> ownership is taken from the City of Milwaukee's Master Property File record and is updated monthly.</dt>
    
  <dt> <strong>Number of Units: </strong> Number of units listed for each parcel.</dt>
    
  <dt> <strong>Taxkey: </strong> Taxkey is a unique ten-digit number assigned to each City of Milwaukee parcel.</dt>
    
  <dt> <strong>Defense Attorney: </strong> Counts the total number cases at a given parcel where a defense attorney entered their name and bar number in a court record. This measure will underrepresent any form of representation as same day representation rarely enters attorney information. </dt>
    
  <dt> <strong>Plantiff Attorney: </strong> Counts the percentage of overall cases at a given parcel where a plantiff's attorney entered their name and bar number in a court record. </dt>
    
  <dt> <strong>Average Total Judgement: </strong> Calculates the average total monetary judgement awarded by the court of all cases at a given parcel. </dt>
    
  <dt> <strong> Percent Default Judgement: </strong> Calculates the percentage of cases at a given parcel when the last judgement issued is a default judgemnt. Default judgements are granted when a party does not file a response or attend court.</dt>
  
   <dt> <strong>Plantiff Attorney: </strong> Counts the percentage of overall cases at a given parcel where a plantiff's attorney entered their name and bar number in a court record. </dt>
    
</dl>


#### Data Sources

**Master Property File**

Information on current land use and listed property owners retrieved from the City of Milwaukee's Master Property File (MPROP). MPROP as it is commonly called, is a table containing a record for each property in the city. It contains more than 90 elements of data describing each of the approximately 160,000 properties in the city. More information can be found [here.](https://data.milwaukee.gov/dataset/mprop)

**Eviction Records**

Eviction data is pulled from the WCCA REST Interface — programtic access to Wisconsin Circuit Court records. Small claims cases in Milwaukee County with a case type of small claims eviction are pulled down and stored on a weekly basis. CCAP provides no warranties as to the accuracy or timeliness of the information contained in the WCCA Data.

---

##### How An Eviction Filing is is Matched to a Parcel

<dt> Defendant address is selected to represent an eviction location. Where multiple addresses exist with a single case, the earliest Milwaukee address in the case is given preference. The court record of events is reviewed to check if any address change took place during the case. If a change is present, the original listed address is parsed from the text and selected. 
The address information is then cleaned and separated into appropriate columns. Data is filtered to only include records that fell into the City of Milwaukee. We prepossessed the data to improve MAI/DIME match accuracy. This includes steps around converting street to st and removing apt or unit numbers from the address data. Addresses were then validated using the City of Milwaukee's MAI/DIME address locator.</dt>


<dl>
<dt> ProPublica’s searchable mapping tool exploring eviction against rent stabilized units influenced our decision to move pass only identifying where an eviction took place. We linked eviction addresses to a City of Milwaukee parcel using an addresse's Taxkey. Taxkey is a unique ten-digit number assigned to each parcel. This allows us to merge additional information around property, ownership, unit size, and building code violations maintained by the City of Milwaukee. Overall, this process produces a 94.8% parcel match rate. This can be benchmarked to Eviction Lab's 93% geocoding match rate — which includes street center line and census tract geocoding. </dt> </dl>
