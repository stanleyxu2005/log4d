# Logging facility for Delphi #

Log4D is a port of the well known log4j logging framework to Delphi. As the
original project (https://log4d.svn.sourceforge.net/svnroot/log4d/trunk) seems
not to be maintained actively, I decided to fork a branch with valuable 
improvements.

## What's New ##

### Parameterized Logging ###

It supports now an advanced feature called 'parameterized logging', which can 
significantly boost logging performance for disabled logging statement. If the 
current log level is lower than the global log level, log message will not be 
concatenated.

  BEFORE: LOG.Debug(Format('Invalid value %s' [Value]));
  NOW:    LOG.Debug('Invalid value %s', [Value]);
