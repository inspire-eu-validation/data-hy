# ID of Test Case (unique within the Conformance Class)

**Version**: 0.1

**Purpose**: One or two sentences inlined here: Why this test is necessary?

**Prerequisites**

* [ID of Conformance Class](http://example.com/uri/of/conformance-class)
* [ID of Test Case](http://example.com/uri/of/test-case)

**Test method**

A paragraph of the test steps and assertions. Use bullets or any markdown formatting as necessary:

* Use the XPath abbreviations as links in the text: [ExtendedCapabilities](#extendedCapabilities) must exist... Messages for failed assertions are also included as links in the text with a unique identifier, e.g. [messageId](#messageId).
* Step 2,...

**Reference(s)**: 

* References to requirements. Common abbreviations are used and are explained in a table in [README.md](README.md)

**Test type**: Automated or Manual

**Notes**

Any additional notes. We can also use this for open questions during drafting.

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
messageId <a name="messageId"/>  |  $featureType '$gmlid':  xxxx has value

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="extendedCapabilities"></a>   | /wms:WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities[1]