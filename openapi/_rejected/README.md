# Harvested here in error — not EVE Online's APIs

These 21 documents were in `openapi/_original/`, the archive that records what the PROVIDER
published. None of them are EVE Online's. They are the Swagger Petstore, OpenAPI tooling test
fixtures (`allow-empty-value`, `frozen-array-input`, `parameter-enum-rendering`, `callbacks`),
and numbered files titled "Demo API", "Test API", "test doc", "Repro API" and
"DDErl REST interface".

**Three of them were being published as EVE Online's own APIs** — `eve-online-pet-api`,
`eve-online-store-api` and `eve-online-user-api`, live on apis.io, carrying the Petstore's
`/pet`, `/store` and `/user` paths and `servers: [http://petstore.swagger.io/v2]`.

EVE Online's real API is the EVE Swagger Interface at `https://esi.evetech.net/latest`, and
seven archive documents describe it — `eve-online-openapi.yml` plus six dated `swagger*.json`
snapshots. Those stay in `_original/`.

Kept rather than deleted: this is the record of what a harvest wrongly collected, and roadmap#2
is about finding exactly this. Deleting it would erase the evidence of the defect along with the
defect.

Moved 2026-08-29, roadmap#2.
