# helm

## installing 
helm install management-portal --name-template "management-portal-{{randAlpha 6 | lower}}" 

## delete all 
helm delete --purge $(helm list --all -q)