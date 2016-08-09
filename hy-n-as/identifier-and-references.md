# Identifiers and references

**Version**: 1

**Purpose**: Verify the consistent use of identifiers and references to other features.

**Prerequisites**

**Test method**

* Verify that identifiers are reusing authoritative, pan-European sources, i.e. review for each feature that, if there is another feature representing the same real world object, then these spatial objects shall carry either the same, unique, geographical name or the same hydrographic thematic identifier.
* For each NetworkProperty feature that links to a WatercourseLink or a WatercourseLinkSequence, verify that any linear references are consistent with the length of the geometry of the network feature.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Section 8.7.3 (1)
* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Section 8.7.3 (2)

**Test type**: Manual

**Notes**:

As there is no network property specified in the application schema, the NetworkProperty-related test is superfluous and the test should be dropped from the data specification. These tests belong to application schemas that make use of NetworkProperty features that reference WatercourseLink features.

## Messages

n/a

## Contextual XPath references

n/a