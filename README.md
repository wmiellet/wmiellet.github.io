# Bland–Altman Agreement Analysis for Molecular Carriage Surveillance of Bacteria in Polymicrobial Samples – A Tutorial

## Overview
The dual-target approach uses agreement statistics to determine whether two genetic markers exhibit conditional dependence. While correlation quantifies the strength of a relationship, agreement assesses whether two methods are likely to measure the same quantity of a target [1]. This distinction reveals whether the markers are measuring the abundance of distinct strains within a single bacterial population or instead reflecting the abundances of strains from two different bacterial populations.

## Producing an Agreement Plot
To implement this, an agreement plot (Bland–Altman) is generated, where the x axis represents the mean of the two measurements (from marker A and marker B), and the y axis represents the difference between them. The limits of agreement define the interval within which 95% of the differences fall . To evaluate the precision of these limits, 95% confidence intervals can be added. If the limits of agreement exceed a predefined acceptable range, the two genetic markers cannot be considered reliable for detecting a single bacterial species with sufficient confidence. As a rule of thumb, we recommend a predefined acceptable limit of 2 Cq (equivalent to a 4 fold difference in concentration) [2].

## Assumptions of the Method
The proposed method rests on two assumptions: (I) the differences between genetic marker measurements are non normally distributed, and (II) the difference between the two markers is not proportional to the mean of the two measurements [1]. When one of the two markers exhibits reduced specificity and samples often contain strains that are positive for only one of the markers, non parametric limits of agreement should be considered [3]. When using non-parametric limits, the median difference is indicated in the agreement plot as well as the limits of agreement based on the 2.5 and 97.5th percentile.

## Types of Agreement plots
We distinguish between two types of agreement plots: the population-specific agreement plot and the serotyping agreement plot. In the former, two genetic markers with presumed population-specific accuracy are compared, whereas in the latter, a serotype-specific marker is compared against a population-specific marker. Serotype-specific markers are allowed to have lower abundance than population-specific markers to account for multiple serotype carriage. However, when the abundance of a serotype-specific marker strongly exceeds that of the population-specific marker, this finding suggests conditional independence—i.e., the two markers are not measuring the same bacterial population. In such cases, the serotype-specific quantification can be attributed to confounding by a different bacterial population. For the serotype agreement plot, the acceptable limit can be either 2 Cq or the limits of agreement derived from markers A and B themselves [2].

### population-specific agreement plot
[Text].
<iframe src="https://wmiellet.github.io/plot.html" width="100%" height="600" frameborder="0"></iframe>

### serotyping agreement plot
[Text].

## Interpretation
[Text].

### ICC
[Text].

## Recommendations
We encourage others to routinely monitor agreement between genetic markers. Due to spatiotemporal variation in sample composition or study group composition, the diagnostic specificity of molecular assays fluctuates. This phenomenon is known as the spectrum effect and is an important source of methodological bias across studies and inter study variation [4]. To avoid these pitfalls, we recommend assessing agreement between genetic markers on a per study subgroup basis, and for annual cross sectional studies, on a yearly basis within a single subgroup.

### Reference list
1. Bland, J. Martin, and Douglas G. Altman. "Comparing methods of measurement: why plotting difference against standard method is misleading." The Lancet 346.8982 (1995): 1085-1087.
2. Miellet, Willem R., et al. "Streptococcus pneumoniae carriage studies in adults: Importance, challenges, and key issues to consider when using quantitative PCR-based approaches." Frontiers in Microbiology 14 (2023): 1122276.
3. Bland, J. Martin, and Douglas G. Altman. "Measuring agreement in method comparison studies." Statistical methods in medical research 8.2 (1999): 135-160.
4. Mulherin, Stephanie A., and William C. Miller. "Spectrum bias or spectrum effect? Subgroup variation in diagnostic test evaluation." Annals of Internal Medicine 137.7 (2002): 598-602.

##### correspondence
