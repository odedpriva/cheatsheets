# redis

## export certificates
redis-cli -h redis.staging.eu-west-1.luminateops.com --scan --pattern "*traianaops.luminatesite.com:*" | while read -r line; do redis-cli -h redis.staging.eu-west-1.luminateops.com get $line | jq -r .cert_pem > /tmp/cert/$line_cp.pem; done

## connect to redis without redis-cli
echo -e "*1\\r\\n\\$4\\r\\nINFO\\r\\n" | nc redis.development.eu-west-1.luminateops.com 6379