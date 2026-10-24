# go-pcore.github.io

The [Hugo](https://gohugo.io) landing page for **go-pcore**, served at
<https://go-pcore.github.io>.

A single self-contained `layouts/index.html` (inline CSS, 3-way
system/light/dark theme toggle) rendering the repo/phase cards from
`hugo.toml`'s `[[params.phases]]`. Deployed to GitHub Pages by the
`deploy-pages` workflow on every push to `main`.

BSD-3-Clause.

## The design is not here

It comes from the shared Hugo module
[`go-fleettools/landingkit`](https://github.com/go-fleettools/landingkit),
pinned in `go.mod` (Renovate bumps it); `kit.go` keeps `go mod tidy` from
deleting that requirement. `[params.brand]` in `hugo.toml` is read from the logo by
`landingkit brand`. A file under `layouts/partials/` with the name of one of the
kit's would silently override it.
