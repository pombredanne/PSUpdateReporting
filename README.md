#PSUpdateReporting

##Purpose

Since Microsoft has created a new site for gathering security update
information, [MSRC](https://portal.msrc.microsoft.com/en-us),
it is slightly more accessible, but many of the methods used previously
(page scraping, etc) are no longer viable. However, administrators are
not without recourse. Microsoft has provided a 
[RESTful API](https://portal.msrc.microsoft.com/en-us/developer).

This PowerShell module makes use of the exposed API in order to retreive
update information. Once the information is gathered, it may be reported
on in a manner useful to the administrator with built-in functionality.

##Functions

Functions are broken down into the usual PowerShell verb-noun
results-based separations.

###Listing

####MSRCAPIKey-actions.ps1

* Get-APIKey

   Displays the API key setting previously set with Set-APIKey.

* Set-APIKey

   Sets the API key provided by the user as a parameter.  
   API key is available 
   [here](https://portal.msrc.microsoft.com/en-us/developer).

####Data-actions.ps1

* Receive-UpdateListing

   Uses API Key to pull information from MSRC, stores data temporarily.  
   Primary parameter is search scope.

* Save-UpdateReport

   Saves report data.  
   Parameters include FileType, Path.

##Testing

Basic pester-based testing is built-in.
