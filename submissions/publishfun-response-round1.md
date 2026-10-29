# Response to the round-1 major revision

Paper: p_6cq9vk9Ye4pp1QK2. Author: Taylor Kalin. Revised manuscript: version 1.1.0, *Corrections and resource bounds for the Trotter quantum transport algorithm*.

The revision directly compares the published journal PDF with the supplied arXiv edition, adds source statements and numerical provenance within the paper, and deposits the unchanged computational snapshot in a DOI archive. It preserves the demonstrated positive results and does not claim that printed mistakes entered unavailable author code. The original v1.0.0 GitHub release remains available as a versioned preprint.

## 1. Audit the journal version and report persistence item by item

> Abstract, Sections 1 and 7: audit the open-access QST 11, 025015 (2026) text and add a table stating, for each finding in Sections 4-5, whether it persists, was corrected, or was altered in the version of record.

Completed. A later ordinary request to the official publisher PDF endpoint succeeded; the first version's report of earlier access challenges was accurate for those sessions and did not mean that the article was paywalled. We do not equate an open-access label with a guarantee that an automated request succeeds. We have now directly inspected the downloaded journal text and the relevant rendered equations, so that access distinction no longer limits the revised conclusions.

New Section 3.1 gives the official URL, DOI, publication date, license, byte size, hash, and printed/PDF page map. Its ten-row table records C1-C10 as persisting in the obtained journal edition, with exact equation and footnote locators. Machine-readable evidence is data/journal-comparison.json. The abstract, Introduction, Methods, Limitations and Reference [2] now state the expanded direct inspection. The source file is 2,014,929 bytes, 34 PDF pages, SHA-256 1b8f24ed2bcd4979526977581fc795f80d90a6efeacfbe28e65339cf8b4803e1.

Section 3.1 also credits substantive journal additions: explicit Gaussian-width dependence, conditional optimal-Hamiltonian/block-encoding cost comparisons and nonperiodic-boundary research directions. Section 6 now distinguishes our loader-probability calculation from the width dependence already acknowledged by the journal authors. We do not claim that the journal simply ignored those qualifications.

## 2. Quote each audited statement beside its correction

> Sections 4.1 and 5.1-5.5: quote verbatim each audited statement (Theorem III.4 paragraph and footnote 10, Appendix B opening, Eqs. (A15)-(A16), (5), (17), (39), (43), (A5), (A10)) alongside the counterexample that refutes it.

Completed in new Appendix A. It includes the exact short text fragments and the corresponding source equations, explicit arXiv page/TeX locators, and an audit contrast for each registered group. The reading convention distinguishes verbatim prose, newly typeset reproductions of source mathematics, and our corrections. Section 3.1 supplies the matching journal locations and explicitly reproduces the journal SWAP expression and derivative assertion. Every disputed source formula was checked visually, including inverse superscripts and absolute-value bars. Appendix A attributes the third-party material and excludes it from our own license grants.

The C10 arXiv locator is corrected from the original registry's page 32 to printed page 33, following Eq. (B20). The journal location is printed page 30, following Eq. (83). This locator correction does not alter its numerical or asymptotic conclusion.

## 3. Clarify commutator prior art and the periodic-seam scope

> Section 4.2: state precisely what is new relative to commutator-scaling Trotter theory [6], or reframe the O(N) bound (10)-(12) explicitly as an application, and address whether it holds under the compactly supported, non-periodic-seam data the audited paper assumes.

Completed in Sections 2 and 4.2. Reference [6] is now cited directly in the body, and the finite-grid bound is explicitly an application of established commutator reasoning, not a new general product-formula theorem. Its audit-specific role is to exhibit a sharper coefficient-aware comparator than the crude product-norm estimate used for the advertised factor.

The hypothesis is smooth periodic coefficients. Both editions explicitly include inherently periodic transport. The bound does not transfer to a discontinuously periodized linear velocity merely because the solution is localized away from the seam; a global operator norm still sees that jump. Section 4.2 states that the original linear-coordinate numerical examples would require a specified smooth periodic extension or a different localized argument before this comparator could be applied to them.

