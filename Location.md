# Terms #

  * [higherGeographyID](http://rs.tdwg.org/dwc/terms/higherGeographyID)
  * [higherGeography](http://rs.tdwg.org/dwc/terms/higherGeography)
  * [continent](http://rs.tdwg.org/dwc/terms/continent)
  * [islandGroup](http://rs.tdwg.org/dwc/terms/islandGroup)
  * [island](http://rs.tdwg.org/dwc/terms/island)
  * [country](http://rs.tdwg.org/dwc/terms/country)
  * [countryCode](http://rs.tdwg.org/dwc/terms/countryCode)
  * [stateProvince](http://rs.tdwg.org/dwc/terms/stateProvince)
  * [county](http://rs.tdwg.org/dwc/terms/county)
  * [municipality](http://rs.tdwg.org/dwc/terms/municipality)
  * [locality](http://rs.tdwg.org/dwc/terms/locality)
  * [verbatimLocality](http://rs.tdwg.org/dwc/terms/verbatimLocality)

# Recommendations #

## Verbatim locality ##

  * Not edited
  * Not concatenated with other controlled higher geography fields
  * Can include higher geography if part of the locality field

## Locality ##

  * No higher geography
  * Can be standardized: Montréal, 3km North of

## higherGeography ##

  * If you do not want to parse your locality field
  * If you have verbatim higher geography
  * If you have non-translated higher geography
  * If you have more levels than DwC provides

## Continent ##

  1. Use this controlled vocabulary: **link**

## Country and country codes ##

  1. Use this controlled vocabulary: **link** (English)
  1. Country codes
  1. Use your internal controlled vocabulary (own language)
  1. Use verbatim

## State/Province, County, Municipality ##

  1. Use this controlled vocabulary: **link** (English)
  1. Use your internal controlled vocabulary (own language)
  1. Use verbatim

# Examples #

| Example | verbatimLocality | locality | country | stateProvince |
|:--------|:-----------------|:---------|:--------|:--------------|
| Country=Canada|Prov=QC|Location=3km N. of Montréal | 3km N. of Montréal | 3km N. of Montréal | Canada | QC |
| Canada, QC, 3km N. of Montréal | Canada, QC, 3km N. of Montréal | 3km N. of Montréal | Canada | QC |
| 3km N. of Montréal | 3km N. of Montréal | 3km N. of Montréal | ? | ? |
| Montreal, 3km North of (edited)  |  | Montreal, 3km North of |  |  |
| Canada; QC; Montreal, 3km North of (edited) |  | Montreal, 3km North of | Canada | QC |