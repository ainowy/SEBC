<pre>
<b>Inspect the derived/default values. Adjust as necessary.</b>

Parameters adjustment:

Worker vcores	20
Worker spindles	12
Worker RAM	128
Workload factor	2
Worker nodes	10

I would say the memory for OS has a high value for a worker node. I think an amount between 0.6% and 0.9% can be enough for the OS. 
Then, in order to allow to execute more tasks per CPU, we should do yarn.nodemanager.resource.cpu-vcores * "workload factor"

<b>2. What criteria affects workload factor? What does a value of 1, 2, or 4 signify?</b>

The workload factor is affected by the number of tasks that are being executed by a core.
Depending on the workload factor, we could execute one or more tasks per core. The schema would be:

Workload factor = 1 for the execution of a task per core
Workload factor = 2 for the execution of two tasks per core
Workload factor = 4 for the execution of four tasks per core
</pre>
