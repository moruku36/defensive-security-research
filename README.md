# Defensive Security Research

公開OSSの防御研究に向けた公式規約調査、安全な検証計画、公開を許可された実績の記録です。研究対象の順序は **Grafana OSS → GitLab → Kubernetes** です。

This repository records official policy research, safe validation plans, and explicitly authorized public achievements for defensive research on open source software. Target order: **Grafana OSS → GitLab → Kubernetes**.

## Status / 現在の状態

As of 2026-10-08: policy research only; no active validation, report submission, or public credit.

| Stage / 段階 | Count / 件数 |
|---|---:|
| Submitted / 提出済み | 0 |
| Validated / 技術的妥当性確認 | 0 |
| Accepted / プログラム受理 | 0 |
| Resolved / 修正完了 | 0 |
| Publicly credited / 公開謝辞 | 0 |

These stages are tracked separately using the program's actual status and dated evidence. Submitted reports, duplicate reports, and unverified hypotheses do not count as accepted findings. Findings are goals, not guarantees.

上記の各段階はプログラムの実際の状態と日付付きの証拠に基づいて別々に記録します。提出、重複、未検証の仮説を受理実績に数えません。発見件数は目標であり保証ではありません。

## Publication rules / 公開原則

- Publish official-source research, general safety plans, non-sensitive progress, and vendor-authorized public acknowledgements only.
- Never commit unfixed vulnerability details, reproducible exploit PoCs, private submissions or communications, secrets, or personal data, even temporarily.
- Keep sensitive validation records outside this public repository in a separately approved confidential storage location. A private repository alone does not grant vendor permission to store confidential program data with a third party.
- Acceptance or a fix does not independently grant disclosure permission. Obtain the program's required written permission before publishing finding details; cite authorized public advisories or credits within that permission.
- Do not create accounts, submit reports, or test third-party live services without the applicable authorization. Scope and policy must be checked again before validation and submission.

公開するのは公式資料の調査、一般的な安全計画、機密を含まない進捗、ベンダーが公開を認めた謝辞のみです。未修正の具体的脆弱性、再現PoC、非公開報告・通信、秘密、個人データは一度もcommitしません。機密記録は別の許可された非公開保管先に分離します。private repoであること自体は第三者保管の許可になりません。受理・修正だけで公開可とは扱わず、規約が要求する書面の公開許可を確認します。

## Official entry points / 公式出典

Checked / 確認日: **2026-10-08 (UTC)**. Program policies can change.

1. Grafana OSS: [Grafana VDP](https://app.intigriti.com/programs/grafanalabs/grafanalabsvdp/detail), [Security policy](https://github.com/grafana/grafana/security/policy). Public VDP via Intigriti; no monetary reward. See [policy notes](docs/grafana-policy.md) and [validation plan](docs/grafana-validation-plan.md).
2. GitLab: [HackerOne program](https://hackerone.com/gitlab), [official policy update](https://about.gitlab.com/blog/gitlab-bug-bounty-program-policy-updates/). Full current platform scope must be checked before any validation.
3. Kubernetes: [official security reporting](https://kubernetes.io/docs/reference/issues-security/security/), [HackerOne program](https://hackerone.com/kubernetes). Full current platform scope must be checked before any validation.

Next: resolve Grafana safe-harbor full-text verification and local runtime availability, then review a human-supervised local-only plan before starting validation.

次の行動: Grafana固有safe harbor全文とローカル実行環境を確認し、本人が関与するローカル限定の計画を見直してから検証を開始します。
