#################################################################
L2 tex to rst
#################################################################

Overview

========



The following note accompanies the JPL GRACE-FO Level-2 products,

version 6.3. It replaces any preceding release notes associated with the

version 6.3 product release. GRACE-FO RL06.3 is an updated version of

the initial GRACE-FO RL06 and GRACE-FO RL06.1 Level-2 data products.

RL06.1 differed from RL06 only in the Level-1B accelerometer transplant

data that was used for the GF2 satellite: Level-2 RL06.1 used ACH1B

RL04, which replaced ACT1B RL04 that was used for Level-2 RL06.

Similarly, RL06.3 differs from RL06.1 in the Level-1B accelerometer data

used for GF2, but *only* for months in 2023 and 2024 in which both

satellites are in nadir pointing with wide dead band (WDB) attitude

control to minimize the frequency of AOCS thruster firings and mitigate

small thruster leaks. For all other months within the mission, RL06.3 is

identical to RL06.1 within a change of filename and header information,

with the exception of March 2023 and June 2023, where some improvements

to data editing were made. For the WDB months, the accelerometer data

product used is that distributed within new \*.ACX2.tgz bundles,

improved through inclusion of updated modeling to account for large

attitude deviations and their effect on solar radiation pressure, drag,

and winds. All GRACE-FO RL06.3 Level-2 products are fully compatible

with the GRACE RL06 Level-2 fields. For each month, there are typically

6 available products, as listed below where **YYYY** corresponds to a 4

digit year and **DDD** corresponds to a 3 digit day of year (for details

see the Level-2 User Handbook :raw-latex:`\citep{L2User}`).



.. container:: description



   The average of the ‘atm’ coefficients from the AOD1B RL06 product,

   for degree/order 180, over the same time span as the computed monthly

   solution. While the file contains values for degrees 0 and 1, these

   harmonic coefficients are not used in the JPL Level-2 data

   processing. Note that the averaging is computed over entire days,

   regardless of whether the full day (as opposed to a partial day) was

   included in the Level-2 data processing. For further details, see the

   RL06 AOD1B Product Description Document :raw-latex:`\citep{AOD}`.



   The average of the ‘ocn’ coefficients from the AOD1B RL06 product,

   for degree/order 180, over the same time span as the computed monthly

   solution. While the file contains values for degrees 0 and 1, these

   harmonic coefficients are not used in the JPL Level-2 data

   processing. Note that the averaging is computed over entire days,

   regardless of whether the full day (as opposed to a partial day) was

   included in the Level-2 data processing. For further details, see the

   RL06 AOD1B Product Description Document :raw-latex:`\citep{AOD}`.



   The average of the ‘glo’ coefficients from the AOD1B RL06 product,

   for degree/order 180, over the same time span as the computed monthly

   solution. These harmonic coefficients are modeled in the background

   during Level-2 data processing. While the file contains values for

   degrees 0 and 1, these harmonic coefficients are not used in the JPL

   Level-2 data processing. Note that the averaging is computed over

   entire days, regardless of whether the full day (as opposed to a

   partial day) was included in the Level-2 data processing. For further

   details, see the RL06 AOD1B Product Description Document

   :raw-latex:`\citep{AOD}`.



   The average of the ‘oba’ coefficients from the AOD1B RL06 product,

   for degree/order 180, over the same time span as the computed monthly

   solution. While the file contains values for degrees 0 and 1, these

   harmonic coefficients are not used in the JPL Level-2 data

   processing. Note that the averaging is computed over entire days,

   regardless of whether the full day (as opposed to a partial day) was

   included in the Level-2 data processing. For further details, see the

   RL06 AOD1B Product Description Document :raw-latex:`\citep{AOD}`.



   The unconstrained monthly gravity field solution, computed out to

   degree/order 60.



   The unconstrained monthly gravity field solution, computed out to

   degree/order 96. Note that due to satellite ground track coverage,

   this solution may not always be published.



General Usage Notes

===================



