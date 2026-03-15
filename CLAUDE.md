# CLAUDE.md — MK LIFETIME GYM プロジェクト引き継ぎ資料

> Claude Code セッション開始時にこのファイルを最初に読むこと。
> 最終更新: 2026年3月

---

## プロジェクト概要

**MK LIFETIME GYM** は横浜市緑区・中山駅徒歩3分に2025年6月1日グランドオープンしたフィットネスジム。

| 項目 | 内容 |
|---|---|
| 正式ジム名 | MK LIFETIME GYM |
| 場所 | 横浜市緑区・中山駅 徒歩3分（詳細住所は決定後更新） |
| オープン日 | 2025年6月1日 |
| 投資家 / サービスデザイナー | 村上 政志 |
| ヘッドトレーナー | 岡本 真（リングネーム：川崎 真琴） |

---

## トレーナープロフィール

- **本名**: 岡本 真 / **リングネーム**: 川崎 真琴
- 広島県尾道市出身、1984年生まれ
- 2012年 プロボクシングデビュー
- 2022年4月 第40代 日本スーパーウェルター級王座獲得（後楽園ホール）
- 所属：RK蒲田ボクシングファミリー
- 戦績：プロ24戦 13勝（2KO）9敗2分

---

## ブランド設計

### MK LIFETIME GYM（現行・本番サイト）
- **ターゲット**: 40代女性・初心者・健康志向の方
- **カラー**: ホワイト / クリーム / テラコッタ（`#b07d62`）
- **トーン**: 上品・ナチュラル・温かみ

### BATTLE FITNESS GYM（将来構想）
- **ターゲット**: 競技アスリート・格闘技志向
- **カラー**: ダーク / レッド
- **状態**: 未着手

---

## 公式サービスメニュー（料金はすべて税込）

| プラン | 料金 | 条件 |
|---|---|---|
| スタンダード（男性） | ¥11,000／月 | 通い放題 |
| スタンダード（女性） | ¥9,900／月 | 通い放題 |
| キッズプラン | ¥6,600／月 | 週2回 |
| パーソナルプラン | ¥50,000／月 | 月8セッション |

---

## オンライン情報

| 種別 | 内容 |
|---|---|
| **Webサイト** | https://mk-lifetime-gym.jp |
| **メインドメイン** | mk-lifetime-gym.jp（お名前.comで取得済み） |
| **サブドメイン** | mk-lifetime-gym.com（同時取得・転送用） |
| **メール** | info@mk-lifetime-gym.jp |
| **Instagram** | @mk-lifetime-gym |
| **X / Twitter** | @mk-lifetime-gym |
| **GitHubリポジトリ** | https://github.com/seishimurakami/gym |
| **GitHub Pages** | seishimurakami.github.io → mk-lifetime-gym.jp |

---

## リポジトリ構成

```
gym/
├── index.html          # MK LIFETIME GYM メインサイト（本番稼働中）
├── CNAME               # mk-lifetime-gym.jp（GitHub Pages カスタムドメイン）
└── images/
    ├── hero_belt_shorts.jpg    # ヒーロー背景画像
    ├── trainer_belt_robe.jpg   # トレーナー写真（ローブ着用）
    ├── fight_scene.jpg         # 試合シーン写真
    └── training.jpg            # トレーニング写真
```

---

## index.html 構成（セクション順）

1. **NAV** — ロゴ（MK LIFETIME GYM）＋メニューリンク
2. **HERO** — フルスクリーン、ヒーロー画像、キャッチコピー、CTAボタン
3. **OPEN RIBBON** — グランドオープン告知バナー
4. **STATS** — 統計数値3点
5. **CONCEPT** — ジムのコンセプト説明
6. **CONCEPT CARDS** — 特徴カード（初心者歓迎・元王者・少人数）
7. **TARGET** — こんな方にぴったり（チェックリスト）
8. **TRAINER PHOTO** — トレーナー写真
9. **TRAINER CAPTION** — プロフィール＋キャリア年表
10. **FIGHT PHOTO** — 試合写真フルワイド
11. **PROGRAMS** — 3プログラム（ボディメイク / フィットネスボクシング / ライフタイムヘルスケア）
12. **PHOTO PAIR** — 写真＋「40s こそ、本番。」テキスト
13. **MEMBER'S VOICE** — 会員の声 3件（仮）
14. **PLAN** — 料金プラン 4種
15. **OPEN** — グランドオープンCTAセクション
16. **ACCESS** — アクセス・連絡先（住所／営業時間／メール／Instagram／X）
17. **FOOTER** — ロゴ、リンク、コピーライト

