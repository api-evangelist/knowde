# Knowde

Knowde is an AI platform for industrial operations, built for the chemicals and ingredients industry. Knowde AI extracts, structures, harmonizes and enriches product data out of legacy systems and offline documents; Knowde MDM is the master data repository that data lands in; Knowde CXP launches supplier storefronts natively integrated with MDM; and the Knowde Marketplace is a network of 8,000+ chemical company storefronts.

- Website — https://www.knowde.com/
- Developer Center — https://developer.knowde.com/
- Status — https://status.knowde.com/
- Trust Center — https://trust.knowde.com/

## APIs

| API | Base URL | Docs |
|---|---|---|
| Knowde GraphQL API | `https://developer-api.knowde.com/graphql` | https://developer.knowde.com/documentation/graphql |
| Knowde REST API | `https://developer-api.knowde.com` | https://developer.knowde.com/documentation/rest |

Knowde recommends GraphQL as the primary programmatic interface. Both surfaces use OAuth 2.0
client credentials against `https://developer-api.knowde.com/oauth/token`, with bearer tokens in the
`Authorization` header and RFC 7009 revocation at `/oauth/revoke`. API Clients are provisioned in the
Developer Portal by a company admin, and the Knowde API must be enabled for the company.

**No machine-readable contract is published anonymously.** The REST reference is rendered with Redoc
and the GraphQL reference is generated from the Knowde schema and exported as SDL, but both pages
redirect anonymous visitors to `https://www.knowde.com/sign-in`. GraphQL introspection at
`https://developer-api.knowde.com/graphql` returns HTTP 401. Every OpenAPI/Swagger/rswag path was
probed on `developer-api.knowde.com`, `api.knowde.com`, `developer.knowde.com` and `www.knowde.com`
and all missed.

## Artifacts

| Dir | File | Method |
|---|---|---|
| `authentication/` | `knowde-authentication.yml` | searched |
| `conventions/` | `knowde-conventions.yml` | searched |
| `conformance/` | `knowde-conformance.yml` | searched |
| `lifecycle/` | `knowde-lifecycle.yml` | searched |
| `changelog/` | `knowde-changelog.yml` | searched |
| `sandbox/` | `knowde-sandbox.yml` | searched |
| `packages/` | `knowde-packages.yml` | searched (no first-party SDK exists) |
| `security/` | `knowde-trust-center.yml` | searched |
| `security/` | `knowde-domain-security.yml` | probed |
| `well-known/` | `knowde-well-known.yml` | probed (no documents published) |
| `llms/` | `knowde-llms.txt` | generated |

Not present, and deliberately not authored: `openapi/`, `graphql/`, `mcp/`, `a2a/`, `asyncapi/`,
`skills/`, `errors/`, `scopes/`, `cli/`, `components/`, `data-model/` — Knowde publishes none of
these surfaces, and the pipeline does not fabricate them.
