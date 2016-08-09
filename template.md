# Title of Test Case (unique within the Conformance Class)

**Version**: 1

**Purpose**: One or two sentences inlined here: Why this test is necessary?

**Prerequisites**

* [Title of Test Case](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/cc/tc)

**Test method**

A paragraph of the test steps and assertions. Use bullets or any markdown formatting as necessary:

* Use the XPath abbreviations as links in the text: [ExtendedCapabilities](#extendedCapabilities) must exist... Messages for failed assertions are also included as links in the text with a unique identifier, e.g. [messageId](#messageId).
* Step 2,...

**Reference(s)**: 

* References to requirements. Common abbreviations are used and are explained in a table in [README.md](README.md)

**Test type**: Automated or Manual

**Notes**

Any additional notes. We can also use this for open questions during drafting.

## Parameters

Identifier  |  Description
---------------------------------------------------------- | -------------------------------------------------------------------------
paramName <a name="paramName"/>  |  description and value range

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
messageId <a name="messageId"/>  |  $featureType '$gmlid':  xxxx has value

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/data-hy/3.1/cc/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="extendedCapabilities"></a>   | /wms:WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities[1]