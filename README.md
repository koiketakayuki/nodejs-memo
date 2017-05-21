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

npm loginした後に、下記のコマンドでauth tokenをチェック

```
cat ~/.npmrc | grep _auth
```

travisコマンドでtokenを暗号化

```
travis encrypt -r koiketakayuki/(リポジトリ名) (auth-token)
```

travisにリポジトリ登録してないとエラーになるので注意。
これでテストを通過後、git push --tagsでタグがついたものだけnpmに自動でpublishされる。

[参考URL]
http://microapps.com/blog/auto-publishing-to-npm-by-travis-ci/
