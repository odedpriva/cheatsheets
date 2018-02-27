# vault

1. create vault with dynamo as backend

```docker run --cap-add=IPC_LOCK -e AWS_ACCESS_KEY_ID=123 -e AWS_SECRET_ACCESS_KEY=123 -e 'VAULT_LOCAL_CONFIG={"backend": {"dynamodb": {"ha_enabled": "false","region":"eu-west-1","table":"gate1-vault-application"}}, "default_lease_ttl": "168h", "max_lease_ttl": "720h","listener":{"tcp":{"address":"0.0.0.0:8200","tls_disable":"true"}}}' -p 8200:8200 vault:0.8.0 server```
