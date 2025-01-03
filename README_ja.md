# 多言語コード文字検出ツール

[English](README.md) | [简体中文](README_zh.md) | [繁体中文](README_zh_TW.md) | [日本語](README_ja.md) | [한국어](README_ko.md) | [Русский](README_ru.md) | [Tiếng Việt](README_vi.md)

このツールは、コードファイル内の無効な文字を検出するための Python ツールです。英語、中国語、日本語、韓国語、およびロシア語の文字を検出し、コード内の特殊な文字や不可見文字を特定できます。

## 機能

-   複数のプログラミング言語ファイル（デフォルト：.py, .java, .c, .cpp, .js, .html, .css, .txt）をサポート
-   複数言語の文字を検出：
    -   英語と数字
    -   中国語（CJK 統一漢字）
    -   日本語（平仮名と片仮名）
    -   韓国語
    -   ロシア語（キリル文字）
    -   ベトナム語（ラテン文字）
-   ディレクトリ全体を再帰的に検索
-   無効な文字の行番号と列番号を正確に表示
-   無効な文字の Unicode コード値を表示
-   コマンドラインパラメータをサポート
-   詳細なエラー出力

## 使用方法

1. プロジェクトディレクトリを指定して実行：

```bash
python invalid_char_checker.py /path/to/your/project
```

2. ファイルタイプを指定して実行：

```bash
python invalid_char_checker.py /path/to/your/project -e .py,.java,.c,.cpp,.js,.html,.css,.txt
```

## サポートされる文字

1. ASCII 文字：

    - 英文字母（a-z, A-Z）
    - 数字（0-9）
    - 常用記号と演算子
    - 空白文字（スペース、タブ、改行など）

2. Unicode 文字：
    - 中国語（CJK 統一漢字）
    - 日本語（平仮名と片 �� 名）
    - 韓国語
    - ロシア語（キリル文字）

## 注意事項

-   ファイルは UTF-8 エンコーディングでなければなりません
-   エンコーディングエラーが発生した場合、プログラムは対応するエラー情報を表示します
-   大規模なプロジェクトを処理する前に小規模なテストを行うことをお勧めします

## エラー処理

-   指定されたディレクトリが存在しない場合、プログラムはエラー情報を表示して終了します
-   ファイルが UTF-8 エンコーディングでない場合、エンコーディングエラーが表示されます
-   ファイル処理中のその他のエラーは詳細な情報を表示して捕獲されます

## ライセンス

MIT License