For typical months, those where satellite ground track coverage is

sufficient, 60x60 (BA01) and 96x96 (BB01) solutions are provided. It is

left to the user’s discretion which solution best suits their particular

application. Additionally, it is suggested that a suitable smoothing

technique is applied, examples of which are available in the literature.

The uncertainties provided with the gravity field solutions have NOT

been calibrated and represent only the formal uncertainties.



Geocenter

---------



Consistent with GRACE, GRACE-FO is not sensitive to degree 1 harmonics

(geocenter). GRACE/GRACE-FO Technical Note TN-13[a,b,c] contains

geocenter estimates using the methods of :raw-latex:`\citet{Swenson}`

and :raw-latex:`\citet{Sun}`, and is updated in synch with Level-2

monthly releases. These have been reprocessed for the entire GRACE and

GRACE-FO time span to be consistent with the below-mentioned TN-14, so

users need to replace the entire TN-13 time series. It is recommended to

augment the GRACE and GRACE-FO geocenter with this product for surface

mass change estimation.



:math:`C_{2,0}`

---------------



Consistent with the GRACE SDS recommendations, GRACE-FO SDS recommends

the replacement of the native GRACE-FO :math:`C_{2,0}` coefficient with

that from SLR. Note that GRACE Technical Note TN-11 will no longer be

updated; it is replaced by GRACE/GRACE-FO Technical Note TN-14.

GRACE/GRACE-FO Technical Note TN-14 is now provided and contains both

:math:`C_{2,0}` and :math:`C_{3,0}` estimates derived from SLR and using

Level-2 RL06 standards, updated in synch with Level-2 monthly releases.

It is recommended to replace/substitute the native GRACE and GRACE-FO

:math:`C_{2,0}` coefficients with this product

:raw-latex:`\citep{LoomisC20}` for all months (04/2002 – current).



:math:`C_{3,0}`

---------------



The GRACE-FO SDS has determined that the :math:`C_{3,0}` coefficient in

GRACE-FO shows comparatively more variability relative to the long-term

climatology derived from the GRACE :math:`C_{3,0}` coefficient.

Therefore, SDS recommends that users assess the impact on regional mass

budgets of substituting the GRACE-FO :math:`C_{3,0}` coefficient with

one derived from SLR (similar to the :math:`C_{2,0}` approach).

GRACE/GRACE-FO Technical Note TN-14 is now provided and contains both

:math:`C_{2,0}` and :math:`C_{3,0}` estimates derived from SLR and using

Level-2 RL06 standards, updated in synch with Level-2 monthly releases.

It is recommended to replace/substitute the native GRACE and GRACE-FO

:math:`C_{3,0}` coefficients with this product

:raw-latex:`\citep{LoomisC30}` from 08/2016 onwards (08/2016 – current).



Feedback is Requested

---------------------



The GRACE-FO project SDS is looking for feedback from the Science Team

and wider community on the impact of :math:`C_{2,0}` and :math:`C_{3,0}`

replacements, either from these or other candidate SLR time series, on

regional mass balances to support the project in further improving the

handling of low-degree harmonics in GRACE and GRACE-FO data processing.



Gravity Field Solutions

=======================



Gravity field solutions are outlined in Table `1 <#tab:RL06-GSM>`__.

Each solution gives a general GSM filename (with a Linux glob string

inserted for the solution mnemonic), the first date included in the

solution, the last date included in the solution, the total number of

days included in the solution (accounting for any days that were

skipped), the spherical harmonic solution sizes available, and comments

associated with each solution (for solution specific annotations).

Additionally, for further details on filenames, formats, and a more

complete overview of the processing see the Level-2 User Handbook

:raw-latex:`\citep{L2User}` and Processing Standards Document

:raw-latex:`\citep{JPL-Process}`.



