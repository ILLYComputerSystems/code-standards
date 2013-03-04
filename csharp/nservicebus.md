NServiceBus
=========

This file contains code standards relating to NServiceBus conventions and MSMQ queue names.

Message Handlers
--
Every handler should be semantically named after the operation it performs *not the message it handles*, e.g.
```UpdateXXXReportWhenClientChangedAddress``` rather than ```HandleClientChangedAddress```.