# actor-asobi

`asobi`（遊び）は freed-time / play / cultural-expression の actor repository です。
旧 `etzhayyim/root/20-actors/asobi` の実装と契約を、この flat west project に統合します。

## Repository contract

- 正規メタデータ・identity・依存関係・schema・seed は EDN。
- Clojure/ClojureScript source は `src/asobi/`、test は `test/asobi/`。
- JSON/JSON-LD は外部互換 wire のみに限定し、`wire/` または `.well-known/` に置く。
- Go/TinyGo と shell runner は deprecated。test entry point は `run_tests.cljk`。
- dependency pin は `dependencies.edn` と `deps.edn` で明示する。

## Layout

    manifest.edn
    identity.edn
    dependencies.edn
    repository-contracts.edn
    data/
    schema/
    src/asobi/
    test/asobi/
    wire/

## Test

    kbb run_tests.cljk
    kbb -M:test

Deployment metadata is canonical in `kotoba.app.edn`; its source entry is
`src/asobi/mesh.cljk`.
