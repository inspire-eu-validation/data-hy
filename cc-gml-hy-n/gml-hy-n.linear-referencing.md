# gml-hy-n.linear-referencing

**Version**: 0.1

**Purpose**: Verify that identifiers are reusing authoritative, pan-European sources.

**Prerequisites**

n/a

**Test method**

* For each NetworkProperty feature that links to a WatercourseLink or a WatercourseLinkSequence, verify that any linear references are consistent with the length of the geometry of the network feature.

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 8.7.3 (2)

**Test type**: Automated

**Notes**

As there is no network property specified in the application schema, this requirement is superfluous and the test could be dropped. It really belongs to application schemas that make use of NetworkProperty features that reference WatercourseLink features.

## Messages

n/a

## Contextual XPath references

n/a