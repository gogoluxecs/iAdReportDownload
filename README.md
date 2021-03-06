iAdReportDownload
=================

Download iAd report from iTunes and map content to bean.

You should edit src/test/java/iad.properties to run integration tests.

### Version

Latest version is 1.0.4.RELEASE.

### Compiling

* You should integrate project lombok to your IDE.
* For eclipse run `mvn eclipse:eclipse`.

### Integration

When you integrate library in your existing code you should add following maven dependencies:

```xml
<dependency>
  		<groupId>org.apache.httpcomponents</groupId>
			<artifactId>httpclient</artifactId>
			<version>4.2.3</version>
</dependency>
<dependency>
  		<groupId>org.jsoup</groupId>
			<artifactId>jsoup</artifactId>
			<version>1.7.2</version>
</dependency>
```

There is pending TODO task for this

### TODO

* Meaningful exception handling.
* PublisherId should be get automatically. Currently in the integration you need to hardcode it.
* Optimize report downloading flow- login in iAd only for the first report, for rest of the reports use session cookie.
If cookie is invlaid - re-log in to iAd and cotitnue with session cookie.
* Fix typo in test package name.

### Version History

#### 1.0.4.RELEASE

* Fixed dozer mapping.xml should be loaded from classpath.

#### 1.0.3.RELEASE

* Maven shade plugin

#### 1.0.2.RELEASE

* Update iAd paramter name for customDateRange reports selections.

#### 1.0.1.RELEASE 

* Fixed HTTP response stream caching to prevent empty bean in mapping when multiple reports are donwloaded.

#### 1.0.0.RELEASE

* First released revision
