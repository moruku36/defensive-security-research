# Grafana OSS local validation plan — draft

Checked: 2026-10-08 UTC. No validation has started. This plan contains no vulnerability claim or exploit PoC.

## Start gates

1. The coordinating task confirmed the expanded Grafana safe-harbor text on 2026-10-08. Recheck current scope and participant terms before execution; there is no local-testing exemption. Preserve dated policy evidence.
2. Recheck the latest release before validation and submission. Use the verified official image digest and record the actual build metadata. The official patched-image build commit differs from the public release tag; complete source reproduction and signed attestation remain unverified. See [artifact notes](grafana-policy.md#official-artifact-and-lab-preparation--公式artifactとラボ準備).
3. Local runtime readiness was demonstrated by the coordinating task: the isolated lab started, passed a health check and was stopped. The assistant handles restart, isolation checks and shutdown for the manual session.
4. A person must understand and personally run each PoC intended for submission, confirm the actual result and explain AI assistance. Prepare the private manual checklist before the session. The researcher supplies any required secret input.

## Environment design

Use a disposable local OSS instance bound only to 127.0.0.1, with a private container network and restricted outbound connectivity after dependency acquisition. Confirm it is inaccessible from the LAN. Use production mode, built-in functionality, synthetic records and locally created test identities. No host filesystem, Docker socket, real cloud credentials, production databases, community plugins or Enterprise features are mounted or connected.

Test identities represent only researcher-owned users and organizations. Setup, port configuration and isolation checks occur before any security test. The coordinating task verified startup with 1 CPU, 1 GiB memory, a 256-PID limit, read-only root filesystem, loopback binding and no host mounts. The lab is stopped. This readiness check does not demonstrate a security finding; recheck isolation when restarting.

## First review focus

Start with public source review of one small OSS authorization boundary, such as organization separation or dashboard/folder access. Read documented role behavior first to avoid reporting an intended Viewer datasource capability. Compare documented expectations with handler authorization and organization/resource selection. Select one concrete hypothesis only when it has an in-scope security impact and does not rely on an excluded feature.

Before manual validation, search official public advisories, release notes and related fixes for the same root cause. Record possible prior art; do not infer novelty from an empty search.

## Manual validation limits

On the owned loopback instance, use a small, predetermined set of human-supervised requests against only synthetic resources. Compare an authorized baseline, the proposed boundary check and a negative control. Record exact version, configuration, role, requests, responses and observed impact in confidential storage outside the public repository. Stop when minimal evidence exists.

No automated scanners, fuzz campaigns, broad endpoint enumeration, brute force, load generation, DoS, cloud metadata access, external callback services, service-provider live systems or other people's data. Stop for unexpected outbound access, instability, third-party effects, sensitive data or scope ambiguity. Ask the program a scope question before extending the boundary.

## Exit and record handling

A reproducible result is a confidential candidate, not an accepted finding. Prepare a report only after human reproduction, scope and duplicate checks. Submission remains a separately authorized action. If the hypothesis fails, retain a non-sensitive progress statement without labeling it a vulnerability.

Public progress may state that policy review or a local test was completed, without disclosing an unpublished vulnerability. Never commit confidential evidence to this repository. Ask for the vendor's required written disclosure permission before publishing finding details, and keep stage counts tied to actual vendor evidence.
