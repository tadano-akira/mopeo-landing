# mopeo-landing

mopeo.org のランディングページ(静的HTML)。

## デプロイ

自宅サーバー(T430)上の `~/mopeo-landing` にこのリポジトリをcloneし、
`docker compose up -d` で nginx コンテナ(`mopeo-web`)が `index.html` を配信する。
到達経路は Cloudflare Tunnel 経由(mopeo.org)。

このリポジトリへのpush後のデプロイは、[Operation Gateway](https://github.com/tadano-akira/operation-gateway)
の `mopeo-landing-deploy` Workflow(承認 → Host Agent経由の `git pull` + `docker compose up -d` → 検証)から
実行できる。
