# Terms #

  * [verbatimEventDate](http://rs.tdwg.org/dwc/terms/verbatimEventDate)
  * [eventDate](http://rs.tdwg.org/dwc/terms/eventDate)
  * [eventTime](http://rs.tdwg.org/dwc/terms/eventTime)
  * [startDayOfYear](http://rs.tdwg.org/dwc/terms/startDayOfYear)
  * [endDayOfYear](http://rs.tdwg.org/dwc/terms/endDayOfYear)
  * [year](http://rs.tdwg.org/dwc/terms/year)
  * [month](http://rs.tdwg.org/dwc/terms/month)
  * [day](http://rs.tdwg.org/dwc/terms/day)

# Recommendations #

The **collection date** is the date, date range or dates on which a specimen was collected, and is typically written on the specimen label.

## Verbatim date ##

The verbatim date is the collection date as written on the specimen label (see the definition for [verbatim](http://code.google.com/p/applecore/wiki/Glossary#Verbatim)) and is recorded in a single free-text field.

It is recommended to have a verbatim date field in your database, as it is the most objective way to record the collection date and in some cases the only way to do so. You can either always populate this field or only when the [formatted date](http://code.google.com/p/applecore/wiki/CollectionDate#Formatted_date) cannot unambiguously represent the collection date (see [examples](http://code.google.com/p/applecore/wiki/CollectionDate#Examples)).

Publish the verbatim date in **_[verbatimEventDate](http://rs.tdwg.org/dwc/terms/verbatimEventDate)_**. Remarks or notes regarding the collection date are accepted in this term as long as the verbatim date is included as well: "3/5/2009 (probably March)" or if the date is illegible: "illisible". If a database contains verbatim and non-verbatim dates in one field or if it is unknown whether the field corresponds to the verbatim date, it should _not_ be considered a _verbatimEventDate_ and should be shared in _[eventDate](http://rs.tdwg.org/dwc/terms/eventDate)_ instead (see [example 8](http://code.google.com/p/applecore/wiki/CollectionDate#Examples)). Transform those non-verbatim dates to ISO 8601 if possible (see [below](http://code.google.com/p/applecore/wiki/CollectionDate#Formatted_date)).

## Formatted date ##

As the verbatim date doesn't readily allows calculation and sorting, most collections (also) record the collection date in a structured format. This can be done in numerous ways:

  * Date = 1980 Jul 8-15
  * Date = 7/8-15/1980
  * Date = 8-15/7/1980
  * Date = 8-15.07.80
  * Date = 8-15 VII 1980
  * Date = 1980-07-08/15 (recommended)
  * Date = 1980-07-08/1980-07-15 (recommended)
  * Start date = 1980 Jul 8 | End date = 1980 Jul 15
  * Day = 8-15 | Month = 7 | Year = 1980
  * Start day = 8 | Start month = 7 | Start year = 1980 | End day = 15 | End month = 7 | End year = 1980

It is recommended to store any formatted date using the **[ISO 8601:2004(E)](http://en.wikipedia.org/wiki/ISO_8601)** standard. In ISO 8601 date and time values are organized from the most to the least significant and with a fixed number of digits per value: YYYY-MM-DD. Date ranges are expressed with a forward slash: YYYY-MM-DD/YYYY-MM-DD, YYYY-MM-DD/MM-DD or YYYY-MM-DD/DD. Partial dates can only be expressed by dropping the least significant values first: YYYY-MM or YYYY, but never MM-DD.  For more information and examples, see [Wikipedia](http://en.wikipedia.org/wiki/ISO_8601) and the [Darwin Core wiki](http://code.google.com/p/darwincore/wiki/Event).

If it is necessary to record the collection date in multiple fields (start/end date or day/month/year), try to store the date in a format close to ISO 8601, so it can easily be transformed by concatenation.

Publish the formatted collection date in **_[eventDate](http://rs.tdwg.org/dwc/terms/eventDate)_**. It is **highly recommended to use the [ISO 8601:2004(E)](http://en.wikipedia.org/wiki/ISO_8601) standard**, as it allows the date information to be shared unambiguously. Other date formats should only be used if the collection is unable to record or transform the dates to ISO 8601.

Although date ranges can be expressed in _eventDate_ (with "/"), multiple dates cannot (see [example 7](http://code.google.com/p/applecore/wiki/CollectionDate#Example)).

## Other date terms ##

In addition to _eventDate_, Darwin Core offers several other date terms which allow (part of) the collection date to be published in a more readily useable format (see [examples](http://code.google.com/p/applecore/wiki/CollectionDate#Examples)). Provide values for this terms if feasible.

Some guidelines:
  * [eventTime](http://rs.tdwg.org/dwc/terms/eventTime): Useful if the time is recorded, but not the date (otherwise _[eventDate](http://rs.tdwg.org/dwc/terms/eventDate)_ can be used as well). Rare for herbarium specimens.
  * [startDayOfYear](http://rs.tdwg.org/dwc/terms/startDayOfYear): If the (leap)year is unknown, do not use for dates after February 28.
  * [endDayOfYear](http://rs.tdwg.org/dwc/terms/endDayOfYear): For single dates, provide the same value as in _startDayOfYear_.
  * [year](http://rs.tdwg.org/dwc/terms/year): 4 digits. Do not use for ranges spanning two different years.
  * [month](http://rs.tdwg.org/dwc/terms/month): Do not use leading zeros. Do not use for ranges spanning two different months.
  * [day](http://rs.tdwg.org/dwc/terms/day): Do not use leading zeros. Do not use for ranges.

# Examples #

## Ideal situation ##

The following examples show the most ideal situation: the [verbatim date](http://code.google.com/p/applecore/wiki/CollectionDate#Verbatim_date) is known, the eventDate is strictly expressed in the ISO 8601 standard and [other date terms](http://code.google.com/p/applecore/wiki/CollectionDate#Other_date_terms) can be populated automatically.

|  | [verbatimEventDate](http://rs.tdwg.org/dwc/terms/verbatimEventDate) | [eventDate](http://rs.tdwg.org/dwc/terms/eventDate) | [eventTime](http://rs.tdwg.org/dwc/terms/eventTime) | [startDayOfYear](http://rs.tdwg.org/dwc/terms/startDayOfYear) | [endDayOfYear](http://rs.tdwg.org/dwc/terms/endDayOfYear) | [year](http://rs.tdwg.org/dwc/terms/year) | [month](http://rs.tdwg.org/dwc/terms/month) | [day](http://rs.tdwg.org/dwc/terms/day) |
|:-|:--------------------------------------------------------------------|:----------------------------------------------------|:----------------------------------------------------|:--------------------------------------------------------------|:----------------------------------------------------------|:------------------------------------------|:--------------------------------------------|:----------------------------------------|
| **1** | 1 juillet 1991 | 1991-07-01 |  | 182 | 182 | 1991 | 7 | 1 |
| **2** |  | 1991-07-01 |  | 182 | 182 | 1991 | 7 | 1 |
| **3** | 3/1/2004 | 2004 |  |  |  | 2004 |  |  |
| **4** | Early spring 1999 | 1999 |  |  |  | 1999 |  |  |
| **5** | March 12 |  |  |  |  |  | 3 | 12 |
| **6** | July 24-25, 1947 | 1947-07-24/1947-07-25 |  | 205 | 206 | 1947 | 7 |  |
| **7** | May 16 and August 7, 1991 |  |  |  |  | 1991 |  |  |

  * Example 2: The collection does not record a verbatim date if the collection date can be unambiguously expressed in a formatted date.
  * Example 3: If additional information is available regarding the month (January or March), the terms can be populated as in example 1.
  * Example 5: Partial dates can only be expressed from the least to the most significant in _eventDate_. In this case the most significant (year) is missing.
  * Example 6: The _eventDate_ may also be written as 1947-07-24/25.
  * Example 7: Some herbarium specimens have multiple dates (e.g. one for the flower and one for the plant). Multiple dates cannot be expressed in _eventDate_.

## Least ideal situation ##

The following example shows the least ideal situation: the [verbatim date](http://code.google.com/p/applecore/wiki/CollectionDate#Verbatim_date) is unknown, the [formatted date](http://code.google.com/p/applecore/wiki/CollectionDate#Formatted_date) is not recorded as ISO 8601 and it is not feasible for the collection to transform the formatted date to ISO 8601 for some of its records.

|  | [verbatimEventDate](http://rs.tdwg.org/dwc/terms/verbatimEventDate) | [eventDate](http://rs.tdwg.org/dwc/terms/eventDate) | [eventTime](http://rs.tdwg.org/dwc/terms/eventTime) | [startDayOfYear](http://rs.tdwg.org/dwc/terms/startDayOfYear) | [endDayOfYear](http://rs.tdwg.org/dwc/terms/endDayOfYear) | [year](http://rs.tdwg.org/dwc/terms/year) | [month](http://rs.tdwg.org/dwc/terms/month) | [day](http://rs.tdwg.org/dwc/terms/day) |
|:-|:--------------------------------------------------------------------|:----------------------------------------------------|:----------------------------------------------------|:--------------------------------------------------------------|:----------------------------------------------------------|:------------------------------------------|:--------------------------------------------|:----------------------------------------|
| **8** |  | 01 Aug 1991 |  |  |  |  |  |  |