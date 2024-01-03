# my-resume-github-actions

## draft unsorted!

Static  Website
Create a bucket with your website’s name (like devsom.co.uk) no http or www
Uncheck ‘Block all public access’
Confirm your acknowledgement then click ‘Create……..’
When it is ready, click on the name of your bucket and upload your .html, .css and .js files. 
Click ‘Properties’, Edit ‘Edit static website hosting’ and enable it then put index.html in the box.
Go to ‘Permissions’, Then at  the bottom, find Bucket policies and edit it. Find ‘Policy Generator’ 
At the ‘Select type of policy’ drop-down list, select ‘S3 policy’, Effect=Allow, Principle= *
In the ‘Actions’, find ‘GetObject’ In the box below, paste bucket ARN number with /* at the end.
Click “Add statement” Policy got created. At last click ‘Generate Policy” Copy the policy  and paste it back into the last page of the S3 and save.
Go back to Properties, At the ‘Static Website hosting’  you will find your website URL.
Website is ready but is not convenient for your readers as it is hosted on S3. Now what?
 Mapping your S3 hosted website with a domain name (This hosting will cost $0.50 a month)
Find ‘Route53’. Click ‘Create hosted zone’, and Enter your Domain name. (no http or www) 
Make sure type is ‘Public hosted…’ and click the ‘Create’ button. You’ll get the NS and SOA.
On the same  page, click ‘Public hosted zone’ and Leave it as ‘Simple routing’ Next.
On the next page find ‘Define simple record’, Leave it as “A” type.  
Select Alias
 to S3, Select your region, and find your S3 link in the box below. 
Click ‘Define simple record’ Click ‘create’ button in next page. You are done on Route53.
