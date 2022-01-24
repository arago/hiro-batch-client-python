# v1.0.3

* Allow continuing of read-in-iteration when the iterator is yielding a dict {"error", Exception}.

* The results now contain a field "order" to get the order in which the commands have been put into the request_queue.

* Added logging of fatal errors while reading from the queues. This also prevents possible deadlocks.

# v1.0.2

* [bugfix] Avoid UnboundLocalError when exception occurs immediately at iterating over batch data.

# v1.0.1

[bugfix] Avoid read-in deadlock

* When an error is thrown while data is read in, the queues
  within HiroGraphBatch need to be closed cleanly or a
  deadlock will occur. Fixed.

# v1.0.0

Created project by splitting `batchclient.py` from [hiro-graph-client](https://github.com/arago/hiro-client-python).