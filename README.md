# selenium

## About

この拡張はSelenium-IDEを使う時の、痒いところに手を届かせるためのSelenium-IDEユーザ拡張です。

例えば・・・

- 同じ入力フォームに対して複数の値を連続で試したい場合。
- ページ遷移時必ずレイアウトチェックをしたい場合。
- テストケースとは別にテスト値を管理したい場合。

この拡張はこれらの問題を解決します！

商用、非商用問わずにご自由にご利用ください！
ライセンスはMIT licenseです。

Selenium-IDEへのユーザ拡張の導入は、Selenium-IDE — Selenium 日本語ドキュメントの"ユーザー拡張スクリプト"の項目を参照してください。
※複数のユーザ拡張を使用する場合、各ユーザ拡張のパスを";"(セミコロン)で結合することで同居させることができます。

## Caution

arrayForeachコマンド、whileコマンドは次の拡張とは初期化処理で競合するため同時に使用できません。

- [SelBlocks (for Selenium IDE) :: Add-ons for Firefox](https://addons.mozilla.org/ja/firefox/addon/selenium-ide-sel-blocks/ "SelBlocks (for Selenium IDE) :: Add-ons for Firefox")

arrayForeachコマンド、whileコマンドを使用する場合は、競合する拡張を無効化、またはアンインストールしてください。

それでは良いテストを :)

## Command index