.. container:: landscape



   .. container::

      :name: tab:RL06-GSM



      .. table:: Overview of gravity field solutions (GSM filenames are

      given using Linux glob strings).



         +----------+----------+----------+----------+----------+----------+

         | *        | **Span   | **Span   | **       | **Degree | **Co     |

         | *Gravity | Start**  | End**    | Number** | /Order** | mments** |

         | Field    |          |          |          |          |          |

         | So       |          |          |          |          |          |

         | lution** |          |          |          |          |          |

         +----------+----------+----------+----------+----------+----------+

         |          |          |          | **of     |          |          |

         |          |          |          | Days**   |          |          |

         +----------+----------+----------+----------+----------+----------+

         | *        | **Span   | **Span   | **       | **Degree | **Co     |

         | *Gravity | Start**  | End**    | Number** | /Order** | mments** |

         | Field    |          |          |          |          |          |

         | So       |          |          |          |          |          |

         | lution** |          |          |          |          |          |

         +----------+----------+----------+----------+----------+----------+

         |          |          |          | **of     |          |          |

         |          |          |          | Days**   |          |          |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 29       | 60x60,   | `[li     |

         | -2_20181 | 18-06-01 | 18-06-30 |          | 96x96    | st:param |

         | 52-20181 |          |          |          |          | -2emp70] |

         | 81_GRFO_ |          |          |          |          |  <#list: |

         | JPLEM\_? |          |          |          |          | param-2e |

         | ???_0603 |          |          |          |          | mp70>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 18       | 60x60,   | `[lis    |

         | -2_20181 | 18-07-01 | 18-07-18 |          | 96x96    | t:param- |

         | 82-20181 |          |          |          |          | 2emp85]  |

         | 99_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 19       | 60x60,   | `[lis    |

         | -2_20182 | 18-10-22 | 18-11-09 |          | 96x96    | t:param- |

         | 95-20183 |          |          |          |          | 2emp85]  |

         | 13_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20183 | 18-11-01 | 18-11-30 |          | 96x96    | t:param- |

         | 05-20183 |          |          |          |          | 2emp85]  |

         | 34_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20183 | 18-12-01 | 18-12-31 |          | 96x96    | t:param- |

         | 35-20183 |          |          |          |          | 2emp85]  |

         | 65_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20190 | 19-01-01 | 19-01-31 |          | 96x96    | t:param- |

         | 01-20190 |          |          |          |          | 2emp85]  |

         | 31_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 25       | 60x60,   | `[lis    |

         | -2_20190 | 19-01-26 | 19-03-04 |          | 96x96    | t:param- |

         | 26-20190 |          |          |          |          | 2emp85]  |

         | 63_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20190 | 19-03-01 | 19-03-31 |          | 96x96    | t:param- |

         | 60-20190 |          |          |          |          | 2emp85]  |

         | 90_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20190 | 19-04-01 | 19-04-30 |          | 96x96    | t:param- |

         | 91-20191 |          |          |          |          | 2emp85]  |

         | 20_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20191 | 19-05-01 | 19-05-31 |          | 96x96    | t:param- |

         | 21-20191 |          |          |          |          | 2emp85]  |

         | 51_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20191 | 19-06-01 | 19-06-30 |          | 96x96    | t:param- |

         | 52-20191 |          |          |          |          | 2emp85]  |

         | 81_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20191 | 19-07-01 | 19-07-31 |          | 96x96    | t:param- |

         | 82-20192 |          |          |          |          | 2emp85]  |

         | 12_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20192 | 19-08-01 | 19-08-31 |          | 96x96    | t:param- |

         | 13-20192 |          |          |          |          | 2emp85]  |

         | 43_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20192 | 19-09-01 | 19-09-30 |          | 96x96    | t:param- |

         | 44-20192 |          |          |          |          | 2emp85]  |

         | 73_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20192 | 19-10-01 | 19-10-31 |          | 96x96    | t:param- |

         | 74-20193 |          |          |          |          | 2emp85]  |

         | 04_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20193 | 19-11-01 | 19-11-30 |          | 96x96    | t:param- |

         | 05-20193 |          |          |          |          | 2emp85]  |

         | 34_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20193 | 19-12-01 | 19-12-31 |          | 96x96    | t:param- |

         | 35-20193 |          |          |          |          | 2emp85]  |

         | 65_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 26       | 60x60,   | `[lis    |

         | -2_20200 | 20-01-01 | 20-01-31 |          | 96x96    | t:param- |

         | 01-20200 |          |          |          |          | 2emp85]  |

         | 31_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 23       | 60x60,   | `[lis    |

         | -2_20200 | 20-02-01 | 20-02-29 |          | 96x96    | t:param- |

         | 32-20200 |          |          |          |          | 2emp85]  |

         | 60_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20200 | 20-03-01 | 20-03-31 |          | 96x96    | t:param- |

         | 61-20200 |          |          |          |          | 2emp85]  |

         | 91_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20200 | 20-04-01 | 20-04-30 |          | 96x96    | t:param- |

         | 92-20201 |          |          |          |          | 2emp85]  |

         | 21_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20201 | 20-05-01 | 20-05-31 |          | 96x96    | t:param- |

         | 22-20201 |          |          |          |          | 2emp85]  |

         | 52_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20201 | 20-06-01 | 20-06-30 |          | 96x96    | t:param- |

         | 53-20201 |          |          |          |          | 2emp85]  |

         | 82_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20201 | 20-07-01 | 20-07-31 |          | 96x96    | t:param- |

         | 83-20202 |          |          |          |          | 2emp85]  |

         | 13_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20202 | 20-08-01 | 20-08-31 |          | 96x96    | t:param- |

         | 14-20202 |          |          |          |          | 2emp85]  |

         | 44_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20202 | 20-09-01 | 20-09-30 |          | 96x96    | t:param- |

         | 45-20202 |          |          |          |          | 2emp85]  |

         | 74_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20202 | 20-10-01 | 20-10-31 |          | 96x96    | t:param- |

         | 75-20203 |          |          |          |          | 2emp85]  |

         | 05_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20203 | 20-11-01 | 20-11-30 |          | 96x96    | t:param- |

         | 06-20203 |          |          |          |          | 2emp85]  |

         | 35_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20203 | 20-12-01 | 20-12-31 |          | 96x96    | t:param- |

         | 36-20203 |          |          |          |          | 2emp85]  |

         | 66_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20210 | 21-01-01 | 21-01-31 |          | 96x96    | t:param- |

         | 01-20210 |          |          |          |          | 2emp85]  |

         | 31_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 28       | 60x60,   | `[lis    |

         | -2_20210 | 21-02-01 | 21-02-28 |          | 96x96    | t:param- |

         | 32-20210 |          |          |          |          | 2emp85]  |

         | 59_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20210 | 21-03-01 | 21-03-31 |          | 96x96    | t:param- |

         | 60-20210 |          |          |          |          | 2emp85]  |

         | 90_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20210 | 21-04-01 | 21-04-30 |          | 96x96    | t:param- |

         | 91-20211 |          |          |          |          | 2emp85]  |

         | 20_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20211 | 21-05-01 | 21-05-31 |          | 96x96    | t:param- |

         | 21-20211 |          |          |          |          | 2emp85]  |

         | 51_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20211 | 21-06-01 | 21-06-30 |          | 96x96    | t:param- |

         | 52-20211 |          |          |          |          | 2emp70]  |

         | 81_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[list   |

         |          |          |          |          |          | :nadir]  |

         |          |          |          |          |          | <#list:n |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20211 | 21-07-01 | 21-07-31 |          | 96x96    | t:param- |

         | 82-20212 |          |          |          |          | 2emp70]  |

         | 12_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[list   |

         |          |          |          |          |          | :nadir]  |

         |          |          |          |          |          | <#list:n |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20212 | 21-08-01 | 21-08-31 |          | 96x96    | t:param- |

         | 13-20212 |          |          |          |          | 2emp70]  |

         | 43_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[list   |

         |          |          |          |          |          | :nadir]  |

         |          |          |          |          |          | <#list:n |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20212 | 21-09-01 | 21-09-30 |          | 96x96    | t:param- |

         | 44-20212 |          |          |          |          | 2emp70]  |

         | 73_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[list   |

         |          |          |          |          |          | :nadir]  |

         |          |          |          |          |          | <#list:n |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20212 | 21-10-01 | 21-10-31 |          | 96x96    | t:param- |

         | 74-20213 |          |          |          |          | 2emp70]  |

         | 04_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[list   |

         |          |          |          |          |          | :nadir]  |

         |          |          |          |          |          | <#list:n |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20213 | 21-11-01 | 21-11-30 |          | 96x96    | t:param- |

         | 05-20213 |          |          |          |          | 2emp70]  |

         | 34_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[list   |

         |          |          |          |          |          | :nadir]  |

         |          |          |          |          |          | <#list:n |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20213 | 21-12-01 | 21-12-31 |          | 96x96    | t:param- |

         | 35-20213 |          |          |          |          | 2emp70]  |

         | 65_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[list   |

         |          |          |          |          |          | :nadir]  |

         |          |          |          |          |          | <#list:n |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20220 | 22-01-01 | 22-01-31 |          | 96x96    | t:param- |

         | 01-20220 |          |          |          |          | 2emp70]  |

         | 31_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[list   |

         |          |          |          |          |          | :nadir]  |

         |          |          |          |          |          | <#list:n |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 28       | 60x60,   | `[lis    |

         | -2_20220 | 22-02-01 | 22-02-28 |          | 96x96    | t:param- |

         | 32-20220 |          |          |          |          | 2emp70]  |

         | 59_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[list   |

         |          |          |          |          |          | :nadir]  |

         |          |          |          |          |          | <#list:n |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20220 | 22-03-01 | 22-03-31 |          | 96x96    | t:param- |

         | 60-20220 |          |          |          |          | 2emp85]  |

         | 90_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20220 | 22-04-01 | 22-04-30 |          | 96x96    | t:param- |

         | 91-20221 |          |          |          |          | 2emp85]  |

         | 20_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20221 | 22-05-01 | 22-05-31 |          | 96x96    | t:param- |

         | 21-20221 |          |          |          |          | 2emp85]  |

         | 51_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20221 | 22-06-01 | 22-06-30 |          | 96x96    | t:param- |

         | 52-20221 |          |          |          |          | 2emp85]  |

         | 81_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20221 | 22-07-01 | 22-07-31 |          | 96x96    | t:param- |

         | 82-20222 |          |          |          |          | 2emp85]  |

         | 12_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20222 | 22-08-01 | 22-08-31 |          | 96x96    | t:param- |

         | 13-20222 |          |          |          |          | 2emp85]  |

         | 43_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20222 | 22-09-01 | 22-09-30 |          | 96x96    | t:param- |

         | 44-20222 |          |          |          |          | 2emp85]  |

         | 73_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:aocsT |

         |          |          |          |          |          | est] <#l |

         |          |          |          |          |          | ist:aocs |

         |          |          |          |          |          | Test>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20222 | 22-10-01 | 22-10-31 |          | 96x96    | t:param- |

         | 74-20223 |          |          |          |          | 2emp85]  |

         | 04_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20223 | 22-11-01 | 22-11-30 |          | 96x96    | t:param- |

         | 05-20223 |          |          |          |          | 2emp85]  |

         | 34_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20223 | 22-12-01 | 22-12-31 |          | 96x96    | t:param- |

         | 35-20223 |          |          |          |          | 2emp85]  |

         | 65_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p85>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20230 | 23-01-01 | 23-01-31 |          | 96x96    | t:param- |

         | 01-20230 |          |          |          |          | 2emp70]  |

         | 31_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 28       | 60x60,   | `[lis    |

         | -2_20230 | 23-02-01 | 23-02-28 |          | 96x96    | t:param- |

         | 32-20230 |          |          |          |          | 2emp70]  |

         | 59_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20230 | 23-03-01 | 23-03-31 |          | 96x96    | t:param- |

         | 60-20230 |          |          |          |          | 2emp86]  |

         | 90_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p86>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[       |

         |          |          |          |          |          | list:76- |

         |          |          |          |          |          | 5-repeat |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :76-5-re |

         |          |          |          |          |          | peat>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20230 | 23-04-01 | 23-04-30 |          | 96x96    | t:param- |

         | 91-20231 |          |          |          |          | 2emp86]  |

         | 20_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p86>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[       |

         |          |          |          |          |          | list:76- |

         |          |          |          |          |          | 5-repeat |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :76-5-re |

         |          |          |          |          |          | peat>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20231 | 23-05-01 | 23-05-31 |          | 96x96    | t:param- |

         | 21-20231 |          |          |          |          | 2emp86]  |

         | 51_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p86>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant] <# |

         |          |          |          |          |          | list:acc |

         |          |          |          |          |          | -transpl |

         |          |          |          |          |          | ant>`__, |

         |          |          |          |          |          | `[       |

         |          |          |          |          |          | list:76- |

         |          |          |          |          |          | 5-repeat |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :76-5-re |

         |          |          |          |          |          | peat>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20231 | 23-06-01 | 23-06-30 |          | 96x96    | t:param- |

         | 52-20231 |          |          |          |          | 2emp86]  |

         | 81_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p86>`__, |

         |          |          |          |          |          | `[list:a |

         |          |          |          |          |          | cc-trans |

         |          |          |          |          |          | plant] < |

         |          |          |          |          |          | #list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20231 | 23-07-01 | 23-07-31 |          | 96x96    | t:param- |

         | 82-20232 |          |          |          |          | 2emp70]  |

         | 12_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20232 | 23-08-01 | 23-08-31 |          | 96x96    | t:param- |

         | 13-20232 |          |          |          |          | 2emp70]  |

         | 43_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20232 | 23-09-01 | 23-09-30 |          | 96x96    | t:param- |

         | 44-20232 |          |          |          |          | 2emp70]  |

         | 73_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20232 | 23-10-01 | 23-10-31 |          | 96x96    | t:param- |

         | 74-20233 |          |          |          |          | 2emp70]  |

         | 04_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20233 | 23-11-01 | 23-11-30 |          | 96x96    | t:param- |

         | 05-20233 |          |          |          |          | 2emp70]  |

         | 34_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20233 | 23-12-01 | 23-12-31 |          | 96x96    | t:param- |

         | 35-20233 |          |          |          |          | 2emp70]  |

         | 65_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20240 | 24-01-01 | 24-01-31 |          | 96x96    | t:param- |

         | 01-20240 |          |          |          |          | 2emp70]  |

         | 31_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 29       | 60x60,   | `[lis    |

         | -2_20240 | 24-02-01 | 24-02-29 |          | 96x96    | t:param- |

         | 32-20240 |          |          |          |          | 2emp70]  |

         | 60_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20240 | 24-03-01 | 24-03-31 |          | 96x96    | t:param- |

         | 61-20240 |          |          |          |          | 2emp70]  |

         | 91_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20240 | 24-04-01 | 24-04-30 |          | 96x96    | t:param- |

         | 92-20241 |          |          |          |          | 2emp70]  |

         | 21_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20241 | 24-05-01 | 24-05-31 |          | 96x96    | t:param- |

         | 22-20241 |          |          |          |          | 2emp70]  |

         | 52_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20241 | 24-06-01 | 24-06-30 |          | 96x96    | t:param- |

         | 53-20241 |          |          |          |          | 2emp70]  |

         | 82_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20241 | 24-07-01 | 24-07-31 |          | 96x96    | t:param- |

         | 83-20242 |          |          |          |          | 2emp70]  |

         | 13_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20242 | 24-08-01 | 24-08-31 |          | 96x96    | t:param- |

         | 14-20242 |          |          |          |          | 2emp70]  |

         | 44_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20242 | 24-09-01 | 24-09-30 |          | 96x96    | t:param- |

         | 45-20242 |          |          |          |          | 2emp70]  |

         | 74_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[lis    |

         |          |          |          |          |          | t:allnad |

         |          |          |          |          |          | ir] <#li |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir>`__, |

         |          |          |          |          |          | `[       |

         |          |          |          |          |          | list:61- |

         |          |          |          |          |          | 4-repeat |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :61-4-re |

         |          |          |          |          |          | peat>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 29       | 60x60,   | `[lis    |

         | -2_20242 | 24-10-01 | 24-10-31 |          | 96x96    | t:param- |

         | 75-20243 |          |          |          |          | 2emp70]  |

         | 05_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[lis    |

         |          |          |          |          |          | t:allnad |

         |          |          |          |          |          | ir] <#li |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir>`__, |

         |          |          |          |          |          | `[       |

         |          |          |          |          |          | list:61- |

         |          |          |          |          |          | 4-repeat |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :61-4-re |

         |          |          |          |          |          | peat>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 30       | 60x60,   | `[lis    |

         | -2_20243 | 24-11-01 | 24-11-30 |          | 96x96    | t:param- |

         | 06-20243 |          |          |          |          | 2emp70]  |

         | 35_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20243 | 24-12-01 | 24-12-31 |          | 96x96    | t:param- |

         | 36-20243 |          |          |          |          | 2emp70]  |

         | 66_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20250 | 25-01-01 | 25-01-31 |          | 96x96    | t:param- |

         | 01-20250 |          |          |          |          | 2emp70]  |

         | 31_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 28       | 60x60,   | `[lis    |

         | -2_20250 | 25-02-01 | 25-02-28 |          | 96x96    | t:param- |

         | 32-20250 |          |          |          |          | 2emp70]  |

         | 59_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         | GSM      | 20       | 20       | 31       | 60x60,   | `[lis    |

         | -2_20250 | 25-03-01 | 25-03-31 |          | 96x96    | t:param- |

         | 60-20250 |          |          |          |          | 2emp70]  |

         | 90_GRFO_ |          |          |          |          | <#list:p |

         | JPLEM\_? |          |          |          |          | aram-2em |

         | ???_0603 |          |          |          |          | p70>`__, |

         |          |          |          |          |          | `        |

         |          |          |          |          |          | [list:ac |

         |          |          |          |          |          | c-transp |

         |          |          |          |          |          | lant-wdb |

         |          |          |          |          |          | ] <#list |

         |          |          |          |          |          | :acc-tra |

         |          |          |          |          |          | nsplant- |

         |          |          |          |          |          | wdb>`__, |

         |          |          |          |          |          | `[li     |

         |          |          |          |          |          | st:allna |

         |          |          |          |          |          | dir] <#l |

         |          |          |          |          |          | ist:alln |

         |          |          |          |          |          | adir>`__ |

         +----------+----------+----------+----------+----------+----------+

         |          |          |          |          |          |          |

         +----------+----------+----------+----------+----------+----------+



Solution Comments

=================



#. The solution is parameterized using nominally 5 second KBR range-rate

   data and nominally 30 second GRACE-FO GPS data. The solved for

   local/common parameters include the satellite initial states (solved

   per arc - nominally 1 day), accelerometer biases/rates in the

   GRACE-FO SRF XYZ directions (solved per arc in the XZ directions and

   every 3 hours in the Y direction), a full accelerometer scale matrix

   (9 parameters solved per arc), GPS phase biases (solved per GPS

   satellite pass), and empirical biases/drifts/once per revolution

   sinusoids for the KBR range-rate data (solved every 90 minutes). The

   solved for global parameters include the spherical harmonic

   coefficients.



#. The solution is parameterized using nominally 5 second KBR range-rate

   data and nominally 30 second GRACE-FO GPS data. The solved for

   local/common parameters include the satellite initial states (solved

   per arc - nominally 1 day), accelerometer biases/rates in the

   GRACE-FO SRF XYZ directions (solved per arc in the XZ directions and

   every 3 hours in the Y direction), GPS phase biases (solved per GPS

   satellite pass), and empirical biases/drifts/once per revolution

   sinusoids for the KBR range-rate data (solved every 90 minutes). The

   solved for global parameters include a full accelerometer scale

   matrix (9 parameters) and the spherical harmonic coefficients.



#. The solution is parameterized using nominally 5 second KBR range-rate

   data and nominally 30 second GRACE-FO GPS data. The solved for

   local/common parameters include the satellite initial states (solved

   per arc - nominally 1 day), accelerometer biases/rates in the

   GRACE-FO SRF XYZ directions (solved per arc in the XZ directions and

   every 3 hours in the Y direction), GPS phase biases (solved per GPS

   satellite pass), and empirical biases/drifts/once per revolution

   sinusoids for the KBR range-rate data (solved every 90 minutes).

   Additionally, bias and 1 cycle per revolution empirical accelerations

   in the along and cross directions are solved for GRACE-D only (solved

   every 90 minutes). The solved for global parameters include a full

   accelerometer scale matrix (9 parameters) and the spherical harmonic

   coefficients.



#. Accelerometer data for GRACE-D is derived using the accelerometer

   data from GRACE-C (accelerometer transplant) and augmented with

   corrections utilizing filtered/preprocessed GRACE-D accelerometer

   data.



#. For these WDB months, accelerometer data for GRACE-D is derived using

   the accelerometer data from GRACE-C (accelerometer transplant)

   augmented with corrections utilizing filtered/preprocessed GRACE-D

   accelerometer data. This includes updated modeling to account for

   large attitude deviations and their effect on solar radiation

   pressure, drag, and winds.



#. We do not do estimation of a global full accelerometer scale matrix

   (9 parameters) as that would unacceptably degrade this monthly

   solution due to off-nominal (nadir) satellite pointing on each of the

   following days: 2021-06-01, 2021-06-02, 2021-06-07, 2021-06-08,

   2021-06-14, 2021-06-15, 2021-06-21, 2021-06-22, 2021-06-28,

   2021-06-29, 2021-07-05, 2021-07-06, 2021-07-12, 2021-07-13,

   2021-07-26, 2021-07-27, 2021-08-02, 2021-08-03, 2021-08-09,

   2021-08-10, 2021-08-16, 2021-08-17, 2021-08-30, 2021-08-31,

   2021-09-13, 2021-09-14, 2021-09-27, 2021-09-28, 2021-10-31,

   2021-11-01, 2021-12-20, 2021-12-21, 2021-12-27, 2021-12-28,

   2022-01-03, 2022-01-04, 2022-01-10, 2022-01-11, 2021-01-17,

   2022-01-18, 2022-01-24, 2022-01-25, 2022-01-31. 2022-02-01,

   2022-02-07, 2022-02-08, 2022-02-14, 2022-02-15, 2022-07-01 through

   2022-08-31, 2023-01-01 through 2023-02-28, and 2023-07-01 onward.



#. The entire solution period has off-nominal (nadir) satellite

   pointing.



#. A span of data from approximately 0600 on 2022-09-27 to 0600

   2022-09-28 is excluded due to an AOCS parameter test where the

   spacecraft are in nadir pointing with much wider attitude control

   deadbands.



#. The GRACE-FO satellites are passing through a 76 revolution/5 day

   repeat ground track which peaks in 2023-04. This causes reduced

   observability of the spherical harmonic coefficients and solution

   analysis may require more aggressive than normal post-processing.



#. The GRACE-FO satellites are passing through a 61 revolution/4 day

   repeat ground track which peaks in 2024-09. This causes reduced

   observability of the spherical harmonic coefficients and solution

   analysis may require more aggressive than normal post-processing.

