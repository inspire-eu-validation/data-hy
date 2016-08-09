# Units of measure

**Version**: 1

**Purpose**: Verify that measurements use an allowed unit.

**Prerequisites**

**Test method**

* Verify that all references to a [unit of measurement](#uom) use one of the approved HTTP URIs (note: currently no approved HTTP URIs exist for units) or values from the UCUM dictionary. Units of measurement must be SI units or, for angles, degrees, minutes and seconds.
* In this data theme the following properties have a unit:
  * [DrainageBasin.area](#area1), which must be an [area unit](#m2)
  * [Falls.length](#length1), which must be a [length unit](#m)
  * [StandingWater.elevation](#length2), which must be a [length unit](#m)
  * [StandingWater.meanDepth](#length3), which must be a [length unit](#m)
  * [StandingWater.surfaceArea](#area2), which must be an [area unit](#m2)
  * [Watercourse.length](#length4), which must be a [length unit](#m)
  * [Watercourse.width.lower](#length5), which must be a [length unit](#m)
  * [Watercourse.width.upper](#length6), which must be a [length unit](#m)
  * [WatercourseLink.length](#length7), which must be a [length unit](#m)
* If a unit of measurement is not one of the expected values, report [unknownUoM](#unknownUoM).

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-rs/README#ref_TG_DS_tmpl) IR requirement Article 12 (2)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
unknownUoM <a name="unknownUoM"/>  |  XML document '$filename', $featureType '$gmlid': A measurement value in property '$property' has an unexpected unit '$uom'. The allowed values are: $allowedUoM.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-rs/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
length unit <a name="m"></a>     | ('m', 'mm', 'cm', 'dm', 'km')
area unit <a name="m2"></a>     | ('m2', 'mm2', 'cm2', 'dm2', 'km2')
DrainageBasin.area <a name="area1"></a>   | //schema-element(hy-p:DrainageBasin)/hy-p:area/@uom
Falls.length <a name="length1"></a>   | //schema-element(hy-p:Falls)/hy-p:length/@uom
StandingWater.elevation <a name="length2"></a>   | //schema-element(hy-p:StandingWater)/hy-p:elevation/@uom
StandingWater.meanDepth <a name="length3"></a>   | //schema-element(hy-p:StandingWater)/hy-p:meanDepth/@uom
StandingWater.surfaceArea <a name="area2"></a>   | //schema-element(hy-p:StandingWater)/hy-p:surfaceArea/@uom
Watercourse.length <a name="length4"></a>   | //schema-element(hy-p:Watercourse)/hy-p:length/@uom
Watercourse.width.lower <a name="length5"></a>   | //schema-element(hy-p:Watercourse)/hy-p:width/*/hy-p:lower/@uom
Watercourse.width.upper <a name="length6"></a>   | //schema-element(hy-p:Watercourse)/hy-p:width/*/hy-p:upper/@uom
WatercourseLink.length <a name="length7"></a>   | //schema-element(hy-n:WatercourseLink)/hy-n:length/@uom
