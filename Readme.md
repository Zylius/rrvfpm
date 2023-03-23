# Project dedicated to analyze differences between FPM and RR speed in various situations

## Using

Just launch using `docker-compose up`.

## How to stress test

The program used to stress test was [WRK](https://github.com/wg/wrk). Example commands:

For FPM with blocking:
```shell
wrk -c100  -t12 -d60s http://localhost:81/testBlock --timeout 60 --latency
```

For RR without blocking:
```shell
wrk -c100  -t12 -d60s http://localhost:82/test --timeout 60 --latency
```

## Configuration

By default these tests use 32 constant FPM processes and 16 RR workers.

Memory is filled up after a simple test with these configs.

## Results
Currently collected results can be found [here](https://docs.google.com/spreadsheets/d/1xRe-D5CHS_ZLAHNUtCxDFvOSnV66ihs2UW-Mwc35oms/edit?usp=sharing).

