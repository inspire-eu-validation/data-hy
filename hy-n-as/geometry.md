# Geometry

**Version**: 1

**Purpose**: Verify geometric consistency, i.e. check that geometries are consistent with the geometries of other features in the data set.

**Prerequisites**

**Test method**

Automated assertions:

* If the HydroNode and the WatercourseLink feature types are contained in the same dataset, using a geometry library, verify for each [HydroNode](#HydroNode) that the [geometry](#geometry) (a gml:Point) is located a position that touches a [WatercourseLink.centrelineGeometry](#centrelineGeometry) (a gml:LineString or gml:Curve), i.e. that the node is at the start or end of a watercourse link. If the check fails report [freeNode](#freeNode).

    * Otherwise, if the HydroNode and the WatercourseLink feature types are not contained in the same dataset, a manual check is required to verify that for each [HydroNode](#HydroNode) the [geometry](#geometry) (a gml:Point) is located a position that touches a [WatercourseLink.centrelineGeometry](#centrelineGeometry) (a gml:LineString or gml:Curve), in this case report the message [freeNodeManualCheck](#freeNodeManualChcek).

Manual assertions:

* Verify that the level of detail is explicit in data sets covering multiple resolutions, i.e. if features are provided at different spatial resolutions, verify that the spatial resolution is specified for each of the features in the levelOfDetail attribute.
* Verify that watercourse links intersections are consistent with the real world, i.e. check that WatercourseLink features intersect wherever a connection exists between the real world phenomena they represent. No intersections must be created at crossing network elements when it is not possible for water to pass from one element to another.
* Verify that geometries are consistent with the reporting under the Water Framework Directive, i.e. review for each feature that the geometry is the same as the geometry used for reporting obligations under Directive 2000/60/EC.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Section 8.7.4 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Section 8.7.4 (2)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Section 8.7.4 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Section 8.7.4 (4)

**Test type**: Automated/Manual

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
freeNode <a name="freeNode"/>  |  XML document '$filename', HydroNode '$gmlid': The node is not located at the start or end of any WatercourseLink feature in the data set.
freeNodeManualCheck <a name="freeNodeManualCheck"/>  |  XML document '$filename', HydroNode '$gmlid': The relevant WatercourseLink feature is not available in the data set, manually verify that the HydroNode geometry (a gml:Point) is located at a position that touches a WatercourseLink.centrelineGeometry (a gml:LineString or gml:Curve), i.e. that the node is at the start or end of a watercourse link.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
HydroNode <a name="HydroNode"></a>   | //schema-element(hy-n:HydroNode) 
geometry <a name="geometry"></a>   | $HydroNode/*/gml:Point
WatercourseLink.centrelineGeometry <a name="centrelineGeometry"></a>   | //schema-element(hy-n:WatercourseLink)/hy-n:centrelineGeometry 
