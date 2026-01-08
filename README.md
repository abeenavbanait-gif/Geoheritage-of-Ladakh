Methodology
Article_Analysis


**Step_1 : Removal of Unwanted Items**
Web of Science Record
       Date of Export
       Hot Paper Status
       Highly Cited Status
       Pubmed Id
       Open Access Designations
       IDS Number
       Web of Science Index
       Number of Pages
       Early Access Date
       Book DOI
       Article Number
       Start Page
       End Page
       Meeting Abstract
       Special Issue
       Supplement
       Part Number
       Issue
       Volume
       Publication Date
       ISBN
       eISSN
       ISSN
Conference: Title, Date, Location, Sponser, and Host (5 columns) 
Document Type
       Book Series Subtitle
       Book Series Title
       Book Author Full Names
       Book Group Authors
       Book Editors
       Book Authors
       Cited References

**Step_2: Getting Countries from the affiliation address**
      Using a formula in numbers to extract Countries:
      TRIM(RIGHT(K2, LEN(K2) − SEARCH("@", SUBSTITUTE(K2, ",", "@", LEN(K2) − LEN(SUBSTITUTE(K2, ",", "",occurrence))),start-pos))) 
      Countries extracted from affiliation address column


**Step_3: Indian Papers segregated from the entire set**
      Total of 86 indian papers extracted
      Merge the sheet WoS into the sheet of Scopus
      De-duplicates are removed on the basis of UNIQUE ID Column: DOI
      Duplicates are identified using count if countif Function: =COUNTIF($B$2:B2,B2)
      This will create 1s and 2s in another column: DOI_check
      1s means first occurrence of that DOI (KEEP) and 2s means duplicate (REMOVE)
      Duplicates are then filtered out using Filter function of Numbers; Filter to keep only unique DOIs
      Click Column: DOI_check
      Add Filter → Number
      Condition → is equal to 1
      Now only one row per DOI remains visible.
      Rows with single doi occurence is colored Yellow and seperated into a new sheet: Updated_Database (Scopus+WoS)
      Authors column is set to ascending order to Identify WoS documents (Authors column of WoS sheet is filled with ‘J’ in merged database )
      So the ‘J’ are deleted and again Authors is set to Ascending order - Now we have seperated all WoS Documents (10 documents)
      Further 7 documents (Scopus: 5 and WoS: 2) added at last which don’t have any DOI 
      Final Outcome: Total No. of papers now increased to 131 papers with WoS: 12 and Scopus: 119

**Step_4: extraction of Ladakh related papers**

  Ladakh related papers were extracted from 131 collected papers from thier Titles, Abstracts and Keywords
  A total of 8 papers were extracted from the corpus of 131 geoheritage dedicated papers of Indian context
  Geosites are listed in tables, description and methodologies were extracted from the papers along with their coordinated
  A KML file was created using coordinates, and ploted using simple “Google My Maps” and a boundary shape file of Ladakh region is retrived from National Water Informatics Centre and ploted the spatial distribution.
  Papers were then analysed for:
  Geological framework explored
  Evaluation of the scientific, educational, and aesthetic value of sites listed.
  Priliminary assessment of the current threats to these listed sites









