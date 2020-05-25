# Notes and Research Folder

## Introducing a new log format into the existing project

- Add a new parameter to setup.props (something like useSpark=True, defaulting to false)
- Based on the value of this parameter, (from ControlDB.parseArgs), ControlDB creates a new db and invokes appropriate classes if the above parameter is true. (It invoked the new IDataStore class that contains the schema for the the new logs)
- This parameter can also be passed from the command line if needed.
