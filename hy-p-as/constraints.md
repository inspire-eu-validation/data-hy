# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation). 

For constraints that require retrieving a referenced resource and the resource cannot be retrieved, report [brokenLink](#brokenLink). The test accepts the following two types of content in @xlink:href attributes: Either a "#" followed by a @gml:id in the same document or a HTTP URI.

Automated tests:

* A river basin may not be contained in any other basin; OCL: "inv: self.containsBasin->forall(c | not c.oclIsTypeOf(RiverBasin))". Verify that all resources referenced in [containsBasin](#containsBasin) are not a schema-element(hy-p:RiverBasin).
* A standing water geometry may be a surface or point; OCL: "inv: self.geometry.oclIsTypeOf(GM_Surface) or self.geometry.oclIsTypeOf(GM_Point)". Verify that [StandingWater.geometry](#geometry1) is a gml:Surface, gml:Polygon or gml:Point. 
* Watercourse geometry may be a curve or surface; OCL: "inv: self.geometry.oclIsTypeOf(GM_Curve) or self.geometry.oclIsTypeOf(GM_Surface)". Verify that [Watercourse.geometry](#geometry2) is a gml:Surface, gml:Polygon, gml:Curve or gml:LineString.
* A condition attribute may be specified only for a man-made watercourse; OCL: "inv: (self->count(condition)=1) implies (self.origin=OriginType::manMade)". Verify that [condition](#condition) is only set, if the origin is "manMade".

Manual tests:

* The shores on either side of a watercourse shall be provided (using the bank property) as two separate Shore objects. Inspect the data set for the Shore objects for each Watercourse and verify that, if they exist, they are referenced from the Watercourse.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-HY](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_HY)) 5.4

**Test type**: Automated/Manual

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-p-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
containsBasin <a name="containsBasin"></a> |  //schema-element(hy-p:DrainageBasin)/hy-p:containsBasin/@xlink:href
StandingWater.geometry <a name="geometry1"></a> |  //schema-element(hy-p:StandingWater)/hy-p:geometry/*
Watercourse.geometry <a name="geometry2"></a> |  //schema-element(hy-p:Watercourse)/hy-p:geometry/*
condition <a name="condition"></a> |  //schema-element(hy-p:Watercourse)/hy-p:condition
