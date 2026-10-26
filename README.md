# A 2023 social accounting matrix for China with income-decile households and financial accounts

Dataset version: **1.0.0**. Release date: **26 October 2026**.
Dataset DOI: <https://doi.org/10.5281/zenodo.23654134>.
GitHub mirror: <https://github.com/wuwei0304/china-sam-2023-data>.

## Download and files

Download the complete [china-sam-2023-data-1.0.0.zip](china-sam-2023-data-1.0.0.zip) from this GitHub repository,
or use the Dataset DOI above for the permanent Zenodo record and its direct download.
Both locations distribute the same ZIP. The archive contains **40 files**, preserving the
directory structure below. The root-level documentation in the GitHub mirror is also inside
the ZIP. Paths in MANIFEST.csv refer to files within the unpacked archive; the manifest lists
the payload files except itself, with byte sizes and SHA-256 checksums.

`output/` contains the full 67-account CSV/XLSX and long-format SAM, the additional 58-account
household aggregation, account labels and macro blocks. `output/validation/`,
`output/sensitivity/` and `output/multipliers/` contain processed technical results.
`data/` contains three structural concordances and variable documentation. `figures/`
contains the four Data Descriptor figures. `inputs/README.md` documents excluded inputs.

## Matrix conventions

Reference year: 2023. Unit: **100 million yuan**, current prices. Rows receive payments;
columns pay. The full SAM has 19 activity accounts, 19 commodities, two factors, ten household
income deciles and institutional, capital, financial and discrepancy accounts. The 58-account
version is an additional reuse format and does not replace the complete 67-account matrix.
The Excel workbook has eight sheets, including household income, capital/financial and
consumption allocations. The maximum row-column balance gap is below 1e-6 in these units.

## CFPS confirmation and excluded source data

CFPS confirmed the following public-sharing scope, as supplied by the authors:

> 上述组级聚合参数随论文在公共数据仓库公开，符合《CFPS 用户使用协议》
>
> 这些聚合结果在公开前，不需要提交贵中心审核或备案

This Dataset contains author-constructed aggregate/modelled economic transactions and
group-level parameters. It contains no household or person records, original CFPS files,
original NBS/PBC input workbooks, internal decile workbook, private correspondence or credentials.
CFPS confirmation of aggregate sharing does not imply endorsement of the model or estimates.

## Reproduction and code

The software is archived independently as version 1.0.0 at
<https://doi.org/10.5281/zenodo.23642715> and maintained at
<https://github.com/wuwei0304/china-sam-2023-code>. That DOI identifies software; the Dataset
DOI above identifies the numerical data. Obtain the four authorised inputs described in
`inputs/README.md`, then run `python run_all.py` in the separate code folder. The source
microdata are required to reconstruct household allocation, not to read these aggregate files.

## Licence and citation

Data and project-authored aggregate outputs: **CC BY 4.0**; see `LICENSE-DATA.md`. The licence
does not cover excluded original databases. Software: MIT in its separate archive.

Wu, W. & Jiang, J. (2026). *A 2023 social accounting matrix for China with income-decile
households and financial accounts* (Version 1.0.0) [Data set]. Zenodo.
https://doi.org/10.5281/zenodo.23654134

The household allocation uses CFPS 2022, conducted by the Institute of Social Science Survey,
Peking University. Attribute CFPS and other original sources when relevant, cite this Dataset
and the software version used, and indicate modifications. The corresponding Data Descriptor
manuscript is in preparation; no journal publication or article DOI is asserted here.

## Validation note

Validation note (26 October 2026): `output/validation/summary.txt` contains an external comparator labelled 'NBS household survey 2023: 0.465'. Its attribution to the cited yearbook table has not been verified against the original table. This comparator is printed for context only; it is not used in SAM construction, balancing or calculation of the dataset's between-decile Gini (0.498). The manuscript omits this comparison. The version 1.0.0 ZIP is preserved unchanged.
