# Credentials events service

## How to deploy  

```bash
# For testing
cat credentials-events-service/*.yaml | envsubst | kubectl apply --dry-run=client -f -
# For deploying
cat credentials-events-service/*.yaml | envsubst | kubectl apply -f -
```

## Env variables

| Name | Description | Example (in clear text)                                          | base64 |
| --- | --- |------------------------------------------------------------------| --- |
| CES_POSTGRES_USER | Username for postgres | Y2jkVzZGI=                                                       | yes |
| CES_POSTGRES_PASSWORD | Password for postgres user | YWxlajkj2pmMzg0                                                  | yes |
| IMAGETAG_CES| Credential events service image tag | v1.3.1                                                           | no |
| POSTGRES_IMAGETAG| Postgres image tag | 15.3                                                             | no |
| trustedIssuersListUrl | Url pointing to a list of trusted Issuers | https://registry.lab.gaia-x.eu/v1/api/trusted-issuers/compliance | no |
| trustedIssuersListDisabled | boolean to disable the trustedIssuersList | "false"                                                          | no |

## Additional notes
Currently, 'trustedIssuersListDisabled' is set to "true", as we are not a part of the default trusted issuers. 