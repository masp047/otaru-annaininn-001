# おたる案内人検定試験 問題・解答 OCRテキスト集

「おたる案内人」検定試験(主催:小樽観光大学校運営委員会)の **第1回〜第23回** の
問題用紙(`mondai`)と解答(`kaitou`)PDF 計46ファイルを、OCR でテキスト化したものです。

- 試験形式:1級・2級 共通問題、原則4択(1〜4)のマークシート方式(回によっては記述式を含む)
- 問題数:各回おおむね100問前後
- 出題分野:小樽の歴史(鰊漁・北前船・鉄道・港湾・運河保存運動)、歴史的建造物・建築、
  地場産業・工芸(オルゴール・硝子・酒造)、文学・美術、自然・地理、観光ホスピタリティ など

## 取得元

Google Drive の共有フォルダ内の PDF 46ファイル
(`1_mondai.pdf`〜`23_mondai.pdf` / `1_kaitou.pdf`〜`23_kaitou.pdf`)。

## OCR の方法

元の PDF は Unicode マッピングを持たない埋め込みフォント(MS-PGothic / 90msp-RKSJ-H)で
作られており、テキスト抽出するとすべて文字化けします。そのため次の手順でテキスト化しました。

1. 各ページを画像に変換(PyMuPDF, 約2.6倍解像度)
2. 画像を日本語OCR(Tesseract 5 / `-l jpn`)にかけてテキスト化

各テキストファイルはページ区切り `===== <name> page N/M =====` を含みます。

## 精度に関する注意 ⚠️

- **問題ファイル(`ocr/mondai/`):Tesseract OCR。精度は高い**(概ね95%以上)。本文・選択肢とも
  よく読めます。ただし固有名詞や旧字、`嘉永→豆永`・`鰊→触/録` 等の誤認識が一部に残ります。
- **解答ファイル(`ocr/kaitou/`):画像を目視で読み取って書き起こし**。解答用紙は格子状(グリッド)
  の表組みで Tesseract では升目内の数字が崩れるため、各ページを高解像度画像化し、人手相当の
  目視読み取りで `問N: 答え` 形式に整形し直しました。数字(1〜4)の選択式に加え、後期の回に
  含まれる記述式(人名・地名・用語)や枝問(問12A/12B 等)も保持しています。
  なお元PDF上で空欄・不鮮明だった升目は `(不明)` と記載しています。
- 第1回問題(`1_mondai`)は人手(目視)でも内容を確認済みです。

解答は目視転記のため実用上そのまま読めますが、採点等で厳密さが必要な場合は元PDFでの
最終照合を推奨します。

## ディレクトリ構成

```
ocr/
  mondai/   1_mondai.txt 〜 23_mondai.txt   (問題, Tesseract OCR, 各約30,000字)
  kaitou/   1_kaitou.txt 〜 23_kaitou.txt   (解答, 目視転記, 「問N: 答え」形式)
```

## 各回一覧

| 回 | 実施日 | 問題 | 解答 |
|----|--------|------|------|
| 第1回 | 2007年1月28日 | `ocr/mondai/1_mondai.txt` | `ocr/kaitou/1_kaitou.txt` |
| 第2回 | 2007年9月16日 | `ocr/mondai/2_mondai.txt` | `ocr/kaitou/2_kaitou.txt` |
| 第3回 | 2008年3月2日 | `ocr/mondai/3_mondai.txt` | `ocr/kaitou/3_kaitou.txt` |
| 第4回 | 2008年11月9日 | `ocr/mondai/4_mondai.txt` | `ocr/kaitou/4_kaitou.txt` |
| 第5回 | 2009年3月29日 | `ocr/mondai/5_mondai.txt` | `ocr/kaitou/5_kaitou.txt` |
| 第6回 | 2009年11月8日 | `ocr/mondai/6_mondai.txt` | `ocr/kaitou/6_kaitou.txt` |
| 第7回 | 2010年3月28日 | `ocr/mondai/7_mondai.txt` | `ocr/kaitou/7_kaitou.txt` |
| 第8回 | 2011年3月27日 | `ocr/mondai/8_mondai.txt` | `ocr/kaitou/8_kaitou.txt` |
| 第9回 | 2012年3月25日 | `ocr/mondai/9_mondai.txt` | `ocr/kaitou/9_kaitou.txt` |
| 第10回 | 2013年3月24日 | `ocr/mondai/10_mondai.txt` | `ocr/kaitou/10_kaitou.txt` |
| 第11回 | 2014年3月23日 | `ocr/mondai/11_mondai.txt` | `ocr/kaitou/11_kaitou.txt` |
| 第12回 | 2015年3月22日 | `ocr/mondai/12_mondai.txt` | `ocr/kaitou/12_kaitou.txt` |
| 第13回 | 2016年3月20日 | `ocr/mondai/13_mondai.txt` | `ocr/kaitou/13_kaitou.txt` |
| 第14回 | 2017年3月19日 | `ocr/mondai/14_mondai.txt` | `ocr/kaitou/14_kaitou.txt` |
| 第15回 | 2018年3月18日 | `ocr/mondai/15_mondai.txt` | `ocr/kaitou/15_kaitou.txt` |
| 第16回 | 2019年3月17日 | `ocr/mondai/16_mondai.txt` | `ocr/kaitou/16_kaitou.txt` |
| 第17回 | 2020年3月15日 | `ocr/mondai/17_mondai.txt` | `ocr/kaitou/17_kaitou.txt` |
| 第18回 | 2021年3月14日 | `ocr/mondai/18_mondai.txt` | `ocr/kaitou/18_kaitou.txt` |
| 第19回 | 2022年3月13日 | `ocr/mondai/19_mondai.txt` | `ocr/kaitou/19_kaitou.txt` |
| 第20回 | 2023年3月12日 | `ocr/mondai/20_mondai.txt` | `ocr/kaitou/20_kaitou.txt` |
| 第21回 | 2024年3月10日 | `ocr/mondai/21_mondai.txt` | `ocr/kaitou/21_kaitou.txt` |
| 第22回 | 2025年3月9日（OCR上は「20265年」と誤読） | `ocr/mondai/22_mondai.txt` | `ocr/kaitou/22_kaitou.txt` |
| 第23回 | 2026年3月8日 | `ocr/mondai/23_mondai.txt` | `ocr/kaitou/23_kaitou.txt` |
