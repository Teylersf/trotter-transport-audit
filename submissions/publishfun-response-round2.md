# Response to round 2 minor revision

Paper p_6cq9vk9Ye4pp1QK2. Author: Taylor Kalin. Revised manuscript: version 1.1.1, *Corrections and resource bounds for the Trotter quantum transport algorithm*.

The requested evidence and link amendments are complete. The numerical programs, data, figures, results, resource discussion and both appendices remain unchanged from version 1.1.0. No new scientific conclusion is introduced.

## 1. Public archival identifier and exact snapshot

The existing DOI is correct: https://doi.org/10.5281/zenodo.23770769 . Fresh unauthenticated requests on 29 October 2026 at 16:47:29–16:47:37 UTC returned HTTP 200 from all four authoritative endpoints:

- DataCite: https://api.datacite.org/dois/10.5281/zenodo.23770769 . It reports DOI 10.5281/zenodo.23770769, state `findable`, `isActive: true`, creator `Kalin, Taylor`, publisher `Zenodo`, type `Software`, and the exact code/data title. Registration is timestamped 2026-10-29T16:11:55Z.
- DOI registration agency: https://doi.org/ra/10.5281/zenodo.23770769 . It identifies DataCite as the registration agency.
- DOI resolver: https://doi.org/10.5281/zenodo.23770769 . It redirects successfully to https://zenodo.org/records/23770769 with final HTTP 200.
- Zenodo: https://zenodo.org/api/records/23770769 . It reports the matching record and DOI, `submitted: true` and `state: done`.

Section 7 now provides these direct public verification routes. The safe current receipt is `submissions/zenodo-doi-verification-round2.json` in the public repository, supplementing the earlier `submissions/zenodo-doi-verification.json` and `data/zenodo-code-archive.json`.

The anonymous ZIP download was independently verified as 625,315 bytes, SHA-256 `ef401c3744e4fa2ef7e9139ede5d1d6d07c077ecc513099b711b2a119a3eef68`. It is exactly `git archive` of scientific commit `1fb4be68eecce95b93adb8026c4e3d29fb442583`, computational version 1.0.0. The later manuscript packaging does not change that snapshot. The DOI identifies the code/data archive, not a peer-reviewed article.

The reviewers' `not_found` result does not agree with these direct authoritative observations. Its cause is not known, so no claim about caching or propagation is made. No replacement DOI was minted because the registered identifier already resolves publicly and identifies the correct immutable deposit.

## 2. Journal footnote 13 and Eq. (59)

Section 3.1 now quotes the complete first sentence of journal footnote 13, printed p.11 / PDF p.12, verbatim:

> The $L^2$ norm of any derivative of $f$ is constant over time, equal to its initial value at time $t=0$.

It identifies the matching Appendix B argument at printed p.26 / PDF p.27 immediately after Eq. (65). The same counterexample and theorem limitations apply.

Section 3.1 now prints journal Eq. (59) with its original real-part parentheses and exact locator, printed p.24 / PDF p.25:

$$
P(0)=\frac{1+\Re(\langle\phi|\psi\rangle)}{2},\qquad
P(1)=\frac{1-\Re(\langle\phi|\psi\rangle)}{2}.
$$

The preceding Eq. (58) and the circuit in Fig.13, printed p.25 / PDF p.26, are explicitly identified. These source passages were checked directly in the rendered publisher PDF, whose SHA-256 is `1b8f24ed2bcd4979526977581fc795f80d90a6efeacfbe28e65339cf8b4803e1`, not inferred from an arXiv excerpt. Their attribution to [2] and the distinction between a displayed error and unavailable implementation code remain explicit.

## 3. Publisher link formatting

Section 3.1 replaces the PDF-endpoint hyperlink with the DOI landing URL, https://doi.org/10.1088/2058-9565/ae488e . A plain-text note directs readers to its PDF download action. The malformed identifier ending in `/pdf` is absent from the submitted manuscript. Reference [2] retains the correct journal DOI.

These amendments address all three editorial requests while preserving the checked scientific results and their stated limits.
