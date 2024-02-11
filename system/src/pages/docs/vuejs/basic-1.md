---
title: 目的
description:  
---

Vue.jsの基礎を理解したら、一般的なWebサービスの画面をVue.jsで作ってみましょう。

ここでは
[OpenWork](https://www.vorkers.com/company.php?m_id=a0C300000044WsL)
のTop画面を題材とします。この画面のようなモック画面を作ります。

コンポーネント分割を意識してモック画面を作成する事で、Vue.jsでの画面開発方法を学習します。

合わせて、コンポーネント間でのデータ・イベントのやり取りや、ちょっとしたトランジション（視覚効果）の作り方も体験します。

---
## 1　画面の分析

題材画面
![1_openwork_600.png](/textbook/1_openwork_600.png "1_openwork_600")

題材の画面を分析して、コンポーネントを分割します。



## 2　モック画面の方針
どのように分割しますか。

情報のまとまり・機能の単位で分割すると上手くいく場合が多いです。

分割イメージが出来たら、紙やデザインツールに下書きしておきましょう。


### 2.1　設計
ここではFigmaで以下の様にモック画面を下書きしました。

モック画面
![1_mock_2.png](/textbook/1_mock_2.png "1_mock_2")

### 2.2　ファイル構成
次に、Vueコンポーネントファイルの構成を整理します。

ここでは次の通りにファイル分割することとします。

```
src
├── ・・・
├── components
│   ├── Header.vue　・・・ ヘッダー
│   ├── PageDetail.vue　・・・ 詳細部分コンテナ
│   ├── PageDetailMain.vue　・・・ 詳細部分 左側メイン
│   ├── PageDetailSide.vue　・・・ 詳細部分 右側サイド
│   ├── PageDetailTabs.vue　・・・ メニュータブ
│   └── PageSummary.vue　・・・ サマリ部分
├── App.vue
└── main.js
```
---