Section 2 also engages Burgarth et al., new Reference [9]. A commutator on only the initial state, or even solely along an exact stationary trajectory, is not a universal finite-time error certificate. Mixed split trajectories and additional product/remainder controls matter. Our diagnostic computes its evolution error separately. The separate anisotropic diffusion/convection contribution, arXiv:2603.08799v1, and its distinct Springer proceedings version are identified in Reference [10]; no correction to that separate proceedings text is presumed here.

## 4. Put numerical provenance and norms in the manuscript

> Sections 4.2 and 6: derive or tabulate the provenance of the multi-digit values (commutator norms 67.8300-1782.5930, the 1.2537e-4 splitting error, the Figure 7 magnitudes), including matrix-norm definitions and tolerances, rather than deferring them to the repository.

Completed in new Appendix B. The first table derives the tensor-factorized commutator construction and tabulates all five tested grids, exact spectral operator norms, coefficient-aware bounds, crude commutator bounds and action on the normalized smooth state. It specifies the state, stencil coefficients and largest-singular-value norm. The second table specifies the smooth periodic input, both coefficients, Trotter ordering and time steps, then reports the actual Lie/reference error beside 1024/2048-step Strang-reference differences. Its product-norm coefficient is explicitly distinguished from a full commutator upper bound by the local factor 1/2.

The third table reconstructs the eight-point p=10 circulant Hamiltonian, intended advection sign, exact cyclic shift and two Figure 7 deterministic error magnitudes. It explains why the half-period comparison cannot distinguish advection direction. Software versions, assertion tolerances, normalization and interpretation limits are stated in the appendix. All 51 tabulated numerical cells were checked against the frozen CSV/JSON bytes at the scientific commit, without rerunning author hardware or presenting internal checks as human peer review.

## 5. Deposit the code/data snapshot in a DOI archive

> Section 7: deposit the code and data snapshot in a permanent DOI-minting archive, since reviewers could not verify the GitHub repository or commit 1fb4be68.

Completed. Section 7 and new Reference [11] cite the public Zenodo software/data record, DOI https://doi.org/10.5281/zenodo.23770769 . Its archive is the exact Git snapshot 1fb4be68eecce95b93adb8026c4e3d29fb442583, computational version 1.0.0, including the numerical programs, outputs, original figures, requirements and manifest used in both manuscript versions. The ZIP is 625,315 bytes, SHA-256 ef401c3744e4fa2ef7e9139ede5d1d6d07c077ecc513099b711b2a119a3eef68. An unauthenticated download returned HTTP 200 and matched those bytes. Zenodo's anonymous metadata reports status published and creator Kalin, Taylor. The newer journal concordance and expanded explanation do not change that numerical snapshot.

The GitHub repository, release tag, exact code commit, compiled PDF and three figure URLs were also independently checked through anonymous HTTP reads. Verification receipts are provided as publication evidence, separate from numerical evidence. The earlier inability of a search-based reviewer to discover a recent repository is not treated as proof that it did not exist; the archive supplies a second independently addressable deposit.

## 6. State the remaining theorem boundary explicitly

> Section 4.1: either complete the corrected time-step theorem with explicit time-dependent constants, or state plainly that the original Theorem III.4 conclusion is unproven under the corrected regularity estimate (7)-(8).

We adopt the second option. Section 4.1 now states expressly that the flow/Sobolev estimate alone does not prove original Theorem III.4 or journal Theorem 3.4. A full repair would still need mixed split-trajectory estimates, discrete-to-continuum replacement control, and every additive remainder. The abstract makes this boundary explicit too. The existing longer theorem coefficient's time maxima are identified as candidates to retain, not presented as a completed repaired theorem. Section 4.3 preserves the narrower, checked coupled-refinement arithmetic and distinguishes it from unrestricted refinement at fixed step count.

The revision therefore strengthens the evidence for persistent printed corrections while keeping the scientific conclusion bounded: useful smooth-state behavior and the reported small-grid error magnitudes survive, but several stated identities and justifications need correction. No general impossibility theorem or demonstrated end-to-end quantum advantage is asserted.
