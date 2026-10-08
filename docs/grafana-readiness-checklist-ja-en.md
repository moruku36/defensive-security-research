# Grafana OSS readiness / Grafana OSS 準備チェックリスト

Checked / 確認日: 2026-10-08 UTC.

- [x] Current scope and expanded safe harbor reviewed by the coordinating task. Conditional protection; no local-testing exception. / 統括タスクが現行scopeとsafe harbor全文を確認済み。規約遵守が条件で、ローカル特例はありません。
- [x] Official v13.2.3 image digest and version layer checked. / 公式v13.2.3 imageのdigest・version layerを確認済み。
- [x] Isolated lab started, passed a health check, and was stopped. / 隔離ラボは起動・health疎通確認後に停止済み。
- [x] Startup limits verified: 1 CPU, 1 GiB memory, 256 PIDs, read-only root filesystem, loopback binding, no host mounts. / 起動時に1 CPU・1 GiB・256 PID・read-only root・loopback・host mountなしを確認済み。
- [ ] Before the session, recheck the latest release, current terms and isolation. / 手動確認前に最新版・現行規約・隔離を再確認する。
- [ ] Prepare disposable synthetic resources and researcher-owned local identities; confirm applicable OSS functionality. / 使い捨ての架空resourceと本人所有のローカルidentityを用意し、対象OSS機能を確認する。
- [ ] A person understands and personally performs each PoC intended for submission; document AI assistance. / 提出予定PoCは本人が理解・実行し、AI利用を説明する。
- [ ] Keep confidential evidence outside this public repo. Obtain required disclosure permission before publishing details. / 機密証拠は公開repo外に置き、詳細公開前に必要な公開許可を確認する。

Automated scanning/reporting is excluded. No vulnerability checks have been executed. Submitted / Validated / Accepted / Resolved / Publicly credited: **0 / 0 / 0 / 0 / 0**.

自動scan/reportは対象外。脆弱性検証は未実施、実績は全段階 **0件**です。

## Next local session / 次のローカル作業

1. Ask the assistant to resume the local manual session. The assistant starts the lab and checks readiness. / assistantにローカル手動確認の再開を伝える。起動・準備確認はassistantが担当。
2. Read the private checklist, confirm you understand the operation and expected result, then personally perform the small manual checks. Enter any required secrets yourself. / 非公開確認票を読み、操作・期待結果を理解して少数の手動確認を本人が実行。必要な秘密は本人が入力。
3. Confirm actual results with the assistant. The assistant records permitted progress and stops the lab; sensitive evidence remains in confidential storage. / 実結果をassistantと確認。assistantが許可範囲の進捗を記録してラボを停止し、機密証拠は非公開保管。

This public checklist intentionally contains only general preparation and progress. Detailed manual checks are maintained separately in confidential storage.

この公開確認票は一般的な準備・進捗のみを扱います。具体的な手動確認票は非公開保管先にあります。

## Evidence / 確認資料

See [policy and artifact notes](grafana-policy.md) for the verified digest, actual build metadata and verification limits. The patched artifact differs from the public tag commit; full source reproduction and signed attestation remain unverified.

[規約・artifact記録](grafana-policy.md)にdigest、実build metadata、確認範囲を記載。patched artifactと公開tagのcommitは異なり、完全source再現・署名attestationは未確認です。

Official sources / 公式出典:
- [Grafana VDP](https://app.intigriti.com/programs/grafanalabs/grafanalabsvdp/detail)
- [Intigriti Researcher Terms](https://kb.intigriti.com/en/articles/5466165-researcher-terms-conditions)
- [Intigriti Code of Conduct](https://kb.intigriti.com/en/articles/5247238-community-code-of-conduct)
- [Docker Hub 13.2.3 tag](https://hub.docker.com/v2/repositories/grafana/grafana/tags/13.2.3/)
- [Docker Hub latest tag](https://hub.docker.com/v2/repositories/grafana/grafana/tags/latest/)
