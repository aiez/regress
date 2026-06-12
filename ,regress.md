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

**Sections:** [NAME](#name) | [DATA](#data) | [SEE ALSO](#see-also) | [LICENSE](#license) | [AUTHOR](#author)

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

## SEE ALSO

    konfig    http://tiny.cc/konfig   shared Makefile, dotfiles
    optimiz   http://tiny.cc/optimiz  optimization datasets
    klassif   http://tiny.cc/klassif  classification datasets
    luamine   http://tiny.cc/luamine  code that reads these files

## LICENSE

    MIT. https://choosealicense.com/licenses/mit/

## AUTHOR

    Tim Menzies <timm@ieee.org>
