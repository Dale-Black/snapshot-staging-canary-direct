# Snapshot staging compatibility corpus

This is a permanent, additive staging fixture for Snapshot. It uses ordinary
Julia and Pluto code and is published only through the managed staging
workflow. New regressions should become small, named cases here (or in a
purpose-built companion staging repository) and remain covered after the bug
is fixed.

The current notebook exercises:

- an unavailable import unrelated to a valid interactive island;
- imports that the island genuinely needs (`Statistics`, a renamed `Base`
  import, and `AbstractPlutoDingetjes.Bonds`);
- a real `PlutoUI.TableOfContents()` with multiple heading levels and a long
  scroll surface;
- semantic Pluto error output without local paths or serialized stack data;
- a WASM slider and derived output;
- collection themes, hard reloads, hash navigation, and fixed shell geometry.

The deployed browser release gate also verifies that the publication points at
the repository's current `main` commit, has an attestation and honest coverage
metadata, and was built by the expected pinned Snapshot engine.
