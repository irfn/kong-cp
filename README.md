# Kong Control Plane
This is a wrapper to official kong charts and just supplies default values

values which should be overridden 
- pg_host: kongdb-postgresql
- pg_user: kong
- pg_password: kong
- pg_database: kong

Additionally a tls secret should be created from kong cluster secrets
`kubectl create secret tls kong-cluster-cert-secret --cert=./cluster.crt --key=./cluster.key`

where this pair should be generated via process mentioned here
https://docs.konghq.com/gateway/latest/production/deployment-topologies/hybrid-mode/setup/
