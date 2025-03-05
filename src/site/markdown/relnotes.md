
# WCS 1.0.0 Test Suite Release Notes

## 1.20 (2025-03-05)

Attention: Java 17 and Tomcat 10.1 are required.

- [#64](https://github.com/opengeospatial/ets-wcs10/issues/64) - Migrate test suite to TEAM Engine 6 (Java 17)

## 1.19 (2024-05-28)
- [#61](https://github.com/opengeospatial/ets-wcs10/issues/61) - WCS 1.0.0 compliance test incorrectly reports my server has an invalid content type (te2 v1.18)

## 1.18 (2024-03-21)
- [#59](https://github.com/opengeospatial/ets-wcs10/issues/59) - Check why ETS on Beta is not completing Test wcs1-0-0:getcoverage_operations-getcoverage_request-parameter-get-kvp-3

## 1.17 (2024-01-31)
- [#56](https://github.com/opengeospatial/ets-wcs10/issues/56) - Invalid request produced by WCS 1.0.0 test wcs1-0-0:getcoverage_operations-getcoverage_response-encoding-supportedFormats
- [#58](https://github.com/opengeospatial/ets-wcs10/pull/58) - Set version of TEAM Engine dependency to 5.7 and upgrade xercesImpl to version 2.12.2

## 1.16 (2020-07-02)
- [#50](https://github.com/opengeospatial/ets-wcs10/issues/50) - invalid XML character in getcoverage_operations-getcoverage_request-parameter-post-kvp-3
- [#21](https://github.com/opengeospatial/ets-wcs10/issues/21) - Missing references of additional test cases
- [#46](https://github.com/opengeospatial/ets-wcs10/pull/46) - Updated teamengine version to 5.4
- [#44](https://github.com/opengeospatial/ets-wcs10/issues/44) - Incorrect validation of lonLatEnvelope srsName attribute
- [#45](https://github.com/opengeospatial/ets-wcs10/issues/45) - Internal Server Error because of invalid xml characters
- [#48](https://github.com/opengeospatial/ets-wcs10/issues/48) - wcs 1.0.0 compliance test getcoverage issue
- [#40](https://github.com/opengeospatial/ets-wcs10/issues/40) - getcoverage_operations-getcoverage_request-grid_size-post-xml-2 fails as concat() cannot be executed
- [#39](https://github.com/opengeospatial/ets-wcs10/issues/39) - Enable Docker support

## 1.15 (2018-05-18)
- Fix [#27](https://github.com/opengeospatial/ets-wcs10/issues/27) Update CTL with better information about conformance classes

## 1.14 (2018-02-27)
- Fix [#32](https://github.com/opengeospatial/ets-wcs10/issues/32) WCS VendorSpecificCapabilities Validation failure for GetCapabilities response
- Fix [#31](https://github.com/opengeospatial/ets-wcs10/issues/31) wcs1-0-0:getcoverage_operations-getcoverage_request-grid_size-post-xml-2 fails cause of unexpected Content-Type
- Fix [#30](https://github.com/opengeospatial/ets-wcs10/issues/30) Incorrect request from WCS Team Engine Test Case for DescribeCoverage
- Fix [#29](https://github.com/opengeospatial/ets-wcs10/issues/29) Incorrect request from WCS Team Engine Test Case for GetCoverage - "gml" namespace identifier missing

## 1.13 (2017-04-13)
- Fix [#24](https://github.com/opengeospatial/ets-wcs10/issues/24) Rename test getcoverage_operations-getcoverage_request-grid_size-get-xml-2
- Fix [#19](https://github.com/opengeospatial/ets-wcs10/issues/19) Question regarding Test wcs1-0-0:getcoverage_operations-getcoverage_request-grid_size-get-kvp-2

## 1.12 (2017-01-31)
- Fix [#15](https://github.com/opengeospatial/ets-wcs10/issues/15) Variable $VAR_WCS_DESCRIBE_COVERAGE_HTTP_POST_URL has not been declared in Test wcs1-0-0:getcoverage_operations-getcoverage_request-grid_size-get-xml-2

## 1.11 (2015-07-30)
- Update pom.xml to build with Maven 2 and minor edits
- Fix [#13](https://github.com/opengeospatial/ets-wcs10/issues/13) Replace DescribeCoverage HTTP GET with HTTP POST request

## 1.10 (2015-03-05)
* Update to new release scheme

## r9 (2014-11-19)

* [#2](https://github.com/opengeospatial/ets-wcs10/issues/2) - WCS Format Parameter on GetCoverage Post request
* [#10](https://github.com/opengeospatial/ets-wcs10/issues/10) - MIME type exception when a GetCoverage request is made without a specific grid size and without a grid resolution


## r8 (2014-10-02)

 * [#9](https://github.com/opengeospatial/ets-wcs10/issues/9) - request bbox issue - r7
 * [#7](https://github.com/opengeospatial/ets-wcs10/issues/7) - CITE tests will generate gml:pos with comma separated ordinates
 * [#5](https://github.com/opengeospatial/ets-wcs10/issues/5) - WCS tests work only if coverage names have no char that needs to be url encoded
 * [#4](https://github.com/opengeospatial/ets-wcs10/issues/4) - Exception tests do not work if higher versions of the WCS spec are also implemented in the same server


## r7 (2014-06-10)

  * Fix CITE-951: ServletException occurs when image returned instead of expected exception report.

## r6 (2014-02-28)

  * Fixed CITE-919: Added function wcs:coords-from-envelope to extract coordinates from gml:Envelope (wcs-functions.xml).
  * Fixed VAR_WCS_COVERAGE_1_POSITION_FIRST and VAR_WCS_COVERAGE_1_POSITION_SECOND variables to allow for multiple occurrences of gml:Envelope (in wcs:spatialDomain context).
  * Fixed CITE-778: Encode coverage names using XPath function encode-for-uri.
  * Fixed type restriction error in 1.0.0_c1/wcsCapabilities.xsd (AbstractDescriptionBaseType).

## r5 (2013-03-22)

  * correct wcs1-0-0:getcapabilities_operations-getcapabilities_request-post-xml-7 as reported in 776
  * removed "deprecated" notice in config.xml

## r4 (2013-02-08)

  * added note about required libs (resources/README.txt)

## r3 (2012-06-25)

  * added correct xlink schema
  * changed for new xlink policy

## r2 (2010-11-15)

  * fixed issue #23 and removed call to removed tests (issue #23)

## r1 (2010-05-13)

  * removed irrelevant testing of a none existing exception message

## r0 (2009-10-12)

  * Corrected time parameter on test getcoverage_operations-getcoverage_request-time-get-kvp-1 (Issue 307)
  * Added CRS parameter to test getcoverage_operations-getcoverage_request-time-get-kvp-2 (Issues 330, 309)
  * Added tests and bug fixes written for NSG that apply to the base WCS specification:

    1. Each HTTP GET URL prefix ends in either a '?' or a '&'
    2. The server handles encoded commas and spaces in list values correctly if any coverage names contain commas or spaces
    3. Service exception XML validates according to the Service Exception XML Schema
    4. N/A - NSG specific
    5. The version and updateSequence attributes are omitted from all of the three capabilities sections (Service, Capability, and ContentMetadata) element when the full Capabilities XML is retrieved.
    6. When a GetCoverage request is made with a BBOX inside the defined Bounding BOX, the server returns content.
    7. When a GetCoverage request is made with a BBOX partly contained in the defined Bounding BOX, the server returns content.
    8. For coverages with a temporal domain with time instants, a GetCoverage request with a temporalSubset that specifies a time instant returns content.
    9. For coverages with a temporal domain with time periods, a GetCoverage request with a temporalSubset that specifies a time period returns content.
    10. For coverages with at least one RectifiedGrid, each of the supportedCRSs is the same as the srsName of one of its RectifiedGrids
    11. If the describeCoverage provides a NativeCRSs element, a getcoverage request with this request succeeds without distortion or degradation of the coverage data.
    12. N/A - NSG specific
    13. SupportedInterpolations is absent, empty, or has a default attribute that specifies one of the child interpolation methods.
    14. For each of the advertised interpolation methods, the server returns content.
    15. When a request contains a BBOX in upper,lower instead of lower,upper format, the service returns an exception.
    16. If the only interpolation method supported is "none", a GetCoverage request that uses resolution parameters to request a coverage that is not at the native resolution returns an exception.
    17. If the only interpolation method supported is "none", a GetCoverage request that uses height and width parameters to request a coverage that is not at the native resolution returns an exception.
    18. A coverage request using RESX, RESY, RESZ and INTERPOLATION=none raises an exception.
    19. A coverage request using RESESPONSE_CRS and INTERPOLATION=none raises an exception.
    20. A coverage request that specifies aGML Rectified grid in its domain subset returns a valid coverage.
    21. A valid getCoverage response is returned for each supportedFormat
    22. If they exist, UPDATESEQUENCE values work with GetCapabilities requests. Test UPDATESEQUENCE parameters with GetCapabilities requests (same as WCS 1.1.1 tests)
    23. To return a coverage in multiple part files, the multi-part MIME encoding is used by the service.
    24. N/A - NSG specific
    25. Each coverage offering supports at least one of these: GeoTIFF, HDF-EOS, DTED, NITF, or GML

