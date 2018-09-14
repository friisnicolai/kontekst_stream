# Kontekst Stream
Asynchronous persistent streams for Flutter. Send and receive events in Flutter using streams that have their data persisted on disk and/or in a cloud storage.

Use cases:
- Async collection and storage of data, for example events
- Async reliable messaging between apps, components, isolates and native processes
- Decoupling of consumers and producers of events, messages and data

Technical Concept

A Kontekst Stream instance is created with underlying storage, having a number of sinks and streams, organized as "Subjects".

Sink:
- A producer adds data to subject sink
- Once commited and acknowledged the producer knows the data is stored

Stream:
- A consumer registers to the Kontekst Stream instance and sets up a stream listening to a subject
- The consumer can choose a position on the data stream where to start listening, start, end or somewhere in the middle
- As new data is added they are sent to the consumer streams
