## Adding parsers for Spark logs:

Similar to LinuxSyslog parsers. Caveats: Spark messages don't contain a separate process id (pid),
hence the source becomes rquivalent to the component. (component+\[pid\] = source in syslogs)

This raises the question: should we ignore m_component or assign it the same calue as the source.

Parsing the timestamp on the message is different since the time formats differ.
