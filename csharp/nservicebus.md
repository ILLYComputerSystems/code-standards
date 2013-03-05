NServiceBus
=========

This file contains code standards relating to NServiceBus conventions and MSMQ queue names.

Message Handlers
--
* Handlers should be semantically named after the operation it performs *not the message it handles*, e.g.
```RecalculateLuceneIndexWhenClientChangedAddress``` rather than ```HandleClientChangedAddress```.
* Handlers should match tense with the intent of the message, i.e. commands should be in the present tense and events should be in the past tense.
* Remember SRP - a handler should only do one distinct role. If your handler is starting to look procedural then you probably need to split it up, e.g. rather than recalculating some stored data, sending off a message to an integration endpoint AND refreshing a cache, try splitting them into 3 separate handlers.
