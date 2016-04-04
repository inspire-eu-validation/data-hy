# gml.schema-extensions-not-overlapping

**Version**: 0.1

**Purpose**: Ensure that any extensions do not contradict or overlap with the approved INSPIRE application schemas

**Prerequisites**

* [gml.root-element](gml.root-element.md)

**Test method**

* Inspect the XML Schema namespace of each feature element. If a namespace is not one of the current list of approved INSPIRE application schema namespaces (TODO: compile list), review the extension documentation for the identified namespaces to check that any extensions do not overlap with the spatial object types and associated data types and enumerations that are defined in Annexes II, III and IV.

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Article 4 (1)

**Test type**: Manual

## Messages

n/a

## Contextual XPath references

n/a