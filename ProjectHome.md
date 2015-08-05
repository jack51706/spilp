Spilp is a simple Python script that takes IIS logs, parses them and creates statistical reports which can be used to discover unusual IP activity more easily.

Check [usage guide](http://code.google.com/p/spilp/wiki/Usage) on how to use spilp.
A **sample** of spilp-generated reports archive can be downloaded [here](http://cmikavac.net/download/spilp_reports.zip).

## Features: ##

  * extracts a [list of IP addresses](http://cmikavac.net/download/spilp/generated_reports/hitsPerIp_110916.txt) with number of hits they made sorted by number of hits
  * extracts a [list of "close" IP addresses](http://cmikavac.net/download/spilp/generated_reports/closeIps_110916.txt) that made a certain number of hits
  * extracts a [list of user agents](http://cmikavac.net/download/spilp/generated_reports/agentHits_110916.txt) sorted by number of hits
  * extracts a [list of cs-method hits](http://cmikavac.net/download/spilp/generated_reports/methodHits_110916.txt) (GET method excluded)
  * extracts a list of file hits sorted by number of hits
    * .pdf, .doc, .xls, .ppt ([document files](http://cmikavac.net/download/spilp/generated_reports/documentDownloads_110916.txt)) + [extended version](http://cmikavac.net/download/spilp/generated_reports/documentDownloadsExtended_110916.txt)
    * .js, .htm, .asp ([web files](http://cmikavac.net/download/spilp/generated_reports/webFilesHits_110916.txt)) + [extended version](http://cmikavac.net/download/spilp/generated_reports/webFilesHitsExtended_110916.txt)
  * extracts extended information for document and web file hits
    * includes timestamps, client IP addresses, methods, ports, user agent details and http status codes
  * extracts a [list of "unusual" http status code hits](http://cmikavac.net/download/spilp/generated_reports/hitsByStatus_110916.txt) sorted by number of hits
    * client IP address list
    * a list of files hit by an IP and number of hits for that file
  * filtering results (include or exclude filtering - works in "either-or" way)
    * ability to auto-generate an IP range list as a filter
  * reverse DNS country lookup using MaxMinds GeoIP country downloadable database
    * additional info in certain reports
    * filtering results by country of origin (as a separate filtering option using spilpconf.py file)
  * ability to process large amount of IIS log files
  * CONFIG file for performance and output tweaking

(if you experience a lot of bolded text under features **_you might need to refresh_** a few times because google code hosting wiki sometimes does not render wiki list markup correctly)