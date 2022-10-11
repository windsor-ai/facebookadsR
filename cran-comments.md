## R CMD check results

0 errors | 0 warnings | 1 note

* This is a new release.

## Second submission

URLs modified as required:

 Found the following (possibly) invalid URLs:
     URL: https://www.windsor.ai/ (moved to https://windsor.ai/)
       From: man/my_facebookads_data.Rd
             inst/doc/tutorial.html
       Status: 301
       Message: Moved Permanently
     URL: https://www.windsor.ai/api-fields/ (moved to
https://windsor.ai/api-fields/)
       From: DESCRIPTION
       Status: 301
       Message: Moved Permanently
       
Title modified as requierd:

   The Title field should be in title case. Current version is:
   'Access to facebook Ads via the 'Windsor.ai' API'
   In title case that is:
   'Access to Facebook Ads via the 'Windsor.ai' API'

## Third submission

URLs modified as required:

   Found the following (possibly) invalid URLs:
     URL: https://www.windsor.ai/ (moved to https://windsor.ai/)
       From: man/my_facebookads_data.Rd
             inst/doc/tutorial.html
             README.md
       Status: 301
       Message: Moved Permanently
     URL: https://www.windsor.ai/api-fields/ (moved to
https://windsor.ai/api-fields/)
       From: README.md
       Status: 301
       Message: Moved Permanently
       
## Fourth submission

0 errors ✔ | 0 warnings ✔ | 0 notes ✔

Code in @examples in R/fetch_facebookads changed so it provides an example, but note that the API key cannot be provided to users. In response to:

  Unexecutable code in man/fetch_facebookads.Rd:
  fetch_facebookads <- (api_key = "your api key",
  date_from = "2022-10-01",
  date_to = "2022-10-02",
  fields = c("campaign", "clicks",
  "spend", "impressions", "date"))
    
    
print() has been changed to warning() in R/fetch_facebookads. In response to:

  You write information messages to the console that cannot be easily
  suppressed. It is more R like to generate objects that can be used to
  extract the information a user is interested in, and then print() that
  object.
  Instead of print()/cat() rather use message()/warning()  or
  if(verbose)cat(..) (or maybe stop()) if you really have to write text to
  the console.
  (except for print, summary, interactive functions)
  e.g.: R/fetch_facebookads.R
