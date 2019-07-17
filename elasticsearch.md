# elasticsearch

1. headers of an endpoint

`curl "$internal_cluster/_cat/indices?help"`

1 only specific headers

`curl "$internal_cluster/_cat/indices?h=i,ss"`

1. sort by colunm

`curl "$internal_cluster/_cat/indices?h=i,ss&s=ss"`

1. output as json ( or yaml or )

`curl "$internal_cluster/_cat/indices?h=i,ss&s=ss&format=json"`

1. get the largest indices

`$ curl -s "${ELASTIC}/_cat/indices?v&h=i,ss&s=store.size:desc" | head -n 20`

1. delete by query

`$ curl -X POST "${internal_cluster}/elastalert_status/_delete_by_query" -H 'Content-Type: application/json' -d '{"query":{"range":{"age":{"gte":10}}}}'`

links

[\_cat](https://www.elastic.co/guide/en/elasticsearch/reference/current/cat.html#common-parameters)
