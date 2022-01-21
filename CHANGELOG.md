# v1.0.2

[bugfix] Avoid UnboundLocalError when exception occurs immediately at iterating over batch data.

# v1.0.1

[bugfix] Avoid read-in deadlock

* When an error is thrown while data is read in, the queues
  within HiroGraphBatch need to be closed cleanly or a
  deadlock will occur. Fixed.

# v1.0.0

Created project by splitting `batchclient.py` from [hiro-graph-client](https://github.com/arago/hiro-client-python).