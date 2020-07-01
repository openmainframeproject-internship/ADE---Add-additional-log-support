## ADE- Additional Log Support

### Project Members:

1. Ayush Shridhar - Mentee
2. Jim Caffrey - Mentor

### Accomplishments of the week:

1. Added parsers for Spark logs. (SparklogLineReader.java, SparklogParserBase.java, SparklogParser.java)
2. Added tests for the parsers.

### Milestones:

1. Added parers. This includes regex patterns for matching the new timestamp.
2. Added tests. Looks to be working as intended.

### Issues:

1. There is no process id present within Spark logs.
2. component of a log message becomes same as the source (due to inavailability of pid)
2. Running tests gives me an unexpected AdeInternalError. Need to investigate why this might be happening.
Temporarily got around this by adding an initializer methods for the test cases.