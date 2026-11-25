# Validation checklist

No simulation was run during repository preparation. Before scientific use:

1. Verify the pinned upstream revision and all expected patch locations.
2. Verify successful compilation and nonzero exit codes on failure.
3. Confirm initial field normalization and compare initial/final beta in logs.
4. Ensure both runs finish and dumps are complete before reading or exporting them.
5. Compare grid refinement, time sampling and outer boundary sensitivity.
6. Check magnetic divergence and conservation diagnostics; verify horizon quadrature and azimuthal normalization.
7. Exclude or flag nearly zero mass accretion before calculating normalized flux.
8. Check that the proposed MAD configuration actually reaches magnetic arrest; the short duration and axisymmetric grid are limitations.
9. Record upstream revision, patches, compiler versions and output checksums.

The original notebook has destructive cleanup commands and optional Google Drive mounting; run only in dedicated working directories.
