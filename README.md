# yama-task

事業キャッチアップ・タスク管理の拠点フォルダ。

## フォルダ構成

| フォルダ | 用途 |
|---------|------|
| `tasks/` | タスク・TODO管理 |
| `research/` | 業界動向・競合調査 |
| `docs/` | 社内ドキュメント・議事録 |
| `kpi/` | KPI・データ追跡 |

## タスク管理の使い方

- 長期タスク → `tasks/TODO.md` に記録
- 作業中のセッション → Claude Code のTask機能で進捗追跡
- 完了タスクは `tasks/done/YYYY-MM.md` にアーカイブ

## キャッチアップの使い方

- `research/YYYY-MM-DD-topic.md` で調査メモを保存
- `docs/meetings/YYYY-MM-DD-topic.md` で議事録を保存
- `kpi/YYYY-MM.md` で月次指標を記録

## カスタムコマンド

### `/update-plan` — 企画骨子アップデート

議事録・Slackログなどの最新の議論を渡すと、企画骨子ファイルを自動更新して変更サマリーを出力し、GitHubにpushする。

**使い方：**
```
/update-plan

【企画骨子】docs/2026-05-CSカルテDB企画.md

【議論内容】
（議事録やSlackログをそのままペースト）

【追加資料】
（任意）
```

**何をしてくれるか：**
1. 企画骨子・議論内容を読み込む
2. 決定事項・変更点・持ち越しを特定
3. 骨子ファイルを更新して更新履歴を追記
4. 変更サマリーをチャットに出力
5. `git commit & push` まで自動実行

**関連ファイル：**
- コマンド定義：`.claude/commands/update-plan.md`
- 詳細ドキュメント：`docs/skill-update-plan.md`

---

## Claude への依頼例

```
# 業界ニュースを調べる
「〇〇業界の最新動向を調べてresearch/に保存して」

# 競合調査
「〇〇社の最新情報をまとめてresearch/competitors/に保存して」

# 議事録整理
「この議事録テキストを整理してdocs/meetings/に保存して」

# タスク追加
「〇〇をtasks/TODO.mdに追加して」
```
