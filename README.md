# CVCOMBO: Control-Variable All-Combinations Robustness Test for Stata

**CVCOMBO** is a Stata package for systematic robustness analysis based on all
non-empty combinations of user-specified control variables.

**CVCOMBO 是一款用于控制变量任意组合稳健性检验的 Stata 工具包。**
> Version 2.0.0 | Jiang ZhenYuan (蒋镇源) & Zhang Na (张娜) | Northwest Normal University
CVCOMBO 是一款面向 Stata 的控制变量任意组合稳健性检验工具。
程序通过 method() 接收用户指定的估计方法，并自动枚举控制变量的所有非空组合，对每一种模型规格进行估计和汇总。当存在 \(k\) 个候选控制变量时，程序自动估计 \(2^k-1\) 种非空控制变量组合。

支持 regress、xtreg、logit、probit、reghdfe 等 Stata 估计命令，并提供共同样本控制、系数与显著性统计、Specification Curve、Specification Matrix、系数分布图以及论文表格自动输出等功能。

适用于实证研究中的控制变量敏感性分析、规格稳健性检验和 Specification Curve 分析。


CVCOMBO is a Stata package for robustness analysis based on all possible non-empty combinations of control variables.
Users specify the estimation method through method(), and CVCOMBO automatically enumerates and estimates every non-empty combination of user-specified controls. With \(k\) candidate control variables, the program estimates \(2^k-1\) alternative specifications.

CVCOMBO supports regress, xtreg, logit, probit, reghdfe, and other compatible Stata estimation commands. It provides common-sample control, coefficient and significance summaries, Specification Curves, Specification Matrices, coefficient distribution plots, and automated paper-ready output.

It is designed for control-variable sensitivity analysis, specification robustness checks, and Specification Curve analysis in empirical research.
