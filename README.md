# govtech-marketplace-uk

*このリポジトリはtempolaryです。*

以下の翻訳のために作成しています。

**内容確認URL**

https://aki-snow.github.io/govtech-marketplace-uk/

https://aki-snow.github.io/govtech-marketplace-uk/crown-commercial-service.github.io/digitalmarketplace-manual/index.html

https://aki-snow.github.io/govtech-marketplace-uk/www.digitalmarketplace.service.gov.uk/index.html

https://aki-snow.github.io/govtech-marketplace-uk/www.gov.uk/guidance/buying-and-selling-on-the-digital-marketplace.html


**ファイルの取得**

* https://www.digitalmarketplace.service.gov.uk
```
wget -r https://www.digitalmarketplace.service.gov.uk
```

* https://www.gov.uk/guidance/buying-and-selling-on-the-digital-marketplace
```
wget -rnp https://www.gov.uk/guidance/buying-and-selling-on-the-digital-marketplace
```

取得したファイル名を以下で確認するとrobots.txtのファイル以外はファイルの拡張子がないhtmlファイルになっているので
```
find ./www.gov.uk -type f -not -name "*.txt"
```

.txtのファイルを除く.htmlの拡張子が無いファイルのファイル名を一括置換してブラウザで正しく表示されるようにしています。
```
find ./www.gov.uk -type f -not -name "*.txt" | sed -e "p;s/\$/.html/" | xargs -n2 mv
```
