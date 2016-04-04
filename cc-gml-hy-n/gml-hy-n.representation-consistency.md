# gml-hy-n.representation-consistency

**Version**: 0.1

**Purpose**: Verify that the network and physical waters representations are consistent, if both a part of the data set.

**Prerequisites**

* [gml-hy-n.basic-test](gml-hy-n.basic-test.md)

**Test method**

* If the data set contains both [WatercourseLink](#WatercourseLink) and [SurfaceWater](#SurfaceWater) (Watercourse or StandingWater) features, verify for each WatercourseLink that its [centerlineGeometry](#centerlineGeometry) is within the [geometry](#geometry) of a single Watercourse or StandingWater feature. Verify for each [HydroNode](#HydroNode) that its geometry is within a Watercourse or StandingWater feature, too. Otherwise report [notWithin1](#notWithin1) or [notWithin2](#notWithin2).

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 8.7.1 (1)

**Test type**: Automated

**Notes**

This could be part of either one of the two conformance classes (Network or Physical Waters).

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
notWithin1 <a name="notWithin1"/>  |  XML document '$filename', WatercourseLink '$gmlid': The geometry is not within a single SurfaceWater feature from the Physical Waters application schema.
notWithin2 <a name="notWithin2"/>  |  XML document '$filename', HydroNode '$gmlid': The geometry is not within a single SurfaceWater feature from the Physical Waters application schema.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
WatercourseLink <a name="WatercourseLink"></a>   | //schema-element(hy-n:WatercourseLink)
SurfaceWater <a name="SurfaceWater"></a>   | //schema-element(hy-p:SurfaceWater)
HydroNode <a name="HydroNode"></a>   | //schema-element(hy-n:HydroNode)
centerlineGeometry <a name="centerlineGeometry"></a>   | $WatercourseLink/net:centerlineGeometry
geometry <a name="geometry"></a>   | $SurfaceWater/hy-p:geometry
