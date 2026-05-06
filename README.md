# Overpass QL EBNF Grammar

A formal grammar for [Overpass Query Language](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_QL) in [W3C EBNF notation](https://www.w3.org/TR/xml/#sec-notation) (the same notation used by the XML 1.0 specification).

## What this is for

The grammar is useful for:

- **Generating queries** — use it as a reference for what combinations of syntax are valid when building tools that produce Overpass QL
- **Validating queries** — check whether a query is syntactically valid before sending it to the API
- **Browsing the language** — the [Railroad Diagram Generator](https://bottlecaps.de/rr/ui) renders the grammar as interactive railroad diagrams, which may be easier to read than the raw EBNF

## How to use it

Paste the contents of `overpassql.ebnf` into the [Railroad Diagram Generator](https://bottlecaps.de/rr/ui) to browse the grammar visually or check it for errors. The [REx Parser Generator](https://bottlecaps.de/rex/) accepts the same notation and can produce a parser if needed.

Transformations to other EBNF-like grammars should be relatively straightforward if you plan to use a different parser implementation.

## How not to use it

Please do not use this grammar to abuse public Overpass servers by sending large volumes of automated queries. If you have a use case that depends on a lot of Overpass traffic, consider running your own local Overpass instance using [the original source code](https://github.com/drolbr/overpass-api) or [one of the container images](https://github.com/b1tw153/overpass-api#installation).

## Scope and accuracy

The grammar covers features documented in the [Overpass QL wiki](https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_QL). The wiki is not always reliable, so the grammar has been verified against the Overpass API source code and tested against a live instance running v0.7.62.11. Features accepted by the implementation but absent from the wiki are excluded.

## Contributing

If you find an error or a gap, please open an issue.
