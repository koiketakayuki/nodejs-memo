# nodejs-memo
Nodejs開発環境構築メモ

たくさんnpmにpublishするなら、自動化しよう。


1. githubのリポジトリ作成
2. travisにリポジトリ登録
3. code climateにリポジトリ登録
4. npm initでプロジェクト情報を作成
5. eslint(airbnbルール)ファイル、.eslintignore作成
6. LICENSE作成
7. .travis.yml作成
8. .travis.ymlにcode climateのrepo tokenを追加
9. .travis.ymlにテスト通過後に、npmに自動デプロイされるよう設定

## travisの自動デプロイについて

travisコマンドでnpmリポジトリ毎の暗号化したtokenが設定されるので、それを用いる。

http://microapps.com/blog/auto-publishing-to-npm-by-travis-ci/
