### Version 0.44 - SVN trunk ###
- weather.cgi :
  * If the GET parameter 'zip' is not provided, use the first ZIP code found in /etc/rrdweather.conf ZIPS variable instead. Patch by Heikki Hokkanen. **This change requires a new perl library (Config::File)**
  * some small fixes (typo, etc.)


### Version 0.43 - July 2009 ###
- db\_update.sh
  * fixed broken link to data feed. Thanks to fugitif67
  * fixed null values when the connection is down. Thanks to fugitif67


### Version 0.42 - October 2007 ###
- weather.cgi
  * header titles now link to their section. Patch by Heikki Hokkanen
  * click on graphs to go to the next section (click on daily graphs to reach weekly graphs and so on)
  * no longer necessary to have several weather.cgi files to display different cities, zip passed as argument. Idea by Gregory Guthrie
  * city name fetched from the XML source
  * made XHTML 1.1 and CSS 2.1 compliant (again)


### Version 0.41 - October 2007 ###
- applied the patches made available by Lionel Porcheron in Ubuntu Universe repository
  * configuration file in /etc instead of editing script files
  * remove interactions and read informations from configuration file
  * change database location in cgi script
  * db\_builder.sh and db\_update.sh scripts now go in /usr/share/rrdweather
> > and no more in /usr/lib/rrdweather
  * call rrdweather\_cron.sh which creates rrd database if necessary (no need to run db\_builder.sh first)
- lower and upper limit variables for pressure graphs in cgi script
- speed variable for wind graphs in cgi script
- reduced size of graphs and changed general layout of graph page
- removed the average label for pressure, which was kind of pointless, and due to the smaller graphs,

> the labels for pressure were too large, so I needed to get rid of one
- new install script


### Version 0.40 - December 2006 ###
- Gregory Bittan reported an issue when the web connection is down.
> The script would still feed the RRD databases with a value of 0, messing up the average figures.
- The update script can now handle the monitoring of several cities
- Lionel Porcheron made RRDweather available to the Ubuntu Community trough
> the Universe repository
- To achieve the goal of monitoring several cities from a single script, RRDWeather had to use
> a new directory structure in order to store database files
- Better indenting
- Improved bash code
- Improved debugging mode
- ...


### Version 0.36 - January 2006 ###
- Lionel Porcheron made weather.cgi fully w3c XHTML 1.1 et CSS 2.1 compliant