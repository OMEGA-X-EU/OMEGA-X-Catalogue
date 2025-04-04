# Omega-X Catalogue

The Omega-X catalogue is a set of components constituting a Gaia-X compliant federated catalogue. It comprises:
- [the federated catalogue](https://gitlab.com/gaia-x/data-infrastructure-federation-services/deployment-scenario/catalogue/federated-catalogue): the API to use to aggregate all offerings from a set of participants, and do search queries among them.
- [the user-agent](https://gitlab.com/gaia-x/data-infrastructure-federation-services/deployment-scenario/user-agent): the API to use to store and manage all self-descriptions from a certain participant.
- [the vc-issuer](https://gitlab.com/gaia-x/data-infrastructure-federation-services/deployment-scenario/vc-issuer): the API to issue verifiable credentials, called by the user-agent.
- [the provider-catalgoue](https://gitlab.com/gaia-x/data-infrastructure-federation-services/deployment-scenario/catalogue/provider-catalogue): the API to use to aggregate all offerings from one participant that are to be shared with the federated catalogue.
- [the credentials-events-service](https://gitlab.com/gaia-x/lab/credentials-events-service): the api to use to share compliance variables originating from a remote catalogue.

This repository contains Kubernetes manifests used in Omega-X Project to deploy Gaia-X Catalogue in the Kubernetes cluster.