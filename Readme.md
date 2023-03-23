# Project dedicated to analyze differences between FPM and RR speed in various situations

## Results
Currently collected results can be found [here](https://docs.google.com/spreadsheets/d/1xRe-D5CHS_ZLAHNUtCxDFvOSnV66ihs2UW-Mwc35oms/edit?usp=sharing).

## How to stress test

The program used to stress test was WRK. Example commands:

For FPM with blocking:
```shell
wrk -c100  -t12 -d60s http://localhost:81/testBlock --timeout 60 --latency
```

For RR without blocking:
```shell
wrk -c100  -t12 -d60s http://localhost:82/test --timeout 60 --latency
```


