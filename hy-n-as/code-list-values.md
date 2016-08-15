# Code list values

**Version**: 1

**Purpose**: Verify whether all attributes whose value type is a code list take the values set out therein

**Prerequisites**

**Test method**

When an attribute has a code list as its type, verify that the values comply with the definitions and include the values set out in Annex II of the regulation. To pass this tests that any instance of an attribute

* takes only values explicitly specified in the INSPIRE code list register when the code list‘s extensibility is 'none'.
* takes only a value explicitly specified in the INSPIRE code list register or shall take a value that is narrower (i.e. more specific) than those explicitly specified in the application schema when the code list‘s extensibility is 'narrower'.

Otherwise report [disallowedCodeListValue](#disallowedCodeListValue).

In the Hydrography - Network application schema, the following properties have to be tested:
* [flowDirection (v3)](#flowDirection3). Valid values:
  * bothDirections 
  * inDirection
  * inOppositeDirection
* [flowDirection (v4)](#flowDirection4). Valid values:
  * http://inspire.ec.europa.eu/codelist/LinkDirectionValue/bothDirections 
  * http://inspire.ec.europa.eu/codelist/LinkDirectionValue/inDirection
  * http://inspire.ec.europa.eu/codelist/LinkDirectionValue/inOppositeDirection
* [hydroNodeCategory (v3)](#hydroNodeCategory3). Valid values:
  * boundary
  * flowConstriction
  * flowRegulation
  * junction
  * outlet
  * source
* [hydroNodeCategory (v4)](#hydroNodeCategory4). Valid values:
  * http://inspire.ec.europa.eu/codelist/HydroNodeCategoryValue/boundary
  * http://inspire.ec.europa.eu/codelist/HydroNodeCategoryValue/flowConstriction
  * http://inspire.ec.europa.eu/codelist/HydroNodeCategoryValue/flowRegulation
  * http://inspire.ec.europa.eu/codelist/HydroNodeCategoryValue/junction
  * http://inspire.ec.europa.eu/codelist/HydroNodeCategoryValue/outlet
  * http://inspire.ec.europa.eu/codelist/HydroNodeCategoryValue/source

The following is not applicable for this application schema as no extensions are allowed. It is still included here as a reminder in case extensions will be allowed in the future:

Inspect the code list valued property elements. If a value is not one of the values listed above, review the code list definition to check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV of the Implementing Rule and that all extensions conform to the requirements. This is a manual test.
  
**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (2)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Article 6 (4)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
disallowedCodeListValue <a name="disallowedCodeListValue"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that is not one of the allowed values listed at $codelist. 

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
flowDirection (v4) <a name="flowDirection4"></a>   | //schema-element(hy-n4:WatercourseLink)/hy-n4:flowDirection/@xlink:href
hydroNodeCategory (v4) <a name="hydroNodeCategory4"></a>   | //schema-element(hy-n4:HydroNode)/hy-n4:hydroNodeCategory/@xlink:href
flowDirection (v3) <a name="flowDirection3"></a>   | //schema-element(hy-n3:WatercourseLink)/hy-n3:flowDirection/text()
hydroNodeCategory (v3) <a name="hydroNodeCategory3"></a>   | //schema-element(hy-n3:HydroNode)/hy-n3:hydroNodeCategory/text()
