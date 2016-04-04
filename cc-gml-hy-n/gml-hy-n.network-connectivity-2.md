# gml-hy-n.network-connectivity-2

**Version**: 0.1

**Purpose**: Verify that all hydrographic nodes are at the start or end of a watercourse link.

**Prerequisites**

* [gml-hy-n.basic-test](gml-hy-n.basic-test.md)

**Test method**

* For each [WatercourseLink](#WatercourseLink) verify that the only [HydroNodes](#HydroNodes) in the distance around the start or end of the [centerlineGeometry](#geometry) are the nodes associated via the [startNode](#start) and [endNode](#end) properties. Otherwise report [additionalNode](#additionalNode).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 8.7.7 (2)

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
additionalNode <a name="additionalNode"/>  |  XML document '$filename', WatercourseLink '$gmlid': HydroNode '$gmlidNode' is located within the connectivity tolerance of the start or end of the link geometry, but is not a start or end node of the link.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
WatercourseLink <a name="WatercourseLink"></a>   | //schema-element(hy-n:WatercourseLink)[net:startNode or net:endNode]
HydroNodes <a name="HydroNodes"></a>   | //schema-element(hy-n:HydroNode)
centerlineGeometry <a name="geometry"></a>   | $WatercourseLink/net:centerlineGeometry
startNode <a name="start"></a>   | $WatercourseLink/net:startNode
endNode <a name="end"></a>   | $WatercourseLink/net:endNode
