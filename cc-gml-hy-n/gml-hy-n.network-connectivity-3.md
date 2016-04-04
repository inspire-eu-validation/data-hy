# gml-hy-n.network-connectivity-3

**Version**: 0.1

**Purpose**: Verify that ???

**Prerequisites**

* [gml-hy-n.basic-test](gml-hy-n.basic-test.md)

**Test method**

* ???

**Reference(s)**: 

* [TG DS Template](README.md#ref_TG_DS_tmpl) IR requirement Section 8.7.7 (3)

**Test type**: ???

**Notes**

Requirement unclear: "In data sets where both transport links and nodes are present, the relative position of nodes and link ends in relation to the specified connectivity tolerance shall correspond to the associations that exist between them in the data set." What should be tested?

Geometries typically will need to be converted into a meter-based CRS, eg ETRS89 LAEA or LCC. 

It is unclear how to handle geometries outside of continental Europe. Classify as MANUAL?

## Parameters

Identifier  |  Description
---------------------------------------------------------- | -------------------------------------------------------------------------
connectivityTolerance <a name="tolerance"/>  |  a number, the tolerance in meter

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
