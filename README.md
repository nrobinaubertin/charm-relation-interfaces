# Charm Relation Interfaces

A catalogue of opinionated and standardized interface specifications for charmed operator relations. The purpose of the repository is to outline the behavior and requirements for key interface names, ensuring that charms claiming to implement a certain interface actually are capable of being integrated with each other.

## Contributing
To contribute a new interface specification, open a pull request containing:
- a `README.md` explaining the purpose of the interface and the protocol
- a `schema.py` file containing pydantic models that specify the app and unit databag model for either side of the interface. 
- `charms.yaml` file consisting of a list of any `providers` and `requirers` known to adhere to the specification. 
- under `docs/`, the json schemas generated from the pydantic schemas. You can use command `tox -e build-json-schemas` to generate them automatically. Do not edit those files manually.  

To quickly get started, see the [template interface](https://github.com/canonical/charm-relation-interfaces/tree/main/interfaces/__template__/v0) for a template of what to include and how it should be structured. 


## Interfaces

| Category      | Interface                                                                    |                               Status                                |
|---------------|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------:|
| Data          | [`mysql_client`](interfaces/mysql_client/v0/README.md)                       | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |
|               | [`postgresql_client`](interfaces/postgresql_client/v0/README.md)             | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |
|               | [`mongodb_client`](interfaces/mongodb_client/v0/README.md)                   | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |
|               | [`kafka_client`](interfaces/kafka_client/v0/README.md)                       | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |
|               | [`opensearch_client`](interfaces/opensearch_client/v0/README.md)             | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |
|               | [`database_backup`](interfaces/database_backup/v0/README.md)                 | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |
| Identity      | [`oauth`](interfaces/oauth/v0/README.md)                                     | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |
| Observability | [`grafana_auth`](interfaces/grafana_auth/v0/README.md)                       | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |
|               | [`ingress`](interfaces/ingress/v0/README.md)                                 | ![Status: Live](https://img.shields.io/badge/Status-Live-darkgreen) |
|               | [`ingress_per_unit`](interfaces/ingress_per_unit/v0/README.md)               | ![Status: Live](https://img.shields.io/badge/Status-Live-darkgreen) |
|               | [`prometheus_remote_write`](interfaces/prometheus_remote_write/v0/README.md) | ![Status: Live](https://img.shields.io/badge/Status-Live-darkgreen) |
|               | [`prometheus_scrape`](interfaces/prometheus_scrape/v0/README.md)             | ![Status: Live](https://img.shields.io/badge/Status-Live-darkgreen) |
| Networking    | [`ingress`](interfaces/ingress/v0/README.md)                                 | ![Status: Live](https://img.shields.io/badge/Status-Live-darkgreen) |
|               | [`ingress_per_unit`](interfaces/ingress_per_unit/v0/README.md)               | ![Status: Live](https://img.shields.io/badge/Status-Live-darkgreen) |
| Security      | [`mutual_tls`](interfaces/mutual_tls/v0/README.md)                           | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |
|               | [`tls_certificates/v0`](interfaces/tls_certificates/v0/README.md)            | ![Status: Live](https://img.shields.io/badge/Status-Live-darkgreen) |
|               | [`tls_certificates/v1`](interfaces/tls_certificates/v1/README.md)            | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |
| Storage       | [`s3`](interfaces/s3/v0/README.md)                                           | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |

## Project-internal Interfaces

### Charmed Kubeflow

| Category      | Interface                                                                    |                               Status                                |
|---------------|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------:|
| Metadata      | [`k8s-service`](interfaces/k8s-service/v0/README.md)                         | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |

### Identity

| Category      | Interface                                                            |                               Status                                |
|---------------|:---------------------------------------------------------------------|:-------------------------------------------------------------------:|
| Identity      | [`hydra_endpoints`](interfaces/hydra_endpoints/v0/README.md)         | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |
|               | [`kratos_external_idp`](interfaces/kratos_external_idp/v0/README.md) | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |
|               | [`kratos_endpoints`](interfaces/kratos_endpoints/v0/README.md)       | ![Status: Draft](https://img.shields.io/badge/Status-Draft-orange)  |

For a more detailed explanation of statuses and how they should be used, see [the legend](https://github.com/canonical/charm-relation-interfaces/blob/main/LEGEND.md).

