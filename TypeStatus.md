# Terms #

  * [typeStatus](http://rs.tdwg.org/dwc/terms/typeStatus)

# Recommendations #

## Core only ##

3 values in typeStatus, separated by "|" or "; "

  1. controlled vocabulary
  1. typified scientific name -> **any other field we can use** [originalNameUsage](http://rs.tdwg.org/dwc/terms/index.htm#originalNameUsage)?
  1. publication -> **any other field we can use?** [namePublishedIn](http://rs.tdwg.org/dwc/terms/index.htm#namePublishedIn)?

## Extension ##

Linked to a determination {JM: did we make this extension up or is it from a source? We want to keep to the core and it may be worth not including this?}

  * typeStatus = controlled vocabulary
  * typified scientific name = scientific name = basionym
  * publication = namePublishedIn

## Controlled vocabulary ##

**Create controlled vocabulary for types**

# Examples #

Give example for core only and extension

  1. known species name
  1. new species name = basionym => specimen becomes a holotype for that name
  1. new name combination (new genus) = new combination => specimen becomes a type for that name

  1. known species name
  1. holotype
  1. syntype