Open questions:
* Support also version 3 in tests?

---

IR Article 3
Types that are common to several of the themes listed in Annexes I, II and III to Directive 2007/2/EC shall conform to the definitions and constraints and include the attributes and association roles set out in Annex I.

IR Article 4 (1)
For the exchange and classification of spatial objects from data sets meeting the conditions laid down in Article 4 of Directive 2007/2/EC, Member States shall use the spatial object types and associated data types, enumerations and code lists that are defined in Annexes II, III and IV for the themes the data sets relate to.

IR Article 4 (2)
Spatial object types and data types shall comply with the definitions and constraints and include the attributes and association roles set out in the Annexes.

IR Article 4 (3)
The enumerations and code lists used in attributes or association roles of spatial object types or data types shall comply with the definitions and include the values set out in Annex II. The enumeration and code list values are uniquely identified by language-neutral mnemonic codes for computers. The values may also include a language-specific name to be used for human interaction.

TG Requirement 1 
Spatial object types and data types shall comply with the multiplicities defined for the attributes and association roles in this section.

IR Article 5 (2)
Types that are a sub-type of another type shall also include all this type‘s attributes and association roles.

IR Article 5 (3)
Abstract types shall not be instantiated.

IR Article 6 (1)
Codelists shall be of one of the following types, as specified in the Annexes:
a) code lists whose allowed values comprise only the values specified in this Regulation;
b) code lists whose allowed values comprise the values specified in this Regulation and
narrower values defined by data providers;
c) code lists whose allowed values comprise the values specified in this Regulation and
additional values at any level defined by data providers;
d) code lists, whose allowed values comprise any values defined by data providers.
For the purposes of points (b), (c) and (d), in addition to the allowed values, data providers may use the values specified in the relevant INSPIRE Technical Guidance document available on the INSPIRE web site of the Joint Research Centre.

IR Article 6 (2)
Code lists may be hierarchical. Values of hierarchical code lists may have a more generic parent value. Where the valid values of a hierarchical code list are specified in a table in this Regulation, the parent values are listed in the last column.

IR Article 6 (3)
Where, for an attribute whose type is a code list as referred to in points (b), (c) or (d) of paragraph 1, a data provider provides a value that is not specified in this Regulation, that value and its definition shall be made available in a register.

IR Article 6 (4)
Attributes or association roles of spatial object types or data types whose type is a code list may only take values that are allowed according to the specification of the code list.

IR Article 6 (5)
Attributes or association roles of spatial object types or data types that have an enumeration type may only take values from the lists specified for the enumeration type.

IR Article 8
1. Member States shall make available updates of data on a regular basis.
2. All updates shall be made available at the latest 6 months after the change was applied in the source data set, unless a different period is specified for a specific spatial data theme in Annex II.

IR Article 9 (1)
The data type Identifier defined in Section 2.1 of Annex I shall be used as a type for the external object identifier of a spatial object.

IR Article 9 (2)
The external object identifier for the unique identification of spatial objects shall not be changed during the life-cycle of a spatial object.

IR Article 10 (3)
Where the attributes beginLifespanVersion and endLifespanVersion are used, the value of endLifespanVersion shall not be before the value of beginLifespanVersion.

IR Article 12 (3)
Where the attributes validFrom and validTo are used, the value of validTo shall not be before the value of validFrom.

TG Requirement 6
Data instance (XML) documents shall validate without error against the provided XML schema.

-

gml.utf8
D2.7 3.3 req 12
Inspect each XML document. If an XML declaration exists, verify that encoding="UTF-8" or that the attribute is missing.

