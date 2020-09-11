# analysis_template

解析用リポジトリのテンプレートです。

## 使い方

```bash
# 本リポジトリをクローンする
$ git clone https://github.com/t-yui/analysis_template.git

# リポジトリの初期化
$ cd analysis_template
$ rm -rf .git/
$ git init

# リモートリポジトリに登録
$ git add .
$ git commit -m ":tada: first commit"
$ git branch -M master
$ git remote add origin [登録先のリモートリポジトリのURL]
$ git push -u origin master
```

## ディレクトリ構成と各ディレクトリの役割

```bash
analysis_template/
├── data/              # データを格納する
│   ├── original/         # オリジナルデータを格納する
│   ├── processed/        # 前処理・加工したデータを格納する
│   └── testdata/         # テストデータを格納する
├── docker/            # Dockerfileを格納する
│   └── Dockerfile        # pystanをjupyterで動かすためのDockerfileを入れています
├── paper/             # 論文や参考文献を格納する
├── reports/           # 解析レポートを格納する
└── scripts/           # 解析用プログラムを格納する
    ├── R/                # R言語に関するディレクトリ
    │   ├── obj/             # オブジェクト（.obj）を格納する
    │   ├── rmd/             # R Markdownファイル（.Rmd）を格納する
    │   ├── script/          # スクリプト（.R）を格納する
    │   └── test/            # テストコードを格納する
    ├── julia/            # Juliaに関するディレクトリ
    │   ├── jld/             # オブジェクト（.jld）を格納する
    │   ├── jupyter/         # ノートブック（.ipynb）を格納する
    │   ├── script/          # スクリプト（.jl）を格納する
    │   └── test/            # テストコードを格納する
    ├── python/           # Pythonに関するディレクトリ
    │   ├── jupyter/         # ノートブック（.ipynb）を格納する
    │   ├── pkl/             # オブジェクト（.pkl）を格納する
    │   ├── script/          # スクリプト（.py）を格納する
    │   └── test/            # テストコードを格納する
    └── sas/              # SASに関するディレクトリ
    └── shell/            # shell scriptに関するディレクトリ
        ├── exec.sh          # 解析コード実行処理を記述する
        └── setup.sh         # 解析環境セットアップ処理を記述する
```

