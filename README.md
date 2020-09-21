# Clean Water (open data initiative)

## Endpoints

  - Labs: https://mmvk4falrj.execute-api.us-west-2.amazonaws.com/v1/history/lab/{XX}
  - Site: https://mmvk4falrj.execute-api.us-west-2.amazonaws.com/v1/history/site/{XX}
  - Sample: https://mmvk4falrj.execute-api.us-west-2.amazonaws.com/v1/history/sample?guid={xx}
  
## Retrieving data from the API
  
Endpoints that return multiple records are limited too 100 results from our database in each request. Those results will get split into unique samples to comply with the Rec Water Quality Data Standard. See notes on How Surfrider records data. When there are more than 100 results available from the database, the HTTP response will contain a 'Link' header, with the formatted URL to retrieve the next set of results.

Example:

`
content-length	73401  
content-type	application/json  
date	Mon, 21 Sep 2020 22:07:49 GMT  
link	<https://mmvk4falrj.execute-api.us-west-2.amazonaws.com/v1/history/lab/51?offset="eyJjb2xsZWN0aW9uVGltZSI6eyJTIjoiMjAxOS0xMC0wMVQwMzozMDowMC4wMDBaIn0sInB1YmxpY2F0aW9uVGltZSI6eyJTIjoiMjAyMC0wMy0wOVQxODo0ODoyNy4wMDBaIn0sImd1aWQiOnsiUyI6IjU1MzExMTI4NyJ9LCJsYWIiOnsiTiI6IjUxIn19">; rel="next"  
`

## How Surfrider records data