gml.feature-collection
D2.7 3.3 rec 11
Inspect the root element of each XML document. Verify that it is either {http://www.opengis.net/wfs/2.0}FeatureCollection, {http://www.opengis.net/gml/3.2}FeatureCollection or {http://inspire.ec.europa.eu/schemas/base/3.3}SpatialDataSet.

Warning: root element of document is not {http://www.opengis.net/wfs/2.0}FeatureCollection 

gml.schema-extensions-not-overlapping (MANUAL)
IR Article 4 (1)
Inspect the XML Schema namespace of each feature element. If a namespace is not one of the current list of approved INSPIRE application schema namespaces (TODO: need to compile list), ask the user to review the extension documentation for the identified namespaces to check that any extensions do not overlap with the spatial object types and associated data types and enumerations that are defined in Annexes II, III and IV.

gml.code-list-extensions (MANUAL)
IR Article 4 (1)
IR Article 6 (1)
IR Article 6 (2)
IR Article 6 (3)
IR Article 6 (4)
Inspect the code list valued property elements. If a reference (@xlink:href) has a value that does not start with
http://inspire.ec.europa.eu/codelist/, ask the user to review the code list to check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV and that all extensions conform to the requirements.

gml.schemaLocation-provided
IR Article 4 (2)
Inspect the root element and verify that a xsi:schemaLocation attribute is provided.

gml.schema-valid-1
IR Article 3
IR Article 4 (2)
IR Article 4 (3)
IR Article 5 (2)
IR Article 5 (3)
IR Article 6 (5)
IR Article 9 (1)
TG Requirement 1 
TG Requirement 6
Prerequisite: gml.schemaLocation-provided
Validate each document against the schema(s) specified in the xsi:schemaLocation attribute.

gml.schema-valid-2
IR Article 4 (2)
Each property element shall either carry a resolvable reference to an object (@xlink:href), contain an object element or contain non-empty text (whitespace is trimmed before checking for empty text).

Warning: no gml:identifier or no HTTP URI in gml:identifier (D2.7 3.3 rec 10)

gml.nilReason-values
IR Article 4 (3)
Inspect all @nilReason values and verify that one of the following is used: 
* (TODO: GML values or VoidReasonValue URIs)

gml.identifier-persistent (MANUAL)
IR Article 9 (2)
Verify that rules for identifiers in the documentation of the spatial data set specify that the identifiers do not change during the life-cycle of a spatial object.

gml.endLifespanVersion
IR Article 10 (3)
For each feature verify that either
* beginLifespanVersion or endLifespanVersion are missing or nil or
* endLifespanVersion is not before the value of beginLifespanVersion.

gml.validTo
IR Article 10 (3)
For each feature verify that either
* validFrom or validTo are missing or nil or
* validTo is not before the value of validFrom.

---

IR Article 11 (1)
The default temporal reference system referred to in point 5 of part B of the Annex to Commission Regulation (EC) No 1205/2008 (14) shall be used, unless other temporal reference systems are specified for a specific spatial data theme in Annex II.

IR Article 12 (1)
The value domain of spatial properties defined in this Regulation shall be restricted to the Simple Feature spatial schema as defined in Herring, John R. (ed.), OpenGIS® Implementation Standard for Geographic information – Simple feature access – Part 1: Common architecture, version 1.2.1, Open Geospatial Consortium, 2011, unless specified otherwise for a specific spatial data theme or type.

IR Article 12 (2)
All measurement values shall be expressed using SI units or non-SI units accepted for use with the International System of Units, unless specified otherwise for a specific spatial data theme or type.

gml.updates (MANUAL)
IR Article 8
Verify that the last update in the source data set is less than 6 months.

IR Annex II, Section 1.2
For the three-dimensional and two-dimensional coordinate reference systems and the horizontal component of compound coordinate reference systems used for making spatial data sets available, the datum shall be the datum of the European Terrestrial Reference System 1989 (ETRS89) in areas within its geographical scope, or the datum of the International Terrestrial Reference System (ITRS) or other geodetic coordinate reference systems compliant with ITRS in areas that are outside the geographical scope of ETRS89. Compliant with the ITRS means that the system definition is based on the definition of the ITRS and there is a well documented relationship between both systems, according to EN ISO 19111.

IR Annex II, Section 1.3
Spatial data sets shall be made available using at least one of the coordinate reference systems specified in sections 1.3.1, 1.3.2 and 1.3.3, unless one of the conditions specified in section 1.3.4 holds.

IR Annex II, Section 1.5 (1)
Coordinate reference system parameters and identifiers shall be managed in one or several common registers for coordinate reference systems.

IR Annex II, Section 1.5 (2)
Only identifiers contained in a common register shall be used for referring to the coordinate reference systems listed in this Section.

TG requirement 2
The identifiers listed in Table 2 shall be used for referring to the coordinate reference systems used in a data set.

IR Annex II, Section 8.7.1 (1)
Hydrography links, centrelines and nodes shall always be located within the extent of the area representation of the same object.

IR Annex II, Section 8.7.1 (2)
Connectivity between hydrographic networks across state borders and – where applicable – also across regional borders (and data sets) within Member States shall be established and maintained by the respective authorities, using the cross-border connectivity mechanisms provided by the NetworkConnection type.

IR Annex II, Section 8.7.1 (3)
All attribution of objects in this schema shall be the same as the equivalent property of that object used for reporting obligations under Directive 2000/60/EC.

IR Annex II, Section 8.7.2 (1)
If a geographical name is used as a unique hydrologic ID for an object in this specification then it shall be derived, where possible, from a pan-European Gazetteer or another authoritative, pan- European source.
       
IR Annex II, Section 8.7.2 (2)
The localId attribute of the external object identifier of a spatial object shall be the same as the ID used for reporting obligations under Directive 2000/60/EC.

IR Annex II, Section 8.7.3 (1)
If the same real world object in a data set is exchanged using spatial objects from more than one of the Hydrography application schemas then these spatial objects shall carry either the same, unique, geographical name or the same hydrographic thematic identifier.
       
IR Annex II, Section 8.7.3 (2)
When linear referencing is used in hydrographic Network data, the position of referenced properties on links and link sequences shall be expressed as distances measured along the supplied geometry of the underlying link object(s).

IR Annex II, Section 8.7.4 (1)
If spatial objects are provided at different spatial resolutions, the spatial resolution must be specified for each spatial object using the levelOfDetail attribute where applicable.

IR Annex II, Section 8.7.4 (2)
Watercourse links shall intersect wherever a connection exists between the real world phenomena they represent. No intersections shall be created at crossing network elements when it is not possible for water to pass from one element to another.

IR Annex II, Section 8.7.4 (3)
In a hydrographic network data set which contains nodes, these nodes shall only be present where Watercourse Links connect or end.

IR Annex II, Section 8.7.4 (4)
The geometry shall be the same as the geometry used for reporting obligations under Directive 2000/60/EC.

IR Annex II, Section 8.7.5 (2)
The attribute delineationKnown shall not be used to indicate a change of geometry over time where this change of geometry is known.

IR Annex II, Section 8.7.6
The centrelines of watercourse objects shall fall within the extent of the physical real world object that they represent if the Watercourse Link is indicated as not being 'fictitious'.

IR Annex II, Section 8.7.7 (1)
Wherever a connection exists in a hydrographic network, all connected link ends and the optional node that take part in this connection have to be positioned at a distance of less than the connectivity tolerance from each other.
        
IR Annex II, Section 8.7.7 (2)
Link ends and nodes that are not connected shall always be separated by a distance that is greater than the connectivity tolerance.
       
IR Annex II, Section 8.7.7 (3)
In data sets where both transport links and nodes are present, the relative position of nodes and link ends in relation to the specified connectivity tolerance shall correspond to the associations that exist between them in the data set.

-

Two conformance classes:

http://inspire.ec.europa.eu/conformance-class/tg/hy-n/3.1 

Instantiable feature types in namespace http://inspire.ec.europa.eu/schemas/hy-n/4.0:
* HydroNode
* WatercourseLink
* WatercourseLinkSequence
* WatercourseSeparatedCrossing

http://inspire.ec.europa.eu/conformance-class/tg/hy-p/3.1

Instantiable feature types in namespace http://inspire.ec.europa.eu/schemas/hy-p/4.0:
* Crossing
* DrainageBasin
* Embankment
* Falls
* FluvialPoint
* Ford
* LandWaterBoundary
* Lock
* Rapids
* RiverBasin
* Shore
* ShorelineConstruction
* Sluice
* SurfaceWater
* Watercourse
* Wetland

NOTE: The XML Schema declarations of each feature in a non-INSPIRE namespace has to be accessed. Recursively identify the first element in an INSPIRE or GML namespace. If it is one of the above, treat these features in the tests as if they were of that INSPIRE feature type.

NOTE: When we mention "features" in the test cases, this refers to all features that belong to the corresponding application schema (and not to any other feature in the data set).

gml-hy-n/p.constraints
IR Article 4 (2)
Validate features against the OCL constraints included in the UML model of the INSPIRE application schemas (TODO: extract constraints from UML for the feature types and convert to XQuery/XPath).

gml-hy-n/p.code-list-values
IR Article 4 (3)
IR Article 6 (1)
Verify that the code lists used in attributes or association roles of the features comply with the definitions and include the values set out in Annex II (TODO: compile list of attributes with code list values and the allowed values for each feature type). Check that URIs resolve.

Warning: no xlink:title

gml-hy-n/p.simple-features
IR Article 12 (1)
Verify for each feature that the Simple Feature requirements are met (use geometry related tests of http://schemas.opengis.net/gmlsfProfile/2.0/gmlsfL2.sch).

gml-hy-n/p.crs
IR Annex II, Section 1.2
IR Annex II, Section 1.3
IR Annex II, Section 1.5 (1)
IR Annex II, Section 1.5 (2)
TG requirement 2
Verify that all uses of @srsName in the features and the bounding box of the feature collection use one of the http URIs from the third column of table 2. [Add additional values to the list for regions outside of continental Europe, if nominated by a Member State and available in a CRS register with a persistent http URI.]

gml-hy-n/p.trs
IR Article 11 (1)
In the features, check all values of the attribute @frame in {http://www.opengis.net/gml/3.2}TimeInstance, {http://www.opengis.net/gml/3.2}timePosition, {http://www.opengis.net/gml/3.2}TimePeriod, {http://www.opengis.net/gml/3.2}beginPosition and {http://www.opengis.net/gml/3.2}endPosition. Verify that only "http://www.opengis.net/def/trs/ISO-8601/" is used as a value.

NOTE: all value in the XML Schema date/time types is automatically in the require reference system.

NOTE: Can be removed here, no TM objects are used in these application schemas.

gml-hy-n/p.uom
IR Article 12 (2)
In the features, check all values of the attribute @uom to be one of the following: [Compile list of units and allow the UCUM representations and OGC or INSPIRE registry URIs, where available]

gml-hy-n/p.attribute-consistency (MANUAL)
IR Annex II, Section 8.7.1 (3)
Review for each feature that all attribution is the same as the equivalent property of that object used for reporting obligations under Directive 2000/60/EC.

gml-hy-n/p.identifier-consistency (MANUAL)
IR Annex II, Section 8.7.2 (2)
Review for each feature that the localId attribute of the external object identifier is the same as the ID used for reporting obligations under Directive 2000/60/EC.

gml-hy-n/p.geometry (MANUAL)
IR Annex II, Section 8.7.4 (4)
Review for each feature that the geometry is the same as the geometry used for reporting obligations under Directive 2000/60/EC.

gml-hy-n/p.identifier-source (MANUAL)
IR Annex II, Section 8.7.2 (1)
Review for each feature that, if a geographical name is used as a unique hydrologic ID for an object in this specification that it is derived, where possible, from a pan-European Gazetteer or another authoritative, pan-European source.

gml-hy-n/p.object-references (MANUAL)
IR Annex II, Section 8.7.3 (1)
Review for each feature that, if there is another feature representing the same real world object, then these spatial objects shall carry either the same, unique, geographical name or the same hydrographic thematic identifier.

NOTE: Obviously this was not meant to be part of the regulation and will be removed in the future. So maybe drop the test?

gml-hy-n.consistency-at-borders (MANUAL)
IR Annex II, Section 8.7.1 (2)
Review the data maintenance procedures and perform spot checks to verify that connectivity between hydrographic networks across state borders and – where applicable – also across regional borders (and data sets) within Member States is established and maintained by the respective authorities, using the cross-border connectivity mechanisms provided by the NetworkConnection type.

gml-hy-n.linear-referencing
IR Annex II, Section 8.7.3 (2)
For each NetworkProperty feature that links to a WatercourseLink or a WatercourseLinkSequence, verify that any linear references are consistent with the length of the geometry of the network feature.

NOTE: As there is no network property specified in the application schema, this requirement is superfluous and the test could be dropped. It really belongs to application schemas that make use of NetworkProperty features that reference WatercourseLink features.

gml-hy-n.link-intersections (MANUAL)
IR Annex II, Section 8.7.4 (2)
Verify that WatercourseLink features intersect wherever a connection exists between the real world phenomena they represent. Note that no intersections are created at crossing network elements when it is not possible for water to pass from one element to another.

gml-hy-n.link-centrelines (MANUAL)
IR Annex II, Section 8.7.6
Verify for each WatercourseLink object with fictitious=false that its centerlineGeometry falls within the extent of the physical real world object that they represent.

gml-hy-n.no-free-nodes
IR Annex II, Section 8.7.4 (3)
Verify for each HydroNode that the geometry (a {http://www.opengis.net/gml/3.2}Point) is located a position that touches a WatercourseLink.centerlineGeometry (a {http://www.opengis.net/gml/3.2}LineString or {http://www.opengis.net/gml/3.2}Curve).

NOTE: This is not consistent with the Connectivity tolerance allowed in IR Annex II, Section 8.7.7 - except the tolerance is 0.

gml-hy-p.multiple-resolutions (MANUAL)
IR Annex II, Section 8.7.4 (1)
If features are provided at different spatial resolutions, verify that the spatial resolution is specified for each of the features in the levelOfDetail attribute.

gml-hy-p.delineationKnown (MANUAL)
IR Annex II, Section 8.7.5 (2)
Verify for each Shore and Watercourse feature with a value for the attribute delineationKnown that the value is not used to indicate a change of geometry over time where this change of geometry is known.

gml-hy-n.network-connectivity-1 (PARAM connectivity-tolerance)
IR Annex II, Section 8.7.7 (1)
For each WatercourseLink with a startNode or endNode property, verify that the distance between the start or end of the centerlineGeometry and the geometry of the associated HydroNode is smaller than the connectivity-tolerance.

NOTE: Geometries typically will need to be converted into a meter-based CRS, eg ETRS89 LAEA or LCC. It is unclear how to handle geometries outside of continental Europe, classify as MANUAL?

gml-hy-n.network-connectivity-2 (PARAM connectivity-tolerance)
IR Annex II, Section 8.7.7 (2)
For each WatercourseLink, verify that the only HydroNodes in the distance around the start or end of the centerlineGeometry are the nodes associated via the startNode or endNode property.

NOTE: See note in network-connectivity-1.

gml-hy-n.network-connectivity-3 (PARAM connectivity-tolerance)
IR Annex II, Section 8.7.7 (3)
[I do not understand the requirement.]

NOTE: See note in network-connectivity-1.

gml-hy-n.network-connectivity-4 (MANUAL)
IR Annex II, Section 8.7.7 (1)
IR Annex II, Section 8.7.7 (2)
IR Annex II, Section 8.7.7 (3)
Verify that the connectivity tolerance provided by the user is the same included in the metadata of the data set in the properties 'specification' and 'explanation' of the DQ\_ConformanceResult element in a DQ_TopologicalConsistency element.

PARAM connectivity-tolerance
The user provides the connectivity-tolerance in meter. 

gml-hy-n.representation-consistency 
IR Annex II, Section 8.7.1 (1)
If the data set contains both WatercourseLink and SurfaceWater (Watercourse or StandingWater) features, verify for each WatercourseLink that its centerlineGeometry is within the geometry of a single Watercourse or StandingWater feature. Verify for each HydroNode that its geometry is within a Watercourse or StandingWater feature, too.

NOTE: This could be part of either one of the two conformance classes.

---

IR Annex II, Section 1.4
Coordinate Reference Systems used in the View Network Service
For the display of spatial data sets with the view network service as specified in Regulation No 976/2009, at least the coordinate reference systems for two-dimensional geodetic coordinates (latitude, longitude) shall be available.

IR Article 14
Portrayal
1. For the portrayal of spatial data sets using a view network service as specified in Commission Regulation No 976/2009 (16), the following shall be available:
(a) the layers specified in Annex II for the theme or themes the data set is related to;
(b) for each layer at least a default portrayal style, with as a minimum an associated title and a
unique identifier.
2. For each layer, Annex II defines the following:
(a) a human readable title of the layer to be used for display in user interface;
(b) the spatial object type(s), or sub-set thereof, that constitute(s) the content of the layer.

TG Requirement 7 
For each layer specified in this section, the styles defined in section 11.2 shall be available.

---

IR Article 13
Metadata required for Interoperability
The metadata describing a spatial data set shall include the following metadata elements required for interoperability:
1. Coordinate Reference System: Description of the coordinate reference system(s) used in the data set.
2. Temporal Reference System: Description of the temporal reference system(s) used in the data set.
This element is mandatory only if the spatial data set contains temporal information that does not refer to the default temporal reference system.
3. Encoding: Description of the computer language construct(s) specifying the representation of data objects in a record, file, message, storage device or transmission channel.
4. Topological Consistency: Correctness of the explicitly encoded topological characteristics of the data set as described by the scope.
This element is mandatory only if the data set includes types from the Generic Network Model and does not assure centreline topology (connectivity of centrelines) for the network.
5. Character Encoding: The character encoding used in the data set.
This element is mandatory only if an encoding is used that is not based on UTF-8.
6. Spatial Representation Type: The method used to spatially represent geographic information.

TG Requirement 3 
Metadata instance (XML) documents shall validate without error against the used ISO 19139 XML schema.

TG Requirement 4 
Metadata instance (XML) documents shall contain the elements and meet the INSPIRE multiplicity specified in the sections below.

TG Requirement 5 
The elements specified below shall be available in the specified ISO/TS 19139 path.
