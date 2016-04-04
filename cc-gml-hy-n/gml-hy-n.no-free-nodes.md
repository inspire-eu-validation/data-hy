# gml-hy-n.no-free-nodes

**Version**: 0.1

**Purpose**: Verify that all hydrographic nodes are at the start or end of a watercourse link.

**Prerequisites**

* [gml-hy-n.basic-test](gml-hy-n.basic-test.md)

**Test method**

* Verify for each [HydroNode](#HydroNode) that the [geometry](#geometry) (a gml:Point) is located a position that touches a [WatercourseLink.centerlineGeometry](#centerlineGeometry) (a gml:LineString or gml:Curve). Otherwise report [freeNode](#freeNode).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 8.7.4 (3)

**Test type**: Automated

**Notes**

This is not consistent with the Connectivity tolerance allowed in IR Annex II, Section 8.7.7 - except the tolerance is 0.

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
freeNode <a name="freeNode"/>  |  XML document '$filename', HydroNode '$gmlid': The node is not located at the start or end of any WatercourseLink feature in the data set.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
HydroNode <a name="HydroNode"></a>   | //schema-element(hy-n:HydroNode)
geometry <a name="geometry"></a>   | $HydroNode/hy-n:geometry/gml:Point
WatercourseLink.centerlineGeometry <a name="centerlineGeometry"></a>   | //schema-element(hy-n:WatercourseLink)/hy-n:centerlineGeometry