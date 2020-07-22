## ADE- Additional Log Support

### Project Members:

1. Ayush Shridhar - Mentee
2. Jim Caffrey - Mentor

### Accomplishments of the week:

1. Fixed issue with severity module. Removing it entirely from spark logs was causing unwanted trouble while invoking the
upload bash script. 
2. Severity has been set to `UNKNOWN` by default. 
3. Added a sample spark log dataset for testing.

### Milestones:

1. Finalized the parsers.
2. Fixed issue with invoking bash scripts.

### Issues:

1. There is no process id present within Spark logs.
2. Would be better to have a specific set of bash scripts for testing Spark logs end-to-end. (This would need spark analyze xml files)