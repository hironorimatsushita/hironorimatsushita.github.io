# hironorimatsushita.github.io

個人公開サイト https://hironorimatsushita.github.io のソースを置くリポです。本人専用の個人ツール(gcal-weekly等)を外部サービスへ登録する時に求められるホームページURL・プライバシーポリシーURLを提供します。

## プロジェクト概要

- 用途: OAuth同意画面の本番公開など、外部サービスが「ホームページURL」「プライバシーポリシーURL」「承認済みドメイン」を要求する時の受け皿として再利用する(初出=gcal-weeklyのOAuth公開、2026-08-31新設)
- 公開: GitHub Pages(mainブランチの直下を配信、ビルドはJekyllのlegacy方式)

## ワークスペース構成

- `index.html`: ホームページ(日英)。公開中のアプリは本人専用で一般向けサービスではない旨を書く
- `privacy.html`: gcal-weeklyのプライバシーポリシー(日英)
- `.gitignore`: バイナリ除外のcanonicalブロック(sync-claude-review管理)。このリポはバイナリを持たない(repos.jsonで`binaries_created=false`)

## 重要な制約

- 公開リポかつ公開サイトなので、機微情報(秘密値・第三者の名前・業務の内部情報)を置かない
- GitHub Pagesで既定有効のプラグインjekyll-optional-front-matterにより、front matterの無いmd(このCLAUDE.mdを含む)もページとして配信されうる。mdを足す・直す時は公開されても困らない内容に限る
- 新しいアプリのポリシーは`privacy.html`への追記でなく、アプリ別のページを足す方向で検討する

## Known Pitfalls

横断の罠は`~/.claude/memory/pitfalls-*.md`(索引=`~/.claude/memory/MEMORY.md`)。ここには写さない。

<!-- この行より下には、このリポ固有の罠だけを`- YYYY-MM-DD: 内容(起源: PR#N)`形式で書く。2リポ以上で再発した罠の昇格先は`~/Projects/workspace-meta/.claude/rules/knowledge-placement.md`「昇格判定」に従う。重複・60日参照なし・ルール化済みはenv-audit Phase 1で陳腐化検出されarchive候補になる -->
