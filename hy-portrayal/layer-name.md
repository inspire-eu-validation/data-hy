# Layer name

**Purpose**: For the portrayal of spatial data sets using a view service, the layers specified in chapter 11 shall be available.

**Prerequisites**

**Test method**

* Check that at least one [layer name](#name) is one of the [harmonized names](#names) for the data theme.

**Reference(s)**:

* [TG DS-HY](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-portrayal/README#ref_TG_DS_HY), IR Requirement, Article 14(1)(a)

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-portrayal/README#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
layer name <a name="name"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Name | ISO 19128
                                 | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:Identifier | WMTS 1.0.0
harmonized names <a name="names"></a> | ('HY.PhysicalWaters.Waterbodies', 'HY.PhysicalWaters.LandWaterBoundary', 'HY.PhysicalWaters.Catchments', 'HY.Network', 'HY.PhysicalWaters.HydroPointOfInterest', 'HY.PhysicalWaters.ManMadeObject', 'HY.PhysicalWaters.Wetland', 'HY.PhysicalWaters.Shore')
