# VC-Issuer

## How to deploy  

```bash
# For testing
cat vc-issuer/*.yaml | envsubst | kubectl apply --dry-run=client -f -
# For deploying
cat vc-issuer/*.yaml | envsubst | kubectl apply -f -
```
## Env variables

| Name |  Description | Example (in clear text) | base64 |
| --- | --- | --- | --- |
| ISSUER_TLS_CRT | Base64 encoded x509 certificate |  | yes|
| ISSUER_TLS_KEY | Base64 encoded x509 certificate key|  | yes|
| PUBLIC_NODE_DOMAIN | Domain to use for ingress | | no |
| IMAGETAG_VC_ISSUER | Image tag for vc-issuer | 1.0.2 (at the time of writing this readme)| no |

