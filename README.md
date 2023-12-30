# 同時アクセスしたコントローラーアプリからの操作を外部サーバーでリアルタイムで描画する

- ユーザー用のアプリケーションで制御
- 同時制御したアプリケーションからの情報を集約したサーバーで描画
- 簡単なゲームにしたい（ジャンケン、横向き対戦型シューティング　など）

## ▼ 大枠の構成

### ○ コントローラーアプリ

- Electron アプリ
  - Nextron を使う？
- 簡単なボタンを配置しクリックして値を送信
- 対戦結果ページに遷移
- 相手や結果の待機ステータスを通知
- ログイン認証
  - SNS 認証（google）

### ○ 描画サーバー

- コントローラーから受け取った情報を表示
- React/Next？ アプリ
- Three.js/TRF 使いたい
- 外部サーバーにデプロイし複数アクセスを受け付ける

### ○ データベース

- ユーザー情報
- 簡単なゲームで結果を保存
- Supabase
  - PostgreSQL？
- リポジトリは個別に用意する？
- データベース制御はどちらのサーバーで行うべきか？
- 描画サーバーでのリアルタイム通信はなにで実現？
  - Socket 通信？
  - SWR？フェッチじゃないなら合わない？
  - ストリーミング再生？

## ▼ 使いたい技術

- Socket.io
- Electron
- Next.js
- TypeScript
- Three.js
- Supabase
- PostgreSQL
- prisma
- zod？

## ▼ 学習

- Socket.io
  - https://socket.io/docs/v4/
- デプロイサーバー（Render？）
  - https://docs.render.com/free
- 承認機能
  - Google 認証
    - コントローラー側か描画サーバー側か要調査？
      - https://otiai10.hatenablog.com/entry/2019/05/03/145913
- Nextron
  - https://github.com/saltyshiomix/nextron
- Supabase
  - https://supabase.com/
