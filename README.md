# aninaka-ops

# データベースへのアクセス

kubectl exec -it psql-pod -n aninaka -- psql -h mypostgres -U postgres

# secret 作成

kubectl create secret tls user-auth-secret --cert user-auth-ingress.crt --key user-auth-ingress.key --dry-run=client --output=yaml > user-auth-secret.yaml
