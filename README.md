:WeblogsApp-1.0
===========

The WebLogApp monitors a web servers access and error logs. 

## Downloads 

 * [WeblogsApp-1.0.zip](https://github.com/logscape/unixapp/raw/master/dist/WeblogsApp-1.0.zip)
 * [WeblogsApp-1.0-overrides.properties](https://www.google.com)


Read ![How to deploy](http://logscape.github.io/deploy.html)


## Setting up Apache 
The WebLogApp supports the most commont web server log formats.

 Common Log Format  ( www-clf ) 

        LogFormat "%h %l %u %t \"%r\" %>s %b" common

 Extended /NCSA Log Format ( www-xlf) 

        LogFormat "%h %l %u %t \"%r\" %>s %b \"%{Referer}i\" \"%{User-agent}i\"" ncsa

 Custom log that includes the time taken to serve a page (%D) 

        LogFormat "%h %l %u %t \"%r\" %>s %b \"%{Referer}i\" \"%{User-agent}i\" %D"  custom

 json example

        LogFormat "timestamp:\"%t\", request: \"%r\", ...



You will need to use the 'custom' format to include the time taken to serve pages in your access log. If this isn't included some of your charts may appear blank . 

## Setting up IIS 

IIS uses W3C log format by default, which provides the time taken metric. 

 ![IIS Logging Config](docs/images/iis-logging.png) 

Make sure that you have W3C selected. 

## Overview

 ![](docs/images/iis-overview.png)


## Web  Resources 

 ![](docs/images/iis-resources.png) 



## Bad Status codes and Error Logs 

 ![](docs/images/iis-errors.png) 


