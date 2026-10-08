# Grafana OSS policy research

確認日 / Checked: 2026-10-08 UTC. 調査段階。未検証・未提出。

## Scope and authorization

[Grafana VDP](https://app.intigriti.com/programs/grafanalabs/grafanalabsvdp/detail) lists grafana/grafana source code as Tier 1 and requires the latest released version (main only when a product has no releases). It displays that safe harbour applies, but the full expanded "Show safe harbour" text could not be retrieved by the research browser. Program-specific promises, exceptions, and third-party coverage remain unverified.

[Intigriti Researcher Terms](https://kb.intigriti.com/en/articles/5466165-researcher-terms-conditions), sections 3 and 5, condition authorization on acceptance and compliance, access to the program, active program status, and in-scope assets. Sections 6 and 10 prohibit excessive exploitation, third-party infiltration, disruption, and unnecessary access to others' data. Section 10.3.5 restricts third-party storage and subprocessors for Company Data absent prior permission. These general terms do not substitute for the unexpanded Grafana safe-harbor clause.

## AI and excluded approaches

Grafana permits AI assistance but requires human accountability and a human-run PoC on an in-scope asset. Automated scanning or reporting is out of scope. AI-assisted public-source review and planning are the initial approach; autonomous scanning, automatic submission, or AI-only verification are excluded.

[Intigriti Code of Conduct](https://kb.intigriti.com/en/articles/5247238-community-code-of-conduct) additionally requires personal discovery, testing and understanding, accuracy, and disclosure of when and how AI was used.

Grafana excludes expected Viewer datasource-query capabilities, datasource-proxy SSRF, deliberately malicious datasource data, community plugins, Enterprise-dependent issues and development-mode features, among other cases. This project also excludes all DoS, brute force and live-service testing as its own narrower safety limit.

## Duplicate handling

[Intigriti Triage Standards](https://kb.intigriti.com/en/articles/10335710-intigriti-triage-standards), section 5: the same root cause with a unified fix is normally one finding; additional impact may warrant assessment; regressions and real fix bypasses may be new findings. An internally known issue may become a duplicate after initial triage. Public advisory searches cannot prove uniqueness because private reports and internal issues are invisible. No duplicate outcome or credit is guaranteed.

## Reporting and public credit

[Grafana SECURITY.md](https://github.com/grafana/grafana/security/policy): prefer Intigriti; only reports through Intigriti are eligible for the Hall of Fame. Email security@grafana.com is also accepted, but email reports are not Hall-of-Fame eligible. The public VDP does not pay bounties.

Report details remain confidential until the required written disclosure agreement; the program asks researchers to wait for a released fix and confirmation before disclosure. A public credit, advisory or CVE can be cited only within its authorized public information. Submitted, Validated, Accepted, Resolved and Publicly credited are separate evidence states, currently all zero.

## Version baseline

On the check date, [releases/latest](https://github.com/grafana/grafana/releases/latest) redirected to [v13.2.3](https://github.com/grafana/grafana/releases/tag/v13.2.3), commit [6193dc03311b631b9727b560d24369e683dc396e](https://github.com/grafana/grafana/commit/6193dc03311b631b9727b560d24369e683dc396e). Recheck before validation and submission. Container digest has not been verified.

[Official Docker documentation](https://grafana.com/docs/grafana/latest/setup-grafana/installation/docker/) identifies grafana/grafana as OSS and says grafana/grafana-oss stops receiving updates starting with 12.4.0. Use the OSS image, a checked release tag and verified digest; avoid copying the documentation's Enterprise/default-public-port examples unchanged.
