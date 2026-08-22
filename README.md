# EVE Online (eve-online)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

EVE Online is a massively multiplayer online (MMO) space game published by CCP Games. The EVE Online third-party developer ecosystem is built around the EVE Swagger Interface (ESI), a RESTful HTTP API hosted at esi.evetech.net that exposes the game state for capsuleers to read and write programmatically, the EVE Single Sign-On (SSO) OAuth 2.0 service hosted at login.eveonline.com for delegated authorization with per-scope consent, the Image Server hosted at images.evetech.net for character portraits, corporation logos and item renders, and the Static Data Export (SDE) for the bulk universe, type, and dogma data that does not change between server downtimes.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/eve-online/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/eve-online/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Authentication
- Authorization
- Gaming
- Images
- MMO
- OAuth2
- REST
- SSO
- Static Data

## Timestamps

- **Created:** 2026-05-28
- **Modified:** 2026-05-30

## APIs

### EVE Swagger Interface (ESI)

The EVE Swagger Interface (ESI) is the official RESTful HTTP API for EVE Online third-party development. It covers roughly 180 endpoints across 30 resource families including Universe, Corporation, Character, Fleets, Market, Industry, Contracts, Mail, Assets, Wallet, Killmails, Sovereignty, Wars, Planetary Interaction, Faction Warfare, Dogma, and User Interface. Every request can carry an X-Compatibility-Date header (ISO YYYY-MM-DD) so that clients pin themselves to a known API behavior. Authentication is delegated to EVE SSO using fine-grained OAuth 2.0 scopes (one scope per route family, e.g. esi-wallet.read_character_wallet.v1). Public routes are anonymous; authenticated routes require a JWT access token whose scopes must cover the route. The API enforces a sliding-window per-bucket rate limit and an error rate limit, surfaces caching via Expires/Last-Modified/ETag, and pages large collections with X-Pages headers.

- **Human URL:** [https://developers.eveonline.com/docs/services/esi/](https://developers.eveonline.com/docs/services/esi/)
- **Base URL:** `https://esi.evetech.net/latest`

#### Tags

- Alliance
- Assets
- Calendar
- Character
- Clones
- Contacts
- Contracts
- Corporation
- Dogma
- Faction Warfare
- Fittings
- Fleets
- Incursions
- Industry
- Insurance
- Killmails
- Location
- Loyalty
- Mail
- Market
- Planetary Interaction
- REST
- Routes
- Search
- Skills
- Sovereignty
- Status
- Universe
- User Interface
- Wallet
- Wars

#### Properties

- [Documentation](https://developers.eveonline.com/docs/services/esi/)
- [A P I Explorer](https://developers.eveonline.com/api-explorer)
- [OpenAPI](https://esi.evetech.net/latest/swagger.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [OpenAPI](openapi/eve-online-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/eve-online.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/eve-online.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Swagger](https://esi.evetech.net/ui)
- [Best Practices](https://developers.eveonline.com/docs/services/esi/best-practices/)
- [Rate Limits](https://developers.eveonline.com/docs/services/esi/rate-limiting/)
- [Git Hub Repo](https://github.com/esi/esi-docs)
- [Git Hub Repo](https://github.com/esi/esi-issues)
- [Git Hub Repo](https://github.com/esi/esi-routes)
- [Git Hub Repo](https://github.com/esi/eve-glue)
- [Support Issues](https://github.com/esi/esi-issues)

### EVE Single Sign-On (SSO)

EVE Single Sign-On (SSO) is the OAuth 2.0 authorization service for EVE Online third-party applications, hosted at login.eveonline.com. It supports the Authorization Code flow for confidential (server-side) applications and Authorization Code with PKCE for native and single-page apps that cannot keep a client secret. Access tokens are issued as RS256-signed JWTs whose sub claim is CHARACTER:EVE:<character-id>, whose aud must contain both the application client_id and the literal "EVE Online", and whose scp claim lists the granted ESI scopes. The service publishes RFC 8414 metadata at /.well-known/oauth-authorization-server, including authorization, token, revocation, and JWKS endpoints.

- **Human URL:** [https://developers.eveonline.com/docs/services/sso/](https://developers.eveonline.com/docs/services/sso/)
- **Base URL:** `https://login.eveonline.com`

#### Tags

- Authentication
- Authorization
- JWT
- OAuth2
- OpenID
- PKCE
- SSO

#### Properties

- [Documentation](https://developers.eveonline.com/docs/services/sso/)
- [O Auth2 Metadata](https://login.eveonline.com/.well-known/oauth-authorization-server)
- [Authorization Endpoint](https://login.eveonline.com/v2/oauth/authorize)
- [Token Endpoint](https://login.eveonline.com/v2/oauth/token)
- [J W K S](https://login.eveonline.com/oauth/jwks)
- [Branding](https://web.ccpgamescdn.com/eveonlineassets/developers/eve-sso-login-black-large.png)
- [Postman Collection](collections/eve-online.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/eve-online.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### EVE Image Server (IEC)

The EVE Image Server (also referred to as IEC, the Image Export Collection) is a public, anonymous HTTP service hosted at images.evetech.net that returns portraits and renders for in-game entities. Supported resources include character portraits, corporation and alliance logos, type icons and renders, and faction logos. Image size variants are requested via the size query parameter (32, 64, 128, 256, 512, 1024) and the service is backed by a CDN with strong cache headers.

- **Human URL:** [https://developers.eveonline.com/docs/services/image-server/](https://developers.eveonline.com/docs/services/image-server/)
- **Base URL:** `https://images.evetech.net`

#### Tags

- CDN
- Images
- Portraits
- Renders

#### Properties

- [Documentation](https://developers.eveonline.com/docs/services/image-server/)
- [Postman Collection](collections/eve-online.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/eve-online.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### EVE Static Data Export (SDE)

The EVE Static Data Export (SDE) is the bulk download of all the static reference data behind the EVE universe — types, groups, categories, market groups, dogma attributes, blueprints, regions, constellations, solar systems, stations, certificates, and translations. It is the dataset most third-party developers cache locally rather than calling ESI for every universe lookup. CCP publishes the SDE as YAML, with community projects converting it to SQLite, MySQL, PostgreSQL, MS SQL, JSON, and Parquet for different workloads.

- **Human URL:** [https://developers.eveonline.com/docs/services/sde/](https://developers.eveonline.com/docs/services/sde/)
- **Base URL:** `https://developers.eveonline.com/static-data`

#### Tags

- Bulk Data
- Reference Data
- SDE
- Static Data

#### Properties

- [Documentation](https://developers.eveonline.com/docs/services/sde/)
- [Download](https://developers.eveonline.com/static-data)
- [Community Conversions](https://developers.eveonline.com/docs/community/sde-conversion/)
- [Postman Collection](collections/eve-online.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/eve-online.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### EVE Online Game Client

EVE Online is the underlying massively multiplayer online (MMO) space game from CCP Games. The game client is the consumer of the third-party developer ecosystem — it is where capsuleers actually fly ships, run corporations, and trade on the market that ESI surfaces. The official launcher, client downloads, account management, and game patch notes live on eveonline.com.

- **Human URL:** [https://www.eveonline.com](https://www.eveonline.com)

#### Tags

- Game
- MMO
- Space

#### Properties

- [Website](https://www.eveonline.com)
- [Download](https://www.eveonline.com/download)
- [Account Management](https://secure.eveonline.com/account)
- [Postman Collection](collections/eve-online.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/eve-online.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.eveonline.com)
- [Developer Portal](https://developers.eveonline.com/)
- [Documentation](https://developers.eveonline.com/docs/)
- [Getting Started](https://developers.eveonline.com/docs/services/esi/overview/)
- [A P I Explorer](https://developers.eveonline.com/api-explorer)
- [Swagger](https://esi.evetech.net/ui)
- [OpenAPI](https://esi.evetech.net/latest/swagger.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Blog](https://developers.eveonline.com/blog)
- [Changelog](https://developers.eveonline.com/blog)
- [Support](https://developers.eveonline.com/support/)
- [Support Issues](https://github.com/esi/esi-issues)
- [Git Hub Org](https://github.com/esi)
- [Git Hub Repo](https://github.com/esi/esi-docs)
- [Git Hub Repo](https://github.com/esi/esi-issues)
- [Git Hub Repo](https://github.com/esi/esi-routes)
- [Git Hub Repo](https://github.com/esi/eve-glue)
- [Git Hub Repo](https://github.com/esi/esi-swagger-ui)
- [Authentication](https://developers.eveonline.com/docs/services/sso/)
- [O Auth2](https://login.eveonline.com/.well-known/oauth-authorization-server)
- [Rate Limits](https://developers.eveonline.com/docs/services/esi/rate-limiting/)
- [Best Practices](https://developers.eveonline.com/docs/services/esi/best-practices/)
- [Pagination](https://developers.eveonline.com/docs/services/esi/pagination/)
- [Terms of Service](https://community.eveonline.com/support/policies/terms-of-service-en/)
- [Privacy Policy](https://www.eveonline.com/privacy-policy)
- [License](https://developers.eveonline.com/license-agreement)
- [Community](https://developers.eveonline.com/docs/community/)
- [Discord](https://www.eveonline.com/discord)
- [Forum](https://forums.eveonline.com/)
- [SDK](https://gitlab.com/allianceauth/django-esi)
- [SDK](https://www.npmjs.com/package/@lgriffin/esi.ts)
- [SDK](https://github.com/antihax/goesi)
- [SDK](https://github.com/eseunghwan/eveonline-php)
- [SDK](https://github.com/ueberauth/ueberauth_eve_online)
- [Tools](https://github.com/tweetfleet/neucore)
- [Tools](https://github.com/eveseat/seat)
- [Tools](https://gitlab.com/allianceauth/allianceauth)
- [Tools](https://github.com/wandererltd/community-edition)
- [Tools](https://github.com/kongyo2/eve-online-mcp)
- [Tools](https://github.com/Berman510/EOE_MCP)
- [Tools](https://github.com/pfh59/eve-mcp-server)
- [Community Resources](https://developers.eveonline.com/docs/community/)
- [Status Page](https://www.eveonline.com/news/announcements)
- [Branding](https://web.ccpgamescdn.com/eveonlineassets/developers/eve-sso-login-black-large.png)
- [Public APIs Listing](https://github.com/public-apis/public-apis)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**URL:** http://apievangelist.com
**FN:** CCP Games
**URL:** https://www.ccpgames.com/
