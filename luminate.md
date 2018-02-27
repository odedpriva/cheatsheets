# luminate

1. swtich tenants
* env=staging;leg=first; for t in \$(cat ~/swtich-list | grep \$env-\$leg-leg | sed \"s/\\${env}-\${leg}-leg=//g\" ); do devops-cli tenant switch-env -n \${t} -m pink-production-management-732237561.eu-west-1.elb.amazonaws.com -c pink-production-connectivity-136311067.eu-west-1.elb.amazonaws.com; done

2. run AT 
* nohup /home/ubuntu/scheduled-acceptance-test.sh silver '!gapps-identity-provider' &