# Clean Water (open data initiative)
  
### Labs

Endpoint: https://mmvk4falrj.execute-api.us-west-2.amazonaws.com/v1/history/lab/{XX}

Surfrider groups testing locations around "labs", which are closely tied to the organization's chapter network. Lab IDs can be found at bwtf.surfrider.org, and chosing a location from the navigation dropdown menu. The lab ID will be the first number appended to the URL.

Example: Selecting New Hampshire, the url becomes https://bwtf.surfrider.org/explore/15, and the Lab ID would be "15".

### Sites

Endpoint: https://mmvk4falrj.execute-api.us-west-2.amazonaws.com/v1/history/site/{XX}
Sites represent a specific location where tests are conducted over time by volunteers from a particular lab. Find a site you are interested in at bwtf.surfrider.org, and the site ID will be the last number in the URL 

Example: Sawyers Beach: Mid Access in New Hampshire. The URL to see this on our web app is https://bwtf.surfrider.org/explore/65/913, and the site ID is "913"

### Samples
Endpoint: https://mmvk4falrj.execute-api.us-west-2.amazonaws.com/v1/history/sample?guid={xx}

This endpoint is used to retrieve information about a particular sample after you have already found it with one of the other API endpoints. This endpoint is basically just to retrieve data about a sample, if for example, an update was pubslished.

## Retrieving data from the API
  
Endpoints that return multiple records are limited too 100 results from our database in each request. Those results will get split into unique samples to comply with the Rec Water Quality Data Standard. See notes on How Surfrider records data. When there are more than 100 results available from the database, the HTTP response will contain a 'Link' header, with the formatted URL to retrieve the next set of results.

Example:

`GET https://mmvk4falrj.execute-api.us-west-2.amazonaws.com/v1/history/lab/51`

`content-length	73401`  
`content-type	application/json`  
`date	Mon, 21 Sep 2020 22:07:49 GMT`  
`link	<https://mmvk4falrj.execute-api.us-west-2.amazonaws.com/v1/history/lab/51?offset="eyJjb2xsZWN0aW9uVGltZSI6eyJTIjoiMjAxOS0xMC0wMVQwMzozMDowMC4wMDBaIn0sInB1YmxpY2F0aW9uVGltZSI6eyJTIjoiMjAyMC0wMy0wOVQxODo0ODoyNy4wMDBaIn0sImd1aWQiOnsiUyI6IjU1MzExMTI4NyJ9LCJsYWIiOnsiTiI6IjUxIn19">; rel="next"` 

## How Surfrider records data
- To Come -
