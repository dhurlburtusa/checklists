# Daemon Process

A daemon process, a.k.a. background process, is a computer program that runs in the background and does not run under the direct control of an interactive user.

These processes tend to be started while or shortly after an operating system starts. They also tend to run for a long time before explicitly being signaled to shutdown.

Processes which are started and are intended to continue running until explicitly signalled to stop (or restart) or automatically stop due to an error are usually considered to be long-running. Web servers and OS services are of this variety. A process that runs for a long time but automatically stops when it completes its task is usually not considered to be a long-running process as described here. For example, a script to process large amounts of data and stops when finished is one such example.

## Lifecycle

Most processes have the following lifecycle.

- Startup phase.
- Running phase.
- Reconfiguration phase (optional).
- Shutdown phase.

### Startup Phase

During the startup phase, the following typically happens:

- Configuration is read and made available.
- Required dependencies are checked for availability.
  + Examples:
    * Expected libraries.
    * File system directories.
    * Disk space.
    * etc.
- Cleanup from previous runs are made.
- Allocation of resources:
  + Examples:
    * Connections to services such as databases, message queues, etc are made.
    * File system directories created.
- One-time tasks are performed (sometimes dependent on previous exit states).
