=============
SiteAnalyzer
=============

SiteAnalyzer is a package to analyze PHP sites. With this package, it is possible to count pages, understand user behavior, analyze the interaction of the site, and perform A/B testings. SiteAnalyzer can be installed into any PHP in seconds without affecting the business logic of the application and customized according to the needs. SiteAnalyzer makes use of machine learning algorithms and statistics to analyze a site and create meaningful reports. 

Features
--------

- Click counter
- User profile analysis
- A/B testing
- Site dynamics analysis

Installation
------------

SiteAnalyzer can be installed through [Composer](https://getcomposer.org):

```shell
$ composer require rdorado/site-analyzer
```


Or modify your composer.json requirements:

```json
    "require": {
        "rdorado/site-analyzer": "^0.0.1"
    }
```
and update your project:

```shell
$ composer update
```

Usage
-----

Count all the views/pages you want to observe by importing the ```SiteAnalyzer``` class and then using the ```count``` static method:

```php
use SiteAnalyzer\SiteAnalyzer;
SiteAnalyzer::count();
```


You can also include other options to be stored on the database. That depends on the kind of reportings or analyzis you want to perform:

```php
$options = ['id' = $myid];
SiteAnalyzer::count($options);
```



Reporting/Displaying the stored information
===========================================

Once you have started to count the page hits, different sort of reports can be displayed. For example, a very basic report is the number of hits per page stored on the database:

```php 
$data = SiteAnalyzer::getStats();
print( SiteAnalyzer::transform($data, "html") );
``` 

Main features
===========================================

Counting
**********************

The core functionality of SiteAnalyzer is to store counts. Every time the static method ```SiteAnalyzer::count();``` is called it stores the url associated 

```php
use SiteAnalyzer\SiteAnalyzer;
SiteAnalyzer::count();
```
