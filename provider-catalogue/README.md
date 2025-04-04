# Provider catalogue

## How to deploy  

```bash
# For testing
cat provider-catalogue/*.yaml | envsubst | kubectl apply --dry-run=client -f -
# For deploying
cat provider-catalogue/*.yaml | envsubst | kubectl apply -f -
```

## Env variables

| Name | Description | Example (in clear text) | base64 |
| --- | --- | -- | --- |
| PUBLIC_NODE_DOMAIN | Domain to use for ingress | | no |
| IMAGETAG_PROVIDER_CATALOGUE | Docker version for the provider catalogue| 1.2.0 | no |
| FEDERATED_CATALOGUE_PARTICIPANT_NAME | Name of the participant hosting the catalogue | participant | no |
| PARTICIPANT_AGENT_SECRET_KEY | 32 alphanumeric char key to use the AP | ktw6hzUc2iKZA66sqGtvw8L6VWmSdC4N | yes |
