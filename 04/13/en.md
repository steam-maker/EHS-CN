If all of the fields of a messenger structure were enumerated according to this view, we would have:

Field              | Note
-------------------|---------------------------------------- 
GLOBAL             | the environment of the parameter values 
SENDER             | the sender of the message
RECEIVER           | the receiver of the message 
REPLY-STYLE        | wait, fork, ...?
STATUS             | progress of the message
REPLY              | eventual result (if any)
OPERATION SELECTOR | relative to the receiver
# OF PARAMETERS    | 
P1                 | 
...                | 
Pn                 | 

This is a generalization of a stack frame, such as used by the B5000, and very similar to what a good intermodule scheme would require in an operating system such as CAL-TSS—a lot of state for every transaction, but useful to think about.
