# log4j-android #

The first and only real full featured Log4j ported to android. .xml and .properties configuration do not work on android.

```
static {
    org.apache.log4j.Logger root = org.apache.log4j.Logger.getRootLogger();
    final SocketAppender appender = new SocketAppender("10.168.1.113", 4445);
    root.addAppender(appender);
}

Logger logger = LoggerFactory.getLogger(this.getClass())

logger.debug("blah");
```