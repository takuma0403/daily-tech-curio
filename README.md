# tech-ideas-daily — 導入メモ

毎日1回、尖った技術知見カードを3枚生成して Markdown に記録するスキル。

## 中身
- `SKILL.md` — スキル本体（実行手順・発想エンジン・凡庸キル・採否ルーブリック・出力フォーマット・記録の仕組み）
- `references/examples.md` — お手本の3枚（目標温度）。生成時にこの温度へ合わせる
- 別フォルダ `tech-ideas/` — 記録が溜まる先のサンプル（`index.md` ＋ `daily/2026-06-26.md`）

## セットアップ
1. このフォルダを定期タスクのスキルとして登録する。
   - **Cowork（推奨・手軽）**: Coworkで `/schedule` → このSKILLの内容をプロンプトに、頻度を「毎日」に。`OUTPUT_DIR` をローカルの `~/tech-ideas/` に。
   - **クラウド定期タスク（PC不要で確実）**: `claude.ai/code/scheduled` で毎日実行を作成。`OUTPUT_DIR` は接続済みリポジトリやNotionに。
2. `SKILL.md` の「設定（出力先）」の `OUTPUT_DIR` を実際のパスに置き換える。
3. 初回は手動実行して、`references/examples.md` の温度に届いているか確認。薄ければ「凡庸キル」「多産→選抜」が効いているか調整。

## 記録の読み方
- 全体を見渡す → `tech-ideas/index.md`（最新が上、各カードのフック一行付き）
- その日の全文 → `tech-ideas/daily/YYYY-MM-DD.md`
- 過去に何を扱ったかは index と daily が記録なので、重複回避もここを読んで行う。

## チューニングの勘所
- 飽きてきたら `SKILL.md` の「発想エンジン（moves）」「レンズ」「アンカー領域」を足す/差し替える。
- 凡庸が混じったら「凡庸キル・リスト」に具体例を追記する。
- 温度を変えたいときは `references/examples.md` を入れ替えるのが一番効く（お手本が温度を決める）。
