# User Agent

## How to deploy  

```bash
# For testing
cat user-agent/*.yaml | envsubst | kubectl apply --dry-run=client -f -
# For deploying
cat user-agent/*.yaml | envsubst | kubectl apply -f -
```

## Env variables

| Name |  Description | Example (in clear text)          | base64 |
| --- | --- |----------------------------------| --- |
| CATALOG_API_KEY | 32 alphanumeric char key to use the API | plw6hzUc2iKZA66sqGtvw8L6VWmSdC5N | yes |
| AGENT_API_KEY | 32 alphanumeric char key for the participant agent | plw6hzUc2iKZA66sqGtvw8L6VWmSdC5N | yes |
| AGENT_TLS_CRT | Base64 encoded x509 certificate |                                  | yes|
| AGENT_TLS_KEY | Base64 encoded x509 certificate key|                                  | yes|
| PROJECT_NAME | Cluster name |                                  | no |
| PUBLIC_NODE_DOMAIN | Domain to use for ingress |                                  | no |

