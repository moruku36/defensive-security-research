# Grafana OSS local validation plan — draft

Checked: 2026-10-08 UTC. No validation has started. This plan contains no vulnerability claim or exploit PoC.

## Start gates

1. Confirm the current Grafana VDP scope, expanded safe-harbor text and participant terms. Preserve dated policy evidence in an appropriate location.
2. Recheck latest release; baseline observed during research: v13.2.3 / 6193dc03311b631b9727b560d24369e683dc396e. Verify downloaded OSS image provenance and digest before execution.
3. Restore an available local execution environment. The research task's shell failed during setup refresh; Docker, WSL and local files could not be inspected. Their availability is unknown.
4. Switch validation work to the user-requested Astra medium only after the parent task explicitly authorizes that stage. A person must understand and run each submitted PoC; model output is not evidence of human validation.

## Environment design

Use a disposable local OSS instance bound only to 127.0.0.1, with a private container network and restricted outbound connectivity after dependency acquisition. Confirm it is inaccessible from the LAN. Use production mode, built-in functionality, synthetic records and locally created test identities. No host filesystem, Docker socket, real cloud credentials, production databases, community plugins or Enterprise features are mounted or connected.

Test identities represent only researcher-owned users and organizations. Setup, port configuration and isolation checks occur before any security test. This is a proposed environment, not an executed or verified configuration.

## First review focus

Start with public source review of one small OSS authorization boundary, such as organization separation or dashboard/folder access. Read documented role behavior first to avoid reporting an intended Viewer datasource capability. Compare documented expectations with handler authorization and organization/resource selection. Select one concrete hypothesis only when it has an in-scope security impact and does not rely on an excluded feature.

Before manual validation, search official public advisories, release notes and related fixes for the same root cause. Record possible prior art; do not infer novelty from an empty search.

## Manual validation limits

On the owned loopback instance, use a small, predetermined set of human-supervised requests against only synthetic resources. Compare an authorized baseline, the proposed boundary check and a negative control. Record exact version, configuration, role, requests, responses and observed impact in confidential storage outside the public repository. Stop when minimal evidence exists.

No automated scanners, fuzz campaigns, broad endpoint enumeration, brute force, load generation, DoS, cloud metadata access, external callback services, service-provider live systems or other people's data. Stop for unexpected outbound access, instability, third-party effects, sensitive data or scope ambiguity. Ask the program a scope question before extending the boundary.

## Exit and record handling

A reproducible result is a confidential candidate, not an accepted finding. Prepare a report only after human reproduction, scope and duplicate checks. Submission remains a separately authorized action. If the hypothesis fails, retain a non-sensitive progress statement without labeling it a vulnerability.

Public progress may state that policy review or a local test was completed, without disclosing an unpublished vulnerability. Never commit confidential evidence to this repository. Ask for the vendor's required written disclosure permission before publishing finding details, and keep stage counts tied to actual vendor evidence.
