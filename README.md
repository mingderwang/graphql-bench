# graphql-bench
* benchmark for mission-control-graph 8/12/2020
* Benchmarks for query-nodes in mission-control-graph testnet
* refer to https://github.com/hasura/graphql-bench
# run
cat bench.yaml | docker run -i --rm -p 8050:8050 -v $(pwd)/queries.graphql:/graphql-bench/ws/queries.graphql hasura/graphql-bench:v0.3
