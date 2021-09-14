# govtech-marketplace

*このリポジトリはtempolaryです。*

以下の翻訳のために作成しています。

**ファイルの取得**

* https://www.digitalmarketplace.service.gov.uk
```
wget -r https://www.digitalmarketplace.service.gov.uk
```

* https://www.gov.uk/guidance/buying-and-selling-on-the-digital-marketplace
```
wget -rnp https://www.gov.uk/guidance/buying-and-selling-on-the-digital-marketplace
```

取得したファイルが.htmlの拡張子が無いファイルのファイル名を一括置換してブラウザで正しく表示されるようにしています。
```
find ./www.gov.uk -type f -not -name "*.txt" | sed -e "p;s/\$/.html/" | xargs -n2 mv | find ./www.gov.uk -type f -not -name "*.txt"
```
