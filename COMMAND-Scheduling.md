Scheduling
==========

Adding tasks
------------

```
schedule = <schedule_id>, start, interval, <commands>
```

Call command every interval seconds, starting from start. An interval of zero calls the task once, while a start of zero calls it immediately. Currently command is forwarded to the option handler. start and interval may optionally use a time format, dd:hh:mm:ss. F.ex to start a task every day at 18:00, use 18:00:00,24:00:00.


Removing tasks
--------------

```
schedule_remove = <schedule_id>
```

Delete id from the scheduler.


Examples
--------

```
schedule = foo, 10, 60, load.start=~/Download/watch_old/*.torrent
schedule = bar, 10, 60, ((print,"foo ",((system.time_seconds))))
schedule = baz, 18:00:00, 24:00:00, ((print,"it's 6pm ",((system.time_seconds))))
```
