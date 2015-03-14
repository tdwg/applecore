# Terms #

  * [habitat](http://rs.tdwg.org/dwc/terms/habitat)

# Recommendations #

The habitat is the ecological or environmental area in which the specimen was collected and may be explicitly provided on the label.

If habitat is provided on the label, report this value. Habitat can be derived from the locality.

If habitat information is standardized in any form it is recommended to report habitat according to a published source and write that interpretation in square brackets.

  * verbatimLocality and habitat can overlap
  * preferred to use verbatim values, but controlled vocabulary can be used.

## Remarks ##

<font color='red'><code>[</code>DELETE? - remarks below probably not necessary, as folks could/may be placing (correctly?) habitat info into more than one DwC field<code>]</code> pws, jm</font>

If you do not have separate habitat field, put everything in occurrenceRemarks = remarks or notes about the specimen

  * occurrenceRemarks: specimen notes [remarks](specimen.md) square brackets. Also garbage field.
  * eventRemarks: it was a rainy day (very often in occurrenceRemarks)
  * locationRemarks: very often in occurrenceRemarks

# Examples #

|  | **Label Data** | [habitat](http://rs.tdwg.org/dwc/terms/habitat) | [verbatimLocality](http://rs.tdwg.org/dwc/terms/verbatimLocality) |
|:-|:---------------|:------------------------------------------------|:------------------------------------------------------------------|
| **1** | Habitat: roadside bordering secondary forest. | roadside bordering secondary forest |  |
| **2** | Borneo. Malaysia. Sabah. Ranau District. Mount Kinabalu National Park. Bukit Ular Trail, ca. 100 meters from northern terminus. Large tree growing on edge of trail in primary montane forest. | primary montane forest | Mount Kinabalu National Park. Bukit Ular Trail, ca. 100 meters from northern terminus. Large tree growing on edge of trail |
| **3** | USA. Connecticut. New Haven. West Rock Ridge State Park. Growing in thin soil on edges of exposed outcrop. Eastern redcedar / Poverty grass (Juniperus virginiana / Danthonia spicata) community.” | Growing in thin soil on edges of exposed outcrop. Eastern redcedar / Poverty grass (Juniperus virginiana / Danthonia spicata) community. | New Haven. West Rock Ridge State Park. Growing in thin soil on edges of exposed outcrop. |
| **4** | USA. Connecticut. Hamden. West Rock Ridge State Park. Seepage dominated by Red Maple, Green Ash, and Northern Spicebush - Skunk-cabbage and Cinnamon fern dominate the herbaceous layer. | Seepage dominated by Red Maple, Green Ash, and Northern Spicebush - Skunk-cabbage and Cinnamon fern dominate the herbaceous layer. | Hamden. West Rock Ridge State Park. |
| **5** | USA. Connecticut. Hamden. West Rock Ridge State Park. Seepage dominated by Red Maple, Green Ash, and Northern Spicebush - Skunk-cabbage and Cinnamon fern dominate the herbaceous layer. | Seepage dominated by Red Maple, Green Ash, and Northern Spicebush - Skunk-cabbage and Cinnamon fern dominate the herbaceous layer. `[`Red maple / Northern spicebush (Acer rubrum / Lindera benzoin) community (Metzler and Barrett 2006, The Vegetation of Connecticut)`]` | Hamden. West Rock Ridge State Park. |
| **6** | USA. Connecticut. Hamden. West Rock Ridge State Park. Seepage dominated by Red Maple, Green Ash, and Northern Spicebush - Skunk-cabbage and Cinnamon fern dominate the herbaceous layer. | Seepage dominated by Red Maple, Green Ash, and Northern Spicebush - Skunk-cabbage and Cinnamon fern dominate the herbaceous layer. `[`North-Central Appalachian Acidic Swamp - CES202.604 (NatureServe)`]` | Hamden. West Rock Ridge State Park. |