| # | Command | Description |
| --- | --- | --- |
| 1 | getImWidth(value) | PHPのmb_strimwidthと同様の機能を提供します。|
| 2 | getRealValue(locator) | ロケ―ターで指定された要素の値を取得し、trimせずに返します。|
| 3 | getRealText(locator) | ロケ―ターで指定された要素のテキストを取得し、trimせずに返します。|
| 4 | getClosestTrXpath(locator) | ロケ―ターで指定された要素が属する直近のtr要素のXPathを取得します。|
| 5 | getRowIndex(locator, store_name) | ロケ―ターで指定された要素が属するテーブル内での行数をストアします。|
| 6 | getElement(locator, store_name) | ロケ―ターで指定された要素をストアします。|
| 7 | storeTextContent(locator) | ロケ―ターで指定された要素のtextContentを返します。|
| 8 | getInnerHtml(locator) | ロケ―ターで指定された要素のinnerHTMLを返します。|
| 9 | getTrimmedInnerHtml(locator) | ロケ―ターで指定された要素のtrim済みinnerHTMLを返します。|
| 10 | getVar(store_name) | 指定したストア名の値を取得します。|
| 11 | getTableRowIndex(locator) | ロケ―ターで指定された要素のテーブル内での行数を返します。|
| 12 | getTableRowIndexOdd(locator) | ロケ―ターで指定された要素のテーブル内での行数が奇数かどうかを返します。|
| 13 | storeFromTableRowIndexOdd(locator, parameters) | ロケ―ターで指定された要素のテーブル内での行数が奇数かどうかをストアします。|
| 14 | setFilter(filter_function, store_name) | フィルタ関数をストアします。|
| 15 | execFilter(filter_name, store_name) | フィルタ関数を実行します。|
| 16 | lf2Br(html) | HTML文中の改行文字を<br>タグに置換します。|
| 17 | getSelectedIndex(locator) | 指定されたselectが現在選択しているindexを返します。|
| 18 | assertAdjustLfHtml(locator, pattern) | 指定されたロケ―ターにあるHTMLと指定した文字列の改行文字を<br>タグに変換した上で、HTMLとして検証を行います。|
| 19 | assertAttributePresent(locator, pattern) | 指定されたロケ―ターに指定した要素があるか検証します。|
| 20 | assertAttributeNotPresent(locator, pattern) | 指定されたロケ―ターに指定した要素がないか検証します。|
| 21 | remove(locator) | 指定されたロケ―ターにある要素を削除します。|
| 22 | assertDocType(doctype) | 指定されたDOCTYPE宣言が行われているかどうか検証します。|
| 23 | assertDocTypeName(name) | 指定されたDOCTYPE名が設定されているかどうか検証します。|
| 24 | assertDocTypePublicId(public_id) | 指定されたDOCTYPE publicIdが設定されているかどうか検証します。|
| 25 | assertDocTypeSystemID(system_id) | 指定されたDOCTYPE systemIdが設定されているかどうか検証します。|
| 26 | openPreProcess(url, ignoreResponseCode) | 拡張変数の事前展開を行い、返します。|
| 27 | setExeCommandSilentMode() | コマンド一括実行時のログ表示を抑制します。|
| 28 | releaseExeCommandSilentMode() | コマンド一括実行時のログ表示を抑制を解除します。|
| 29 | execCommand(command_name, values) | 現在のコマンド一括実行時のログ表示抑制状態を返します。|
| 30 | assertExecCommand(command_name, values) | targetで指定した値をコマンドとし、valueで指定した値を引数として検証コマンドをアサーションとして実行します。|
| 31 | execCommandFromArray(store_name) | ストアに保存された配列を元にコマンドを実行します。|
| 32 | assertExecCommandFromArray(store_name) | ストアに保存された配列を元にコマンドを実行します。|
| 33 | execCommandFromCsv(file_path) | CSVファイルに記載されたコマンドを一括で実行します。|
| 34 | assertExecCommandFromCsv(file_path) | CSVファイルに記載されたコマンドをアサーションとして一括で実行します。|
| 35 | execCommandFromExtCsv(file_path) | 拡張されたCSVファイルに記載されたコマンドを一括で実行します。|
| 36 | execCommandFromExtCsvSilent(file_path) | 拡張されたCSVファイルに記載されたコマンドを一括でログ出力無しで実行します。|
| 37 | assertExecCommandFromExtCsv(file_path) | 拡張されたCSVファイルに記載されたコマンドを一括で実行します。|
| 38 | storeFromExtCsv(file_path) | 拡張されたCSVファイルに記載された値を一括でストアします。|
| 39 | storeCsv(file_path, store_name) | CSVファイルを配列化し、ストアします。|
| 40 | storeExtCsv(file_path, store_name) | 拡張されたCSVファイルを配列化し、ストアします。|
| 41 | storeExtCsvPreProcess(file_path, store_name) | 拡張されたCSVファイルを配列化、値の展開を行ったのちストアします。|
| 42 | loadCsv(file_path) | CSVファイルをロードします。||ロードしたCSVファイルはグローバル変数の配列として保持します。|
| 43 | storeCsvCell(position, store_name) | 指定したセルのデータをストアします。|
| 44 | eachCsvRow(position_store_name, store_name) | CSVデータの行をeachして、データと行数をストアします。|
| 45 | fetchCellFromCurrentRow(column, store_name) | CSVデータの現在の行から指定した列のデータをストアします。|
| 46 | storeArrayColumn(array_info, store_name) | 添え字で指定された要素をストアします。|
| 47 | listArrayColumn(array_info, store_info) | 配列の各要素を一括でストアします。|
| 48 | assertTextContent(locator, value) | targetで指定された要素が持つcontentTextを元にassertionを行います。|
| 49 | storeCurrentTestSuiteFolder(store_name) | 現在実行中のテストスイートファイルがあるフォルダパスをストアに保存します。|
| 50 | storeCurrentTestSuitePath(store_name) | 現在実行中のテストスイートファイルのフルパスをストアに保存します。|
| 51 | storeCurrentTestSuiteFileName(store_name) | 現在実行中のテストスイートファイルのファイル名をストアに保存します。|
| 52 | storeCurrentTestCaseFolder(store_name) | 現在実行中のテストケースファイルがあるフォルダパスをストアに保存します。|
| 53 | storeCurrentTestCasePath(store_name) | 現在実行中のテストケースファイルのフルパスをストアに保存します。|
| 54 | storeCurrentTestCaseFileName(store_name) | 現在実行中のテストケースファイルのファイル名をストアに保存します。|
| 55 | arrayEach(array_store_name, store_name) | 配列によるforeachを開始します。|
| 56 | endArrayEach() | 配列によるforeachの終了位置です。|
| 57 | while(target) | whileを開始します。|
| 58 | endWhile() | whileの終了位置です。|