---

## デザイン仕様

### CSS変数
```css
--white:        #ffffff
--cream:        #faf8f5
--light:        #f3efe9
--warm:         #ede8e0
--border:       #e0d8ce
--text:         #2c2520
--muted:        #9a8f85
--accent:       #b07d62   /* メインアクセント（テラコッタ） */
--accent-light: #d4a98a
--accent-dark:  #8a5e45
--green:        #7a9e7e
```

### フォント
- **見出し**: Cormorant Garamond（Google Fonts）
- **本文**: Noto Sans JP（Google Fonts）

### レイアウト
- スマートフォン最適化（max-width: 430px、中央寄せ）
- PCでは中央カラムとして表示

### アニメーション
- ヒーロー画像: `zoomOut` 10秒（scale 1.06 → 1.0）
- スクロール表示: `.reveal` クラス + IntersectionObserver
  - `.reveal` → `opacity:0; transform:translateY(24px)`
  - `.reveal.visible` → `opacity:1; transform:none`
  - threshold: 0.12

---

## 既知の課題・要対応事項

| 優先度 | 項目 | 詳細 |
|---|---|---|
| 🔴 高 | 詳細住所の更新 | 「詳細住所は決定後更新予定」を実住所に変更 |
| 🔴 高 | 電話番号の追加 | 現在「メールにて受付中」と仮表記 |
| 🔴 高 | 営業時間の確定 | 「10:00〜22:00（要確認）」を正式時間に変更 |
| 🟡 中 | HTTPS強制 | GitHub Pages設定で「Enforce HTTPS」をON（DNS確認完了後） |
| 🟡 中 | MEMBER'S VOICE | 現在は仮の声。実際の会員コメントに差し替え |
| 🟡 中 | OGP / SNSメタタグ | SNSシェア時の画像・タイトル設定が未実装 |
| 🟡 中 | Google Analytics | アクセス解析未設定 |
| 🟢 低 | BATTLE FITNESS GYM サイト | 別ブランチまたは別リポジトリで構築予定 |
| 🟢 低 | お問い合わせフォーム | 現在はmailtoリンクのみ。Formspree等の導入を検討 |

---

## GitHub / デプロイ

- **ホスティング**: GitHub Pages（無料）
- **公開ブランチ**: `main`
- **カスタムドメイン**: `mk-lifetime-gym.jp`（CNAMEファイルで設定済み）
- **HTTPS**: TLS証明書はLet's Encryptを自動取得（設定後15分以内）
- **デプロイ方法**: `main` ブランチへのpushで自動反映

### DNS設定（お名前.com）
```
# Aレコード（apex ドメイン）
@  A  185.199.108.153
@  A  185.199.109.153
@  A  185.199.110.153
@  A  185.199.111.153

# CNAMEレコード（wwwサブドメイン）
www  CNAME  seishimurakami.github.io.
```

---

## 財務計画

- **収支計画Excelファイル**: `MK_LIFETIME_GYM_収支計画.xlsx`
  - シート①: 前提条件（編集可能パラメータ）
  - シート②: 月次収支計画（36ヶ月）
  - シート③: 年次サマリー（3年）
- 会員上限: 100名
- **注意**: 年次収支シートのE6（3年目期末会員数）とE9（3年目月平均売上）が抜けやすいバグあり
  - E6 = `ROUND(D6*(1-退会率)^12 + 安定期獲得数*12, 0)`
  - E9 = `E6 * B7`
  - E10 = `E9 * 12`

---

## Claude Codeでよく行う作業

```bash
# リポジトリのクローン（初回）
git clone https://github.com/seishimurakami/gym.git
cd gym

# ファイル編集後のデプロイ
git add .
git commit -m "update: 変更内容を記述"
git push origin main

# ファイル名変更
git mv 旧ファイル名 新ファイル名
git commit -m "rename: ファイル名変更"
git push origin main
```

---

## 次のアクション候補

1. **住所・電話番号・営業時間を確定してindex.htmlに反映**
2. **Enforce HTTPS をGitHub Pages設定でONにする**
3. **OGPメタタグを追加**（SNSシェア時の見た目改善）
4. **Google Analyticsの設置**
5. **お問い合わせフォームの導入**（Formspree推奨・無料）
6. **実際の会員の声に差し替え**（開業後）
