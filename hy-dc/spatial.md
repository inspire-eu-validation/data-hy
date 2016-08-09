# Spatial consistency

**Version**: 1

**Purpose**: Verify that the spatial information is consistent.

**Prerequisites**

n/a

**Test method**

Verify that hydrographic networks are spatially connected across data sets.

Automated assertions:

* If the data set contains both [WatercourseLink](#WatercourseLink) and [SurfaceWater](#SurfaceWater) (Watercourse or StandingWater) features, use a geometry library to verify for each WatercourseLink that its [centerlineGeometry](#centerlineGeometry) is within the [geometry](#geometry) of a single Watercourse or StandingWater feature. Verify for each [HydroNode](#HydroNode) that its geometry is within a Watercourse or StandingWater feature, too. Otherwise report [notWithin](#notWithin).

Manual assertions:

* Review the data maintenance procedures and perform spot checks to verify that connectivity between hydrographic networks across state borders and – where applicable – also across regional borders (and data sets) within Member States is established and maintained by the respective authorities, using the cross-border connectivity mechanisms provided by the NetworkConnection type.

**Reference(s)**: 

* [TG DS-HY](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-dc/README#ref_TG_DS_HY) IR requirement Section 8.7.1 (1)
* [TG DS-HY](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-dc/README#ref_TG_DS_HY) IR requirement Section 8.7.1 (2)

**Test type**: Automated/Manual

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
notWithin <a name="notWithin"/>  |  XML document '$filename', $featureType '$gmlid': The geometry is not within a single SurfaceWater feature from the Physical Waters application schema.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-dc/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
WatercourseLink <a name="WatercourseLink"></a>   | //schema-element(hy-n:WatercourseLink)
SurfaceWater <a name="SurfaceWater"></a>   | //schema-element(hy-p:SurfaceWater)
HydroNode <a name="HydroNode"></a>   | //schema-element(hy-n:HydroNode)
centerlineGeometry <a name="centerlineGeometry"></a>   | $WatercourseLink/\*:centerlineGeometry
geometry <a name="geometry"></a>   | $SurfaceWater/\*:geometry