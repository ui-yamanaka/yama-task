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
