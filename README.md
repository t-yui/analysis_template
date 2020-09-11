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

## ディレクトリ構成

```bash
analysis_template/
├── data/
│   ├── original/
│   ├── processed/
│   └── testdata/
├── docker/
├── paper/
├── reports/
└── scripts/
    ├── R/
    │   ├── obj/
    │   ├── rmd/
    │   ├── script/
    │   └── test/
    ├── julia/
    │   ├── jld/
    │   ├── jupyter/
    │   ├── script/
    │   └── test/
    ├── python/
    │   ├── jupyter/
    │   ├── pkl/
    │   ├── script/
    │   └── test/
    └── sas/
```

## 各ディレクトリの役割




