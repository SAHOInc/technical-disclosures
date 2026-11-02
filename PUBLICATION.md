# Publication workflow · 发布流程 · 公開手順

## English

### 1. Prepare outside the public repository

Copy [the template](templates/disclosure-template.md) into a private drafting location. Replace every placeholder with actual implementation facts. Use Peng Bo as the author and CC BY 4.0 for original documentation, unless separately indicated. Confirm the right to share all included material before public upload.

Use a stable ID such as `TD-0001`, a generic title, and a path such as `speech-translation/response-card-interaction.md`. These are naming examples, not disclosed implementations. Include architecture, state transitions, algorithms or pseudocode, reproducible examples, parameters, failure handling, variations and dated references. Record which language is authoritative and review the other two translations.

### 2. Publish the technical document

Upload only approved public material. Public commits and public pull requests are already publication; a draft Release does not keep committed files confidential. Add a catalog row with the real first public URL and timestamp. Do not invent dates, inventorship, test results, or DOI values.

### 3. Enable Zenodo before the Release

1. Sign in to [Zenodo](https://zenodo.org/) using GitHub and review the requested OAuth permissions.
2. Open the profile menu → GitHub → Sync now.
3. Find **SAHOInc/technical-disclosures** and enable its toggle. Keep other repositories disabled.
4. Verify the enabled state before publishing a Release. Older releases are not automatically backfilled.
5. Set accurate title, creators, description, keywords, resource type and license. This is a collection of technical documents; do not describe it as an executable software package. If using `.zenodo.json`, follow [the official schema](https://developers.zenodo.org/#add-metadata-to-your-github-repository-release). Do not commit placeholder metadata. If both `.zenodo.json` and `CITATION.cff` are present, Zenodo uses `.zenodo.json`.

### 4. Release one reviewed disclosure or coherent batch

Choose a new tag such as `v1.0.0` at the reviewed commit. Publish a normal Release after Zenodo is enabled; do not rely on commits, tags alone, draft Releases or prereleases to trigger archiving. List each new/changed technical document and revision in the Release Notes. The archive contains the entire tagged repository.

### 5. Verify the archive and preserve evidence

1. Check the repository on Zenodo for a successful archived record. A GitHub Release alone is not proof of successful ingestion.
2. Open the DOI landing page. Verify the tag, commit, authors, license, publication date, public access and downloaded archive contents.
3. Keep the exact version DOI and, separately, the concept DOI. Download the archive, Release Notes and record metadata. Compute and retain SHA-256 checksums for your saved files; a checksum verifies integrity, not publication time.
4. Update `CATALOG.md` and add a DOI link to the Release Notes after verification. Do not rewrite the published tag or silently replace historical technical content.
5. Corrections to technical content need a new revision and a new Release. Keep earlier versions and explain the change.
6. If archiving fails, inspect Zenodo's integration error, correct metadata and follow the official recovery guidance. Do not label the entry archived until verified.
7. Optionally publish a public announcement linking the verified DOI; retain its permalink. Announcement text should identify the technical subject and version and invite technical discussion.

## 中文

### 1. 在非公开位置准备

复制[三语模板](templates/disclosure-template.md)，以真实实现替换全部占位符。原创文档默认署名 Peng Bo 并采用 CC BY 4.0（另有标注除外），确认所含材料可公开。

使用稳定编号（如 `TD-0001`）、通用技术名称和稳定路径。记录架构、状态转换、算法或伪代码、可复现示例、参数、故障处理、替代实现和带日期的参考资料。上述编号与首页主题仅为命名示例。注明权威语言，核对另两种语言的译文。

### 2. 公开技术文档

只上传已确定可公开的材料。公开 Commit 和公开 PR 已经构成公开，Release 草稿不会使已提交文件保密。目录中记录真实首次公开网址及时间；不虚构公开日期、发明人、测试结果或 DOI。

### 3. 在发布 Release 之前启用 Zenodo

通过 GitHub 登录 Zenodo，审阅 OAuth 权限。在个人菜单选择 GitHub → Sync now，仅开启 **SAHOInc/technical-disclosures** 并核实开启状态。历史 Release 不会自动补归档。准确设置标题、作者、摘要、关键词、资源类型和许可。本仓库是技术文档集合，不是可执行软件包。使用 `.zenodo.json` 时遵守官方格式，不上传占位元数据；它与 `CITATION.cff` 同时存在时，以 `.zenodo.json` 为准。

### 4. 发布经核对的单项技术或关联批次

在核对过的 Commit 上创建新标签（如 `v1.0.0`），再发布正式 Release。不要依赖普通 Commit、单独标签、草稿或预发布触发归档。Release Notes 列明新增或修改的技术、文档路径和修订号。Zenodo 保存整个标签对应的仓库快照。

### 5. 核实归档并保存证据

核实 Zenodo 显示归档成功，打开 DOI 页面，检查标签、Commit、作者、许可、日期、公开访问和下载的实际文件。分别保存版本 DOI 与概念 DOI、归档文件、Release Notes 和元数据，并保存下载文件的 SHA-256 校验值；校验值仅证明完整性，不证明公开时间。之后更新目录和 Release Notes 的 DOI 链接，不移动已发布标签。技术更正通过新修订、新 Release 保留历史。归档失败时检查错误并依照官方指引修复，核实前不标记为成功。可选公开公告应链接已核实 DOI，并保存公告网址。

## 日本語

### 1. 非公開の場所で準備

[三言語テンプレート](templates/disclosure-template.md)をコピーし、実装の事実で全項目を埋めます。別途記載がなければオリジナル文書の著者を Peng Bo、ライセンスを CC BY 4.0 とし、資料を共有する権限をアップロード前に確認します。

固定 ID（例：`TD-0001`）、一般的な技術名称、固定パスを使用します。構成、状態遷移、アルゴリズムや疑似コード、再現例、パラメーター、障害処理、代替実装、日付付き参考資料を記載します。例示は実際の技術開示ではありません。正本の言語を明示し、他の二言語を確認します。

### 2. 技術文書を公開

公開可能と決定した資料のみアップロードします。公開コミットや公開 PR の時点で内容は公開され、Release の下書きでも機密にはなりません。一覧に実際の初回公開 URL と日時を記録し、日付、発明者、試験結果、DOI を捏造しません。

### 3. Release より先に Zenodo を有効化

GitHub で Zenodo にログインし、OAuth 権限を確認します。プロフィールメニュー → GitHub → Sync now を選び、**SAHOInc/technical-disclosures** のみを有効にして状態を確認します。過去の Release は自動で遡及保存されません。題名、著者、概要、キーワード、資料種別、ライセンスを正しく設定します。本リポジトリは技術文書集であり、実行可能なソフトウェアではありません。`.zenodo.json` は公式仕様に従い、仮の値を公開しません。`CITATION.cff` と両方ある場合、Zenodo は `.zenodo.json` を使用します。

### 4. 確認済み技術または関連文書群を公開

確認済みコミットに新しいタグ（例：`v1.0.0`）を作り、正式な Release を公開します。通常のコミット、タグのみ、下書き、プレリリースでの自動保存を前提にしません。Release Notes に追加・変更した技術、文書パス、改訂番号を列記します。アーカイブはタグに対応するリポジトリ全体です。

### 5. アーカイブの確認と証拠保存

Zenodo の成功表示と DOI ページを確認し、タグ、コミット、著者、ライセンス、日時、公開アクセス、実際の保存ファイルを照合します。バージョン DOI とコンセプト DOI を区別し、アーカイブ、Release Notes、メタデータ、保存ファイルの SHA-256 を保管します。ハッシュ値は完全性の確認用であり公開時刻の証明ではありません。確認後に一覧と Release Notes へ DOI を追記し、公開済みタグは移動しません。技術内容の訂正は新しい改訂と Release として履歴を残します。保存に失敗した場合は公式手順に従い、確認前に成功扱いしません。任意の公開告知では確認済み DOI を案内し、告知 URL を保存します。

## Release Notes template / 发布说明模板 / 公開説明テンプレート

```text
Technical disclosures — <version>
Technical scope / 技术范围 / 技術範囲: <actual scope>
Added or revised / 新增或修改 / 追加・変更:
- <ID> — <title EN / 中文 / 日本語> — <path> — <revision>
Reviewed commit: <full commit SHA>
Changes since previous version: <actual changes>
Zenodo archival status: Pending verification
Version DOI: <add only after verification>
Concept DOI: <add only after verification>
```

## Official references / 官方参考 / 公式資料

- [Enable repository](https://help.zenodo.org/docs/github/enable-repository/)
- [Archive a release](https://help.zenodo.org/docs/github/archive-software/github-upload/)
- [Metadata formats](https://help.zenodo.org/docs/github/describe-software/)
