# luminate

1. swtich tenants

`env=staging;leg=first; for t in \$(cat ~/swtich-list | grep \$env-\$leg-leg | sed \"s/\\${env}-\${leg}-leg=//g\" ); do devops-cli tenant switch-env -n \${t} -m pink-production-management-732237561.eu-west-1.elb.amazonaws.com -c pink-production-connectivity-136311067.eu-west-1.elb.amazonaws.com; done`

1. creating tenant
`curl -H "Content-Type: application/json" -X POST --data '{"Name":"testpeleg"}' http://127.0.0.1:8080/v1/tenants`

1. sanity

`for c in $(docker ps --format {{.Names}}); do num=$( docker logs $c --since 2m 2>&1 | wc -l); echo $num $c; done | sort -nr`

1. poor man performance:

`while true; do var=$((var+1)) ; curl -s -o /dev/null -w "$var sites %{http_code}\n" 'https://admin.luminate.luminatesite.com/v1/sites' -H 'Content-Type: application/json' -H 'Referer: https://admin.luminate.luminatesite.com/applications' -H 'Cookie: ACCEZZIOCOOKIE=c23f6743-2617-464a-98c7-880ba6b65b89' -H 'Connection: keep-alive' -H 'Cache-Control: no-cache' --compressed; done`