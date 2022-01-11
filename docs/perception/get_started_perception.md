## Case 1. rosbagを用いずにデータセットのみで評価を行う

- 評価 Metrics の開発などに
- poetry install

```
pip3 install poetry
```

- setting

```
git clone https://github.com/tier4/AWMLevaluation.git
cd AWMLevaluation
poetory install
```

- 実行

```
cd awml_evaluation
poetry run python3 -m test.lsim
```


## Case 2. Lsim側に組み込む
### install

- pip, submodule等は使わない
- reposに追加
  - 評価地点に関してはhashで管理する

```
repositories:
  # autoware
  simulator/AWMLevaluation:
    type: git
    url: git@github.com/tier4/AWMLevaluation.git
    version: main
```

### 実装

- <https://github.com/tier4/AWMLevaluation/blob/main/awml_evaluation/test/lsim.py> を参照

## Case 3. localでmodelの評価を行う

TBD