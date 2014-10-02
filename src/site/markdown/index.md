# Overview

This executable test suite is based on the following documents:

  * [OGC Web Coverage Service (WCS) Implementation Specification](http://www.opengeospatial.org/standards/wcs) (OGC-03-065r6)
  * [OGC Web Coverage Service (WCS) Implementation Specification Corrigendum (1.0.0)](http://www.opengeospatial.org/standards/wcs) (OGC-05-076)
  * [Test Requirements and Assertions](testreq.html)

The only difference in testing an implementation of the original WCS 1.0.0
spec (03-065r6) or the corrigendum (05-076) is the schemas used for
validation. Both are tested using test module wcs1-0-0:main in the abstract
test suite. When the test suite is started, the user can select which version
of the schemas is implemented.

The tests performed against an implementation are selected based on the
capabilities document for the WCS implementation. By omitting a request,
operation or capability from the capabilities document the tests for that
functionality will not be executed against the implementation. The test suite
makes a few basic assumptions about the WCS:

  * That there are at least two coverages provided by the tested server.
  * The first coverage offering should include all the tested features while the second coverage could be any thing.
  * The first coverage offering must take one of the 5 formats described in the WCS1.0.0 standard document as the first supported format.
  * The first coverage offering should have parameters defined in the axisDescription.
  * If the xml encoding is tested, the first coverage offering should have interpolation method defined.
  * If the server support time position, the first coverage offering should define time feature.

There is no standard MIME header definitions for the 5 required formats. Thus
the actual MIME header depends on the server. The assertion test will check
the results based on the first available format for the first coverage. A MIME
header value should be entered during session configuration.

The WCS spec allows servers to use an UpdateSequence value for maintaining
cache consistency. If the server advertises an UpdateSequence value then
values that are lexically higher and lower than the current updateSequence
value should be entered during session configuration.

Those values are required to test GetCoverage with parameter RESX and RESY.
The values depends on the crs provided by the first offering. Values for RESX
and RESY should be entered during session configuration.

### Manual Test Scopes

  * To verify that the server supports XML encoding, the checkbox labeled "Verify that the server supports XML encoding" should be checked during session configuration. 
  * To verify that the server supports axis description encoding, the checkbox labeled "Verify that the server supports range set axis" should be checked during session configuration. 

### Automated Test Scopes

The following test scopes will be tested automatically:

  * HTTP GET is a mandatory test
  * If HTTP POST appears in the capabilities document, HTTP POST will be tested.
  * If updateSequence appears in the capabilities document, updateSequence is tested.
  * If timePosition appears in the capabilities document, time is tested.

## What is tested

Only the protocol is tested.

  * GetCapabilities, GET KVP, POST KVP, and POST XML encodings
  * DescribeCoverage, GET KVP, POST KVP, and POST XML encodings
  * GetFeature, GET KVP, POST KVP, and POST XML encodings

Each encoding is optional except for the GetCapabilities GET KVP encoding. The
optional encodings are only tested when the GetCapabilities response indicates
that the encoding is supported.

The user is prompted for the end point URL of the server. If there is no
server at that location, the testing stops.

## What is not tested

* The coverage returned by a GetCoverage request

## Test data

There is no test data required for the WCS 1.0.0 executable test suite.

## Namespaces

There are two namespaces used by the WCS.
ogc: http://www.opengis.net/ogc
wcs: http://www.opengis.net/wcs

## Schemas

The schemas for the corrigendum are currently available online at
<http://schemas.opengis.net/wcs/1.0.0>.

## Abstract Test Suite

Details on the tests performed are available in the [abstract test
suite](wcs-1.0.0-ats.html).

## Release Notes

Release notes are available from the [relnotes.html](relnotes.html).
