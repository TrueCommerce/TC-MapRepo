This Git repository is used to store XBSP maps used by the Integration Gateway

The structure of this repository is to have remote branches titled

DEV
Q1
Q2
Q2
R1
S1
PROD

Under these branches will be a branch named for each tenant.  the branches
will be cleaned names based off of the Foundry Company Name.  A cleaned name
would have all non alpha-numeric characters stripped out and the resulting
name Pascal cased.  For example, "21st Century Health care, Inc." would become
"21stCenturyHealthCareInc"

The company name for the null tenant will be replaced "(null)" .

Each of these "Tenant" branches will consist of this readme.txt file, and the XBSPs
deployed for this tenant.

So in GIT/SourceTree you would see the following remote structure...

REMOTES
|
+--DEV
|  |
|  +--(null)
|  |
|  +--21stCenturyHealthCareInc
|  
+--PROD
|  |
|  +--(null)
|  |
|  +--21stCenturyHealthCareInc
|  
+--Q1
|  |
|  +--(null)
|  |
|  +--21stCenturyHealthCareInc
|  
+--Q2
|  |
|  +--(null)
|  |
|  +--21stCenturyHealthCareInc
|  
+--Q3
|  |
|  +--(null)
|  |
|  +--21stCenturyHealthCareInc
|  
+--R1
|  |
|  +--(null)
|  |
|  +--21stCenturyHealthCareInc
|  
+--S1
   |
   +--(null)
   |
   +--21stCenturyHealthCareInc

And each of the branches would have a file/folder structure similar to the following...

|
+--readme.txt
|
+--(null)
   |
   +--map1.xbsp
   |
   +--map2.xbsp

The purpose of the branch structure is to limit the number of files contained in each 
branch and isolate them by tenant.

As a rull these branches should never be pulled into another branch or pulled into the
master branch.


