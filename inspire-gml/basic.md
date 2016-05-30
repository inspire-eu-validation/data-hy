# basic

**Version**: 0.1

**Purpose**: Verify that all documents are consistent with the standardization target of the conformance class.

**Prerequisites**

* [Conformance Class 'GML 3.2 documents'](http://www.opengis.net/doc/IS/GML/3.2/clause/2.4)

*Note*: Executable Test Suite for the conformance class: http://cite.opengeospatial.org/teamengine/about/gml32/3.2.1/site/

**Test method**

* Verify for each XML document that the root element is either a GML feature or a GML feature collection. For feature collections the following elements are recognised: wfs:FeatureCollection, gml:FeatureCollection, base:SpatialDataSet. Otherwise report [incorrectRoot](#incorrectRoot)

**Reference(s)**: 

* [D2.7](README.md#ref_D2_7) recommendation 11
* [GML 3.2](README.md#ref_GML32) 2.4

**Test type**: Automated

**Notes**

The use of the WFS 2.0 feature collection is recommended, but other feature collections (e.g. SpatialDataSet or gml:FeatureCollection) are currently allowed, too.

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
incorrectRoot <a name="incorrectRoot"/>  |  XML document '$filename':  The root element is not a GML feature and not one of the recognised feature collections ({http://www.opengis.net/wfs/2.0}FeatureCollection, {http://www.opengis.net/gml/3.2}FeatureCollection or {http://inspire.ec.europa.eu/schemas/base/3.3}SpatialDataSet). The name of the root element is '$elementName' in namespace '$namespace'. It is recommended to use the WFS 2.0 feature collection element in INSPIRE.

## Contextual XPath references

n/a