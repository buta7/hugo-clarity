# README

## セットアップ

サイト作成

```shell
hugo new site hugo-clarity
```

レポジトリ初期化

```shell
cd hugo-clarity
git init
echo '*~' >> .gitignore
echo '*.bak' >> .gitignore
echo '*.orig' >> .gitignore
echo '.env' >> .gitignore
echo 'public' >> .gitignore
echo 'resources' >> .gitignore
```

テーマ設定(submoduleはhttpsプロトコルで追加)

```shell
git submodule add https://github.com/chipzoller/hugo-clarity.git themes/clarity
```

(参考)submoduleの削除

```shell
git submodule deinit -f themes/clarity
git rm themes/clarity
rm -fr .git/modules/clarity
```

サイト設定

```shell
cp -p themes/clarity/exampleSite/config.toml .
cp -pr themes/clarity/exampleSite/{content,data} .
```

## Link

* [Hugo Clarity \| Hugo Themes](https://themes.gohugo.io/hugo-clarity/)
