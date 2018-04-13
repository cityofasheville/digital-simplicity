# Doing More with Less
### By Christen McNamara

![A tiny house being pulled down a road by a pickup truck with mountains in the background](../assets/tinyHouse.jpg "A tiny house being pulled down a road by a pickup truck with mountains in the background")


Last Fall, my co-worker Cameron Carlyle and I were trying to come up for an idea to present at the NC GIS Conference in Raleigh.  Work we had already completed seemed boring so we decided to pick one of our really ambitious goals, and present it – which meant we would have to do it.  Yikes!

We had been struggling with managing multiple local servers housing our GIS REST services and web servers for our [web map viewers](https://cityofasheville.github.io/maps//).  As we produced more map applications, services and open data, our servers were screaming under the load. Don’t get me wrong, it was great that staff and citizens were consuming city data, but finding the time to maintain servers was limiting my time for other work.  Our goal was to leverage the cloud for our GIS data, and relieve the stress on those servers.  In other words, we wanted to find a way to continue producing high demand GIS web services without having to worry about the hardware.

We’re still working on this project, but are excited to be using [GitHub*](https://github.com/) pages to host our our web mapping applications instead of IIS on our local Windows servers.  We are also using ESRI’s ArcGIS Online to host our data as REST services, and keep the data up-to-date using our ETL software. Using cloud based hosting decreases our dependency on local server infrastructure (which we have to maintain), and gives us more time to work on cool projects or maybe start writing up our presentation!

I’ll update the blog with the project status as we continue, or come see our presentation at NC GIS 2017, February 24th.

Have you ever used GitHub for projects?


*Our team has been using GitHub for a few years developing projects such as SimpliCity and evaluating potential candidates — it’s a great tool for open collaboration, a necessity for any truly digital team.

Originally published February 15, 2017.

Tag: data management, GIS, IT services, maps, open data