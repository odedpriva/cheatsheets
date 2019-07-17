# aws

## activemq

```shell
aws mq update-broker --broker-id $borker_id --cli-input-json '{"Configuration":{"Id":"'"${config_id}"'","Revision":'${revision_id}'}}'
aws mq reboot-broker --broker-id $borker_id
```
