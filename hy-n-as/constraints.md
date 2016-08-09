# Constraints

**Version**: 1

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

Verify that the OCL constraints listed below that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation).

This is not applicable for this application schema as no constraints are specified. The test case is still included as a reminder in case constraints will be added in the future.

The test always passes.

**Reference(s)**: 

* [TG DS Template](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-HY](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/hy-n-as/README#ref_TG_DS_HY)) 5.4

**Test type**: Automated

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

n/a
