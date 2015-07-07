# log4j-android #

The first and only real full featured Log4j ported to android. .xml and .properties configuration do not work on android.

To use this project:

  * Clone the mercurial repository or download the source.
  * Use "maven install" or find the appropriate jar file in the target directory if you are not using maven.
  * if you are using maven include this dependency after installing
```
      <dependency>
	      <groupId>ufwa-common</groupId>
	      <artifactId>log4j-android</artifactId>
	      <version>1.2.17-1</version>
      </dependency>
```

Then just include this logger initialization in your application initialization.

```
static {

    org.apache.log4j.Logger root = org.apache.log4j.Logger.getRootLogger();

    final SocketAppender appender = new SocketAppender("10.168.1.113", 4445);
    root.addAppender(appender);

}

Logger logger = LoggerFactory.getLogger(this.getClass())

logger.debug("blah");
```