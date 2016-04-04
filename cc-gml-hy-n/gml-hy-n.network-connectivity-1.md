# gml-hy-n.network-connectivity-1

**Version**: 0.1

**Purpose**: Verify that all hydrographic nodes are at the start or end of a watercourse link.

**Prerequisites**

* [gml-hy-n.basic-test](gml-hy-n.basic-test.md)

**Test method**

* For each [WatercourseLink](#WatercourseLink) with a startNode or endNode property, verify that the distance between the start or end of the [centerlineGeometry](#geometry) and the geometry of the [start](#start) and [end](#end) HydroNode is smaller than the [connectivityTolerance](#tolerance). Otherwise report [noConnectionStart](#noConnectionStart) or [noConnectionEnd](#noConnectionEnd).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 8.7.7 (1)

**Test type**: Automated

**Notes**

Geometries typically will need to be converted into a meter-based CRS, eg ETRS89 LAEA or LCC. 

It is unclear how to handle geometries outside of continental Europe. Classify as MANUAL?

## Parameters

Identifier  |  Description
---------------------------------------------------------- | -------------------------------------------------------------------------
connectivityTolerance <a name="tolerance"/>  |  a number, the tolerance in meter

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
noConnectionStart <a name="noConnectionStart"/>  |  XML document '$filename', WatercourseLink '$gmlid': The HydroNode '$gmlidNode' at the start of the link (coordinates: '$coordNode') is spatially not located at the start of the link (coordinates: '$coordStart').
noConnectionEnd <a name="noConnectionEnd"/>  |  XML document '$filename', WatercourseLink '$gmlid': The HydroNode '$gmlidNode' at the end of the link (coordinates: '$coordNode') is spatially not located at the end of the link (coordinates: '$coordStart').

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
WatercourseLink <a name="WatercourseLink"></a>   | //schema-element(hy-n:WatercourseLink)[net:startNode or net:endNode]
centerlineGeometry <a name="geometry"></a>   | $WatercourseLink/net:centerlineGeometry
start <a name="start"></a>   | $WatercourseLink/net:startNode/hy-n:HydroNode/net:geometry
end <a name="end"></a>   | $WatercourseLink/net:endNode/hy-n:HydroNode/net:geometry
