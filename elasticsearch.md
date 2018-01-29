# elasticsearch

1. get the largest indices

`$ curl -s  ${ELASTIC}/_cat/indices?v&h=i,ss&s=store.size:desc head -n 20`

