# kikaku-note-hdmi

`hdmi.kikaku-note.com` 用のHDMI規格一覧サイト。

## 想定構成

```txt
kikaku-note-hdmi
├── index.html
└── robots.txt
```

## Cloudflare Pages設定

| 項目 | 設定 |
|---|---|
| Framework preset | None |
| Build command | 空欄 |
| Build output directory | . |
| Production branch | main |

## Custom domain

```txt
hdmi.kikaku-note.com
```

## 反映後に確認するURL

```txt
https://hdmi.kikaku-note.com/
https://hdmi.kikaku-note.com/robots.txt
```

## 反映後にやること

1. Cloudflare PagesでProduction Deploy成功確認
2. Custom domainがActiveか確認
3. SSL enabled確認
4. `kikaku-note.com/sitemap.xml` にURL追加
5. `kikaku-note.com` 本体トップの「公開中」にHDMIを追加
6. Search Consoleで `https://hdmi.kikaku-note.com/` をURL検査
7. インデックス登録リクエスト
8. GA4リアルタイムでホスト名確認

## sitemap.xml 追加用スニペット

`</urlset>` の直前に追加。

```xml
  <url>
    <loc>https://hdmi.kikaku-note.com/</loc>
    <lastmod>2026-05-26</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
```

## コミット例

```powershell
git add index.html robots.txt README.md
git commit -m "Add HDMI specification guide"
git push
```
