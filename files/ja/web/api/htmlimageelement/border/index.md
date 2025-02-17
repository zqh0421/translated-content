---
title: HTMLImageElement.border
slug: Web/API/HTMLImageElement/border
page-type: web-api-instance-property
tags:
  - API
  - HTML
  - HTML DOM
  - HTMLImageElement
  - 画像
  - プロパティ
  - リファレンス
  - border
  - img
  - 非推奨
browser-compat: api.HTMLImageElement.border
translation_of: Web/API/HTMLImageElement/border
---
{{APIRef("HTML DOM")}}{{deprecated_header}}

廃止された {{domxref("HTMLImageElement")}} の **`border`** プロパティは、 画像を囲む境界線の太さをピクセル数で指定します。既定値である 0 は、境界線を描画しないことを示します。

このプロパティは使用しないでください。代わりに、 CSS を使用して境界線をスタイル付けしてください。 {{cssxref("border")}} プロパティまたはその個別指定プロパティを使用すると、境界線の太さを設定するだけでなく、他の様々なスタイリングオプションを適用できる可能性があります。

具体的には、書字方向を意識した {{cssxref("border-block-start-width")}}, {{cssxref("border-block-end-width")}}, {{cssxref("border-inline-start-width")}}, {{cssxref("border-inline-end-width")}} 属性を用いて制御されます。

互換性（あるいはその他の理由）のために、代わりに（あるいは追加で）古いプロパティを使用することができます。 {{cssxref("border-top-width")}}, {{cssxref("border-right-width")}}, {{cssxref("border-bottom-width")}}, {{cssxref("border-left-width")}} です。

## 値

画像を囲む境界線の太さを CSS ピクセル単位で指定した整数値が入った文字列です。 `0` または空の文字列は、境界線を描画しないことを意味します。`border` の既定の値は `0` です。

## 使用上の注意

`border` は使わないでください。これは時代遅れです。代わりに、 CSS の {{cssxref("border")}} プロパティとその個別指定プロパティを使用して、画像の周りに境界線をを設定してください。

例えば、以下のような HTML があった場合です。

```html
<img src="image.png" border="2">
```

以下は、この廃止されたプロパティの代わりに、 CSS を使用して同じ外観を提供するものです。

```html
<img src="image.png" style="border: 2px;">
```

さらに追加情報を入力することで、境界線の色などを変更することができます。

```html
<img src="image.png" style="border: dashed 2px #333388;">
```

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}
