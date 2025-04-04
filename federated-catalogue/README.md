# Omega-X Catalogue

## How to deploy  

```bash
# For testing
cat federated-catalogue/*.yaml | envsubst | kubectl apply --dry-run=client -f -
# For deploying
cat federated-catalogue/*.yaml | envsubst | kubectl apply -f -
```

## Env variables

| Name |  Description | Example (in clear text)          | base64 |
| --- | --- |----------------------------------| --- |
| FEDERATED_CATALOGUE_API_KEY | 32 alphanumeric char key to use the API | ktw6hzUc2iKZA66sqGtvw8L6VWmSdC4N | yes |
| FEDERATED_CATALOGUE_PARTICIPANT_NAME | Name of the participant hosting the catalogue |                                  | no |
| IMAGETAG_FEDERATED_CATALOGUE | Federated catalogue docker image version | 1.2.0                            | no |
| PUBLIC_NODE_DOMAIN | Domain to use for ingress |                                  | no |