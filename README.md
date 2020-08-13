# graphql-bench
* benchmark for mission-control-graph 8/12/2020
* Benchmarks for query-nodes in mission-control-graph testnet
* refer to https://github.com/hasura/graphql-bench
# run
cat bench.yaml | docker run -i --rm -p 8050:8050 -v $(pwd)/queries.graphql:/graphql-bench/ws/queries.graphql hasura/graphql-bench:v0.3
# result for Phare 0
```
====================
benchmark: gravity
  --------------------
  candidate: GravityQuery on gravity-bench at http://graph.graph-mission-control.muzamint.com/subgraphs/name/jannis/gravity/graphql
    Warmup:
      ++++++++++++++++++++
      1000000Req/s Duration:60s open connections:1000
      Running 1m test @ http://graph.graph-mission-control.muzamint.com/subgraphs/name/jannis/gravity/graphql
        8 threads and 1000 connections
        Thread calibration: mean lat.: 5035.475ms, rate sampling interval: 18186ms
        Thread calibration: mean lat.: 8589.287ms, rate sampling interval: 18972ms
        Thread calibration: mean lat.: 5081.690ms, rate sampling interval: 18235ms
        Thread calibration: mean lat.: 5082.377ms, rate sampling interval: 18202ms
        Thread calibration: mean lat.: 5109.702ms, rate sampling interval: 18268ms
        Thread calibration: mean lat.: 5124.433ms, rate sampling interval: 18300ms
        Thread calibration: mean lat.: 5141.018ms, rate sampling interval: 18300ms
        Thread calibration: mean lat.: 5149.882ms, rate sampling interval: 18300ms
        Thread Stats   Avg      Stdev     Max   +/- Stdev
          Latency    34.67s    14.17s    0.99m    58.20%
          Req/Sec   512.00     10.24   524.00     68.75%
        241081 requests in 1.00m, 31.50MB read
        Socket errors: connect 0, read 0, write 0, timeout 828
        Non-2xx or 3xx responses: 241081
      Requests/sec:   4019.71
      Transfer/sec:    537.79KB
    Benchmark:
      ++++++++++++++++++++
      1000000Req/s Duration:100s open connections:1000
      Running 2m test @ http://graph.graph-mission-control.muzamint.com/subgraphs/name/jannis/gravity/graphql
        8 threads and 1000 connections
        Thread calibration: mean lat.: 5331.362ms, rate sampling interval: 18857ms
        Thread calibration: mean lat.: 5349.570ms, rate sampling interval: 18857ms
        Thread calibration: mean lat.: 5357.100ms, rate sampling interval: 18857ms
        Thread calibration: mean lat.: 5380.390ms, rate sampling interval: 18890ms
        Thread calibration: mean lat.: 5394.931ms, rate sampling interval: 18874ms
        Thread calibration: mean lat.: 5392.352ms, rate sampling interval: 18874ms
        Thread calibration: mean lat.: 5391.598ms, rate sampling interval: 18874ms
        Thread calibration: mean lat.: 5417.959ms, rate sampling interval: 18923ms
        Thread Stats   Avg      Stdev     Max   +/- Stdev
          Latency     0.92m    25.54s    1.66m    58.15%
          Req/Sec   462.41     19.91   500.00     75.00%
        368987 requests in 1.67m, 48.21MB read
        Socket errors: connect 0, read 0, write 0, timeout 1123
        Non-2xx or 3xx responses: 368987
      Requests/sec:   3691.41
      Transfer/sec:    493.87KB
 * Serving Flask app "bench" (lazy loading)
 * Environment: production
   WARNING: Do not use the development server in a production environment.
   Use a production WSGI server instead.
 * Debug mode: off
 ```
