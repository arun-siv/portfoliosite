perf record -ag -F 97
perf record -p 188 -

-a all cpu
-p specific process
-- run workload and capture it
-F frequency of samples(Hz)
-c # of events in each sample

perf script

perf report --stdio

perf report 