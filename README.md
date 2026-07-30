# dummyforbatten

Throwaway repo for one purpose: rehearsing the **R2 reversal drill** of batten's
publication plan (`docs/general/plan_publicacion.md` §2.2).

R2 is the failure *"release published, assets broken"*. Its reversal is
`gh release edit <tag> --draft=true`, which should make the assets 404 while
machines that already installed keep working from their cache.

That flip cannot be rehearsed in the real repo — a draft does not create the tag,
so the release workflow never fires — and it cannot be rehearsed in a private one
either: an anonymous `curl` gets 404 there always, so the drill "passes" without
proving anything. It needs a repo that is **public and disposable**. This one.

The assets published here are real cross-compiled `batten` binaries, because the
drill doubles as the one smoke test no local server can stand in for: that
`releases/latest/download/<name>` actually resolves, and that the bootstrap's
sha256 check works against a `checksums.txt` served by GitHub rather than by an
`httptest.Server`.

**Nothing here is a real batten release. Do not install from it.**
The real one is at <https://github.com/ArthurZizumbo/batten>.
