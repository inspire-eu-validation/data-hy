# simple-features

**Version**: 0.1

**Purpose**: Verify that the features are Simple Features, i.e. their geometries meet the requirements of the Simple Features standard. 

**Prerequisites**

n/a

**Test method**

Check whether all spatial properties only use 0, 1 and 2-dimensional geometric objects that exist in the right 1-, 2- or 3-dimensional coordinate space, and where all interpolations respect the rules specified in the reference documents.

* Verify that no spatial topology types are used, i.e. check that none of the GML object elements for spatial [topology](#topology) are used as child elements of a feature from the application schema. For unmet constraints report spatialTopologyTypeFound.
* Verify that only linear interpolation is used, i.e. check that none of the [nonlinear](#nonlinear) GML curve segment object elements are used as child elements of a feature from the application schema. For unmet constraints report invalidInterpolationFound.
* Verify that only gml:Polygon or gml:Surface are used, i.e. check that none of the disallowed GML [surface](#surface) object elements are used as child elements of a feature from the application schema. For unmet constraints report invalidSurfaceElementFound.
* Verify that only planar interpolation is used, i.e. check that only [PolygonPatch](#PolygonPatch) is used as a GML surface patch object elements in features from the application schema. For unmet constraints report invalidSurfacePatchElementFound.
* Verify that only valid GML geometry elements are used, i.e. check that none of the [disallowed](#disallowed) GML geometry object elements are used as child elements of a feature from the application schema. For unmet constraints report invalidGeometryElementFound.
* Verify that in points only gml:pos is used for coordinates, i.e. check that only [pos1](#pos1) is used in point geometries of a feature from the application schema. For unmet constraints report invalidPositionElementFound.
* Verify that in curves and surfaces only gml:posList is used for coordinates, i.e. check that the only gml:posList is used in curve and surface geometries of a feature from the application schema. For unmet constraints report invalidPositionElementFound.
* Verify that geometry aggregates do not use the GML array property elements, i.e. check that the only the regular property elements are used, but not the [array](#array) property elements. For example, for a gml:MultiPoint, only gml:pointMember may be used, not gml:pointMembers. For violations report arrayElementFound.
* Coordinate reference systems may have 1, 2 or 3 dimensions, i.e. check all occurances of [srsDimension](#srsDimension) and for values greater than '3' report tooManyDimensions.
* Verify that in curves and surfaces only gml:posList is used for coordinates, i.e. validate all geometry elements of a feature from the application schema using a geometry library. For invalid geometries report invalidGeometry.

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 12 (1)

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
spatialTopologyTypeFound <a name="spatialTopologyTypeFound"/>  |  XML document '$filename', $featureType '$gmlid': A spatial topology element '$elementName' was found. Spatial properties are limited to the set of geometric types consisting of point, curve with linear interpolation, planar surface, or aggregates thereof. Spatial topology is excluded.
invalidInterpolationFound <a name="invalidInterpolationFound"/>  |  XML document '$filename', $featureType '$gmlid': A curve geometry with an invalid curve segment '$elementName' was found. Curves (standalone or within surfaces) must have linear interpolation (LineString, Curve with LineStringSegment segments).
invalidSurfaceElementFound <a name="invalidSurfaceElementFound"/>  |  XML document '$filename', $featureType '$gmlid': A surface geometry with an invalid GML object element '$elementName' was found. Planar surface types are restricted to Polygon or Surface elements.
invalidSurfacePatchElementFound <a name="invalidSurfacePatchElementFound"/>  |  XML document '$filename', $featureType '$gmlid': A surface geometry with an invalid GML object element '$elementName' for surface patches was found. Surface patches are restricted to gml:PolygonPatch elements.
invalidGeometryElementFound <a name="invalidGeometryElementFound"/>  |  XML document '$filename', $featureType '$gmlid': A geometry with an invalid GML object element '$elementName' was found. Supported geometry types are restricted to point, curve with linear interpolation, planar surface, or aggregates thereof.
invalidPositionElementFound <a name="invalidPositionElementFound"/>  |  XML document '$filename', $featureType '$gmlid': A $geometryType geometry with an invalid GML object element for coordinates '$elementName' was found. Only $posElementName is allowed.
arrayElementFound <a name="arrayElementFound"/>  |  XML document '$filename', $featureType '$gmlid': A geometric aggregate using the array property '$elementName' was found. Only the standard properties (gml:pointMember for gml:MultiPoint, gml:curveMember for gml:MultiCurve, gml:surfaceMember for gml:MultiSurface, and gml:geometryMember for gml:MultiGeometry) are allowed.
tooManyDimensions <a name="tooManyDimensions"/>  |  XML document '$filename', $featureType '$gmlid': Coordinates with a dimension '$dimension' were found. Only coordinate reference systems with 1, 2 or 3 dimensions are allowed.
invalidGeometry <a name="invalidGeometry"/>  |  XML document '$filename', $featureType '$gmlid': The feature geometry is not a valid GML geometry.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
features <a name="features"></a>   | //schema-element(hy-n3:HydroNode) \| //schema-element(hy-n3:WatercourseLink) \| //schema-element(hy-n3:WatercourseLinkSequence) \| //schema-element(hy-n3:WatercourseSeparatedCrossing) \| //schema-element(hy-n4:HydroNode) \| //schema-element(hy-n4:WatercourseLink) \| //schema-element(hy-n4:WatercourseLinkSequence) \| //schema-element(hy-n4:WatercourseSeparatedCrossing)
topology <a name="topology"></a>  | $features[.//\*[self::gml:Node|self::gml:Edge|self::gml:Face|self::gml:TopoSolid|self::gml:TopoPoint|self::gml:TopoCurve|self::gml:TopoSurface|self::gml:TopoVolume|self::gml:TopoComplex]
nonlinear <a name="nonlinear"></a>  | $features[.//gml:Curve/gml:segments/\*[not(self::gml:LineStringSegment)]]
surface <a name="surface"></a>  | $features[.//\*[self::gml:OrientableSurface|self::gml:CompositeSurface|self::gml:PolyhedralSurface|self::gml:Tin|self::gml:TriangulatedSurface]]
PolygonPatch <a name="PolygonPatch"></a>  | $features[.//gml:Surface/gml:patches/\*[not(self::gml:PolygonPatch)]]
disallowed <a name="disallowed"></a>  | $features[.//\*[self::gml:Solid|self::gml:MultiSolid|self::gml:CompositeSolid|self::gml:CompositeCurve|self::gml:Grid]]
pos1 <a name="pos1"></a>  | $features[.//gml:Point/\*[not(self::gml:pos)]]
pos2 <a name="pos2"></a>  | $features[.//\*[self::gml:LineString|self::gml:LineStringSegment|self::gml:LinearRing]/\*[not(self::gml:posList)]]
array <a name="array"></a>  | $features[.//\*[self::gml:MultiPoint/gml:pointMembers|self::gml:MultiCurve/gml:curveMembers|self::gml:MultiSurface/gml:surfaceMembers|self::gml:MultiGeometry/gml:geometryMembers]]
srsDimension <a name="srsDimension"></a>  | $features[.//\*[@srsDimension > 3]]
