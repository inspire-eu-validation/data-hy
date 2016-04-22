# gml.code-list-extensions

**Version**: 0.1

**Purpose**: Ensure that any extensions do not contradict or overlap with the approved INSPIRE code lists.

**Prerequisites**

* [gml.root-element](gml.root-element.md)

**Test method**

* Inspect the code list valued property elements (TODO: compile list). If a reference (@xlink:href) has a value that does not start with
http://inspire.ec.europa.eu/codelist/, review the code list to check that any extensions do not overlap with the code lists that are defined in Annexes II, III and IV and that all extensions conform to the requirements.

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 4 (1)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 6 (1)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 6 (2)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)
* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 6 (4)

**Test type**: Manual

**Notes**

Potentially move to application schema specific conformance classes.

## Messages

n/a

## Contextual XPath references

n/a