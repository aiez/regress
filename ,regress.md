<!-- Copyright (c) 2026 Tim Menzies, MIT License https://opensource.org/licenses/MIT -->
<a href="https://timm.fyi"><img align="right" alt="Author" src="https://img.shields.io/badge/Author-timm-dc143c?logo=readme&logoColor=white"></a><img align="right" alt="Language" src="https://img.shields.io/badge/Language-CSV-000080?logo=files&logoColor=white"><img align="right" alt="License" src="https://img.shields.io/badge/License-MIT-32cd32?logo=open-source-initiative&logoColor=white"><img align="right" alt="Purpose" src="https://img.shields.io/badge/Purpose-Data·Regression-7b68ee?logo=githubcopilot&logoColor=white">

### [http://tiny.cc/regress](http://tiny.cc/regress)
Example regression datasets: 61 CSV files (abalone, auto93,
housing, wine quality, ...) with self-describing headers — column
names encode type and goal, so no separate schema files are
needed. Data only, no code.

```bash
# install
git clone http://tiny.cc/konfig ../konfig
git clone http://tiny.cc/regress regress && cd regress
make help
```

<a href="http://tiny.cc/regress"><img width="150" align="right" alt="qr" src="https://tiny.cc/tiny/qr-image/tiny.cc~regress~l~150.png"></a>

**Sections:** [NAME](#name) | [DATA](#data) | [FILES](#files) | [SEE ALSO](#see-also) | [LICENSE](#license) | [AUTHOR](#author)

## NAME

    regress - regression benchmark CSVs. headers are the schema;
    last goal columns end in '+' (maximize) or '-' (minimize).

## DATA

    CSV with self-describing header; no separate schema file:

      first char UPPER  -> numeric (Num)
      first char lower  -> symbolic (Sym)
      suffix '+'        -> numeric goal, maximize
      suffix '-'        -> numeric goal, minimize
      suffix '!'        -> symbolic goal (klass)
      suffix 'X'        -> ignore
      else              -> predictor
      missing value     -> '?'

    E.g. auto93.csv: Clndrs,Volume,HpX,Lbs-,Acc+,Model,origin,Mpg+

## FILES

[2dplanes.csv](#file-2dplanes-csv) | [abalone.csv](#file-abalone-csv) | [ailerons.csv](#file-ailerons-csv) | [auto93.csv](#file-auto93-csv) | [autohorse.csv](#file-autohorse-csv) | [autompg.csv](#file-autompg-csv) | [autoprice.csv](#file-autoprice-csv) | [bank32nh.csv](#file-bank32nh-csv) | [bank8FM.csv](#file-bank8fm-csv) | [baskball.csv](#file-baskball-csv) | [bodyfat.csv](#file-bodyfat-csv) | [bolts.csv](#file-bolts-csv) | [breasttumor.csv](#file-breasttumor-csv) | [cal.housing.csv](#file-cal-housing-csv) | [cholesterol.csv](#file-cholesterol-csv) | [cleveland.csv](#file-cleveland-csv) | [cloud.csv](#file-cloud-csv) | [cpu.act.csv](#file-cpu-act-csv) | [cpu.csv](#file-cpu-csv) | [cpu.small.csv](#file-cpu-small-csv) | [delta.ailerons.csv](#file-delta-ailerons-csv) | [delta.elevators.csv](#file-delta-elevators-csv) | [detroit.csv](#file-detroit-csv) | [diabetes.numeric.csv](#file-diabetes-numeric-csv) | [echomonths.csv](#file-echomonths-csv) | [elevators.csv](#file-elevators-csv) | [elusage.csv](#file-elusage-csv) | [fishcatch.csv](#file-fishcatch-csv) | [fried.csv](#file-fried-csv) | [fruitfly.csv](#file-fruitfly-csv) | [gascons.csv](#file-gascons-csv) | [house16H.csv](#file-house16h-csv) | [house8L.csv](#file-house8l-csv) | [housing.csv](#file-housing-csv) | [hungarian.csv](#file-hungarian-csv) | [kin8nm.csv](#file-kin8nm-csv) | [longley.csv](#file-longley-csv) | [lowbwt.csv](#file-lowbwt-csv) | [machine.cpu.csv](#file-machine-cpu-csv) | [mbagrade.csv](#file-mbagrade-csv) | [meta.csv](#file-meta-csv) | [mv.csv](#file-mv-csv) | [pbc.csv](#file-pbc-csv) | [pharynx.csv](#file-pharynx-csv) | [pol.csv](#file-pol-csv) | [pollution.csv](#file-pollution-csv) | [puma32H.csv](#file-puma32h-csv) | [puma8NH.csv](#file-puma8nh-csv) | [pwlinear.csv](#file-pwlinear-csv) | [pyrim.csv](#file-pyrim-csv) | [quake.csv](#file-quake-csv) | [schlvote.csv](#file-schlvote-csv) | [sensory.csv](#file-sensory-csv) | [servo.csv](#file-servo-csv) | [sleep.csv](#file-sleep-csv) | [stock.csv](#file-stock-csv) | [strike.csv](#file-strike-csv) | [triazines.csv](#file-triazines-csv) | [veteran.csv](#file-veteran-csv) | [vineyard.csv](#file-vineyard-csv) | [wisconsin.csv](#file-wisconsin-csv)

## SEE ALSO

    konfig    http://tiny.cc/konfig   shared Makefile, dotfiles
    optimiz   http://tiny.cc/optimiz  optimization datasets
    klassif   http://tiny.cc/klassif  classification datasets
    luamine   http://tiny.cc/luamine  code that reads these files

## LICENSE

    MIT. https://choosealicense.com/licenses/mit/

## AUTHOR

    Tim Menzies <timm@ieee.org>
