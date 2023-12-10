# Document

# Overview

# Table fields

### Document Date

* The Date field shall allow the researcher to select a date which contains their best guess
* The Date field shall adhere to ISO 8601 for Dates:
    * YYYY-MM-DD
* This is actually set by the researcher themselves in their system settings. However all calculations are based on an ISO 8601 paradigm,

    #### DateUncertainty

    * There shall be three checkboxes with which the researcher can indicate uncertainty of either Year, Month or Day (date in month).

    #### DateObscured
    * A calculated field shall be superimposed on the Document Date field. This field shall exchange the digits of an uncertain component (as indicated by the checkboxes) for their letter component "Y/M/D".
        * For example the date 2012-12-5, with the checkboxes uncertain year, uncertain day shall be rendered as:
            * YYYY-12-DD
            


