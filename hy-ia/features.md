# Feature references

**Version**: 1

**Purpose**: Verify that referenced features can be retrieved.

**Prerequisites**

**Test method**

* Verify that any feature reference in an association role is publicly accessible via HTTP, i.e. inspect all relevant properties. If a reference (@xlink:href) has a value that starts with "#", verify that an element with a `gml:id` attribute with the referenced identifier exists in the same document. If the reference starts with "http", verify that a HTTP GET request to the URI retrieves an XML document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following asscoiation roles:

* HydroObject.[relatedHydroObject](#relatedHydroObject) : HydroObject
* WatercourseSeparatedCrossing.[element](#element) : WatercourseLink
* WatercourseLink.[startNode](#startNode) : HydroNode
* WatercourseLink.[endNode](#endNode) : HydroNode
* SurfaceWater.[bank](#bank) : Shore
* SurfaceWater.[drainsBasin](#drainsBasin) : DrainageBasin
* SurfaceWater.[neighbour](#neighbour) : StandingWater
* DrainageBasin.[outlet](#outlet) : SurfaceWater

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-ia/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-ia/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
relatedHydroObject <a name="relatedHydroObject"></a> |  //schema-element(hy:HydroObject)/hy:relatedHydroObject/@xlink:href
element <a name="element"></a> |  //schema-element(hy-n:WatercourseSeparatedCrossing)/net:element/@xlink:href
startNode <a name="startNode"></a> |  //schema-element(hy-n:WatercourseLink)/net:startNode/@xlink:href
endNode <a name="endNode"></a> |  //schema-element(hy-n:WatercourseLink)/net:endNode/@xlink:href
bank <a name="bank"></a> |  //schema-element(hy-p:SurfaceWater)/hy-p:bank/@xlink:href
drainsBasin <a name="drainsBasin"></a> |  //schema-element(hy-p:SurfaceWater)/hy-p:drainsBasin/@xlink:href
neighbour <a name="neighbour"></a> |  //schema-element(hy-p:SurfaceWater)/hy-p:neighbour/@xlink:href
outlet <a name="outlet"></a> |  //schema-element(hy-p:DrainageBasin)/hy-p:outlet/@xlink:href
