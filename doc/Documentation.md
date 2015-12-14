# Documentation #

## Views ##

Currently, jvmtop has two views: The **overview mode** and the **detail mode**.

**The overview mode is the top-like view which shows all jvms at once** The detail view provides much more details about a specific jvm and provides a top-like view for all threads.

More views and other enhancements are planned. Ideas and suggestions are always welcome (add an entry in the issue tracker).


### VM overview mode ###

Command-line: `jvmtop.sh`

Columns are:
```
PID = process id
MAIN-CLASS = the "jvm name" but often the entry point class (with used main() method)
HPCUR = currently used heap memory
HPMAX = maximum heap memory the jvm can allocate
NHCUR = currently used non-heap memory (e.g. PermGen)
NHMAX = maximum non-heap memory the jvm can allocate
CPU = CPU utilization
GC = percentage of time spent in garbage collection (~100% means that the process does garbage collection only)
VM = Shows JVM vendor, java version and release number (S6U37 = Sun JVM 6, Update 37)
USERNAME = Username which owns this jvm process
#T = Number of jvm threads
DL = If !D is shown if the jvm detected a thread deadlock
```


### Detail mode (Single-VM monitoring) ###

Command-line:  `jvmtop.sh <pid>`

Columns are:
```
TID = thread id
NAME = thread name
STATE = current thread state
CPU = current CPU utilization (in ratio to available cpu time on all processors)
TOTALCPU = CPU utilization (in ratio to process cpu consumption) since the thread is alive
BLOCKEDBY = the thread id which blocks this thread
```

### Profiler ###

Due to the deisgn:
* the to-be-profiled jvm will face an significantly increased CPU-usage till the profiling ends
* compared to other profilers, the sample-rate is lower, however, for huge performance issues, it should suffice to diagnose issues in most-cases.
