# Vekia

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Vekia is a French supply-chain software vendor founded in 2008 in Lille by Manuel Davy (Vekia SAS,
143 rue d'Athènes, 59800 Lille, RCS Lille Métropole 503 225 716). Its platform, **Vekia Engine**,
applies probabilistic AI and machine learning to demand and stock forecasting, then generates
optimised purchase-order proposals pushed back into the customer's existing ERP, alongside
shortage-risk alerting and a logistics control tower. **Vekia Disrupt** covers disruption and
shortage management. The platform is hosted on Microsoft Azure in Europe and sold to retail and
specialised distribution, e-commerce, industry, energy and telecom, with published case studies at
ENGIE, Mr Bricolage and Okaïdi.

## Developer surface

**Vekia publishes no public API.** There is no developer portal, no API reference, no SDK and no
machine-readable contract of any kind — no OpenAPI, AsyncAPI, GraphQL SDL, JSON Schema or Postman
collection. `api.vekia.fr`, `docs.vekia.fr`, `developer.vekia.fr` and `app.vekia.fr` do not resolve;
`/developers` and `/api` return the site's 404; there is no GitHub organization and no package in any
public registry. ERP/WMS/TMS integration is delivered as a project by Vekia's own team.

Two real machine-readable documents *are* served from `www.vekia.fr`, both belonging to the WordPress
installation behind the corporate site rather than to the product: RFC 8414 OAuth authorization
server metadata and RFC 9728 protected resource metadata, which name an OAuth-gated WordPress MCP
endpoint (`/wp-json/mcp/mcp-oauth-server`, HTTP 403 unauthenticated). They are recorded in
[`well-known/`](well-known/vekia-well-known.yml) and [`mcp/`](mcp/vekia-mcp.yml) with that caveat
stated, and deliberately carry **no** `MCPServer` pointer — see `x-artifacts-without-pointers` in
`apis.yml`.

Source: portfolio company of [serena](https://github.com/api-evangelist/serena) — https://www.vekia.fr/
