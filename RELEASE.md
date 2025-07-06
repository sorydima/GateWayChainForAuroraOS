# Release Process

Semantic Versioning **MAJOR.MINOR.PATCH**

1. Ensure `CHANGELOG.md` is updated and all PRs are merged.
2. Bump version in:
   * `GateWayChain.pro`
   * `rpm/specs/gatewaychain.spec`
3. Tag & sign:

```bash
git tag -s vX.Y.Z -m 'GateWayChain vX.Y.Z'
git push origin vX.Y.Z
```

4. Build artifacts:

```bash
git checkout vX.Y.Z
./scripts/release.sh   # builds AppImage, RPM, flatpak
```

5. Draft GitHub release, attach artifacts & SHA256 checksums.
6. Announce on Matrix `#gatewaychain:rechain.network`.

_Last updated: 2025-07-06_
