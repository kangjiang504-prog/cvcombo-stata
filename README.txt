CVCOMBO v2.0.0
Control-variable all-combinations robustness test for Stata

Authors
Jiang ZhenYuan (蒋镇源)
Zhang Na (张娜)
School of Economics, Northwest Normal University
Support: kangjang504@gmail.com; zhangna@nwnu.edu.cn

DESCRIPTION
cvcombo enumerates every nonempty combination of user-specified control variables and estimates each specification with a user-supplied method(). With k candidate controls, it estimates 2^k - 1 specifications.

The method() interface is generic. Examples include regress, xtreg, logit, probit, and reghdfe. The selected estimator must accept if/in qualifiers and return _b[mainvar] and _se[mainvar].

PAPER OUTPUT
The paper option additionally exports:
1. Specification Curve
2. Coefficient distribution
3. Coefficient-by-number-of-controls boxplot
4. Specification Matrix
5. Ranked coefficient and 95% confidence interval plot
6. CSV robustness summary
7. Word Table 8 in three-line-table format

SVG output uses Arial and English/ASCII graph labels to avoid dependence on local Chinese fonts. The Word table uses Unicode Chinese text and Microsoft YaHei where available.

DEPENDENCIES
No external dependency is required for regress, xtreg, logit, or probit. If method(reghdfe) is used, reghdfe must be installed separately from SSC.

INSTALLATION
After SSC publication:
    ssc install cvcombo
    help cvcombo

EXAMPLE
    cvcombo LS Demand, method(reghdfe) \
        controls(Size Lev Employee Growth Age CAP WW HHI) \
        absorb(id year) cluster(id) samplevars(id year) \
        saving(cvcombo_results.dta) replace paper \
        paperdir(cvcombo_paper_output)

LICENSE
MIT License. See LICENSE.txt.
