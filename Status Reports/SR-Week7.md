## ADE- Additional Log Support

### Project Members:

1. Ayush Shridhar - Mentee
2. Jim Caffrey - Mentor

### Accomplishments of the week:

1. Finalize AdeMaskLog for spark.
2. Added more tests - everything seems to work fine.

### Milestones:

1. Added spark log support in AdeMaskLogs.java
2. Replaced all missing components of Spark logs with hooks. The plan is to finalize these once we have the final logs.
3. Realized the issue with no data being insertde in derby database. (controldb merely creates schemans)

### Issues:

1. There is no process id present within Spark logs.
2. upload script now fails to insert spark logs. Gives an `AdeInternalException` error.