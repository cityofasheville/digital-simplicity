# Treating Data Like a Strategic Asset
### By Eric Jackson

My recent post on [shared data systems](./shared-data-shared-systems-getting-everyone-page.md) in the City of Asheville, NC introduced the idea that adding a dataset to our management and reporting repository is also a chance to be more proactive about how we manage that dataset. It’s an opportunity to decide exactly how to represent and document the data, who should have access to it, and how we keep it up-to-date. This is obviously a good idea — it only remains to figure out how.

Not surprisingly, that how turns out to be a challenge. Fortuitously, the day after I published the post, open data leader [Andrew Nicklin](https://govex.jhu.edu/author/anicklin/) of the Johns Hopkins Center for Government Excellence [wrote](https://govex.jhu.edu/three-ways-data-quality-challenges-arise/) that “the most important step you can take [to address data quality problems] is starting to treat your data like a strategic asset.” That idea — treating data as a strategic asset — turns out to provide a helpful foundation for figuring out how to realize our vision.

## What makes data strategic?

Treating data like a strategic asset sounds great, but what does it actually mean? More fundamentally, just what makes a particular set of data “strategic”?

Internally it seems straightforward that the strategic value of a dataset should be tied to its ability to measure performance and to support decision-making in areas that the organization deems strategic. Externally, I believe the value of data is best measured by its ability to empower entrepreneurial activity for economic gain and improved civic engagement, something explicitly called out in many open data policies, including [ours](http://coablog.ashevillenc.gov/wp-content/uploads/2016/02/Resolution-No.-15-189.pdf). Briefly, then, we may say data is strategic if:

* It is used to improve decision-making that influences outcomes tied to strategic goals;
* It is used by external actors to create economic or social value for the community.

What’s striking about those definitions is what they share: use. _It is the use of the data that makes it strategic (or not)_. Thus, our approach centers on use and users.

## Cultivating and empowering data users

If the strategic value of data lies in its use, then data with no users obviously can’t be strategic. Perhaps then we should avoid adding a dataset until a compelling use and set of users are identified?

That’s certainly an option, but we believe treating data as a strategic asset aligns better with the proactive approach proposed in the recent GovLab/Omidyar Network report on open data impact, which recommends that governments “take steps to increase the capacity of public and private actors to make meaningful use of open data”. Their recommendation pertains to external users of open data, but it applies equally well to internal users. The key is to create a relationship with data users and to actively support and expand their ability to make effective use of data.

Our work in this area is just beginning, but we are experimenting with several ideas:

Talk about it. Every chance we get we talk up our efforts to make data easier to access and use. What’s gratifying is that word has begun to spread: people are starting to come to us to talk about opportunities they see to use data to manage performance and and to communicate and collaborate with citizens.
Give users ways to tell us what they’re interested in. The new version of SimpliCity will let people subscribe to specific topics and datasets so that we can reach out to them when changes are in the works or to get user feedback on what we’re providing. We are also launching a new public records request portal that not only lets citizens access data from prior requests, but gives us a better window into the kinds of data that people are interested in.
Identify and connect with key data users in the community. We plan to hold outreach events for frequent open data users in the community, such as the local Code for America brigade, news organizations, advocacy groups and professional groups.
Provide ways for users to hold us accountable. There is no better quality-control mechanism than to have active users who depend on the quality of the data, but it is important to communicate clearly what they can expect and to give them an easy way to communicate issues to us. In addition to our efforts above, the infrastructure discussed in the next section will play a vital supporting role in accomplishing this.
Let metadata drive the data infrastructure
Creating relationships and maintaining conversation with users of the data is important, but what about the actual mechanics of maintaining high-quality metadata for our data? No matter how noble our plans and intentions, the minute we have to do something special to keep the metadata up to date is the minute it will begin falling behind.

Our big idea here is to turn the process around. Rather than try to keep metadata in sync with the data, why not let the metadata itself drive the entire data infrastructure? Maintaining metadata and maintaining data then become the same activity.

![Complexity. Photo by Mark Skipper](../assets/767005521085dfe95e5bo-1024x771.jpg "Behind-the-scenes look at the data infrastructure of a city.")

That’s the idea that powers our new data management system, ComplexCity.* ComplexCity consists of a hierarchy of metadata directories together with a few scripts that use that metadata to create and maintain the data infrastructure. At the highest level, the system has three key design goals:

Provide high-quality metadata to reporting and management data users,
Maintain the integrity of the relationship between reporting and source data,
Maintain the integrity of the relationship between the data and applications that use it.
The system is a work in progress, but currently there are scripts to:

Validate data set definitions against the associated tables in the target and (soon) source databases;
Create ETL jobs that move data from enterprise systems into the reporting warehouse;
Run the ETL jobs, accounting for dependencies between datasets; and
Generate API code and configuration for use in SimpliCity’s GraphQL server.
ComplexCity will also help us better hold ourselves accountable to users of the data through generated dataset dashboards. With the launch of the new version of SimpliCity, each dataset in the system will automatically get a dashboard that includes summary information about the data, quick links to APIs and downloads and, most importantly, all the metadata, including links to contact the data owners about any issues with the dataset. By exposing this metadata to our users, we hope to empower them both to make more effective use of the data and to help us ensure that it is high-quality and serves the needs of the community.

## The road ahead
These plans are simple enough to state, but will entail an enormous amount of work in the months (and years) ahead. In carrying out that work, we will undoubtedly discover major gaps in our thinking as well as exciting opportunities to leverage what we’re building for even greater value. We’d love to hear your own ideas and critiques and would love even more to find ways to bring this approach to other local governments.

----
*The name was initially triggered by a joke — _SimpliCity_, powered by _Complexity_ — but the more we thought about it, the more it grew on us. There is no getting away from the fact that the data infrastructure of a city is complex. ComplexCity is our approach to managing it.

Originally published February 13, 2017.

Photo Credit: Mark Skipper [Complexity](https://www.flickr.com/photos/bitterjug/7670055210/).
