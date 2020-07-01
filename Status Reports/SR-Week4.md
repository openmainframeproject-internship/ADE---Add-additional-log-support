## ADE- Additional Log Support

### Project Members:

1. Ayush Shridhar - Mentee
2. Jim Caffrey - Mentor

### Accomplishments of the week:

1. Added newer parameter in setup.props file to deceide the logs begin used.
The parameter (useSpark = True if dealing with Spark and false for Syslogs) is an attribute of AdeExternalConfigProperties. 

### Milestones:

1. Add new parameter in ade-ext and setup.props.
2. Build and test to ensure the changes are working as intended.

### Issues:

1. Look at the interfacing of AdeExternalConfigProperties and log parsers.
We'd like to invoke the Spark log parsers if useSpark=True.
2. Investigate if Schema needs to be updated.