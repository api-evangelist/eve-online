# EVE Online (eve-online)

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
