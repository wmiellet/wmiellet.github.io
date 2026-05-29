# Bland–Altman Agreement Analysis for Molecular Carriage Surveillance of Bacteria in Polymicrobial Samples – A Tutorial

<i>Disclaimer: This page is being worked on. The page is currently incomplete and the text is somewhat rough around the edges.</i>

## Overview
Polymicrobial samples, such as saliva and oropharyngeal specimens, often harbor high bacterial diversity, with many species present in low abundance. In such settings, confidently identifying a target bacterial population becomes difficult when closely-related bacteria are abundant and either frequently engage in gene exchange or share a high degree of similarity due to ancestral recombination or a common ancestor. Examples include <i>Streptococcus pneumoniae</i>, <i>Neisseria meningitidis</i>, <i>Haemophilus influenzae</i> and <i>Streptococcus pyogenes</i> in saliva, as well as pathogenic <i>Escherichia coli</i> in the gut. To address this, we have developed a sensitive, culture-independent detection strategy called the dual-target (or "Two-to-Tango") approach [1].

The dual-target approach uses agreement statistics to determine whether two genetic markers exhibit conditional dependence. Demonstrating such dependence between genetic markers, can be used to confirm that a specific bacterial population can be individually quantified. While correlation quantifies the strength of a relationship, agreement assesses whether two methods are likely to measure the same quantity of a kind [2]. This distinction reveals whether the genetic markers are jointly measuring the abundance of strains from a single bacterial population, or instead reflecting two distinct populations.

## Producing an Agreement Plot
Unlike a correlation plot, where each axis represents one genetic marker, an agreement plot readily allows one to inspect two assays for conditional independence. In an agreement plot the <i>x</i>-axis represents the mean of the two measurements (from marker A and marker B), and the <i>y</i>-axis represents the difference between them. The limits of agreement define the interval within which 95% of the differences fall . To evaluate the precision of these limits, 95% confidence intervals can be added. If the limits of agreement exceed a predefined acceptable range, the two genetic markers cannot be considered reliable for detecting a single bacterial species with sufficient confidence. As a rule of thumb, we recommend a predefined acceptable limit of 2 Cq (equivalent to a 4 fold difference in concentration) [2].

### Assumptions of the Method
The proposed method rests on two assumptions: (I) the differences between genetic marker measurements are non normally distributed, and (II) the difference between the two markers is not proportional to the mean of the two measurements [2]. When one of the two markers exhibits reduced specificity and samples often contain strains that are positive for only one of the markers, non parametric limits of agreement should be considered [4]. When using non-parametric limits, the median difference is indicated in the agreement plot as well as the limits of agreement based on the 2.5 and 97.5th percentile.

## Types of Agreement plots
We distinguish between two types of agreement plots: the population-specific agreement plot and the serotyping agreement plot. In the former, two genetic markers with presumed population-specific accuracy are compared, whereas in the latter, a serotype-specific marker is compared against a population-specific marker. Serotype-specific markers are allowed to have lower abundance than population-specific markers to account for multiple serotype carriage. However, when the abundance of a serotype-specific marker strongly exceeds that of the population-specific marker, this finding suggests conditional independence—i.e., the two markers are not measuring the same bacterial population. In such cases, the serotype-specific quantification can be attributed to confounding by a different bacterial population. For the serotype agreement plot, the acceptable limit can be either 2 Cq or the limits of agreement derived from markers A and B themselves [3].

### population-specific agreement plot
[Text].
<iframe src="https://wmiellet.github.io/plot.html" width="100%" height="350" frameborder="0"></iframe>
Figure 1: [Legend text].
[Text]

<iframe src="https://wmiellet.github.io/plot2.html" width="100%" height="350" frameborder="0"></iframe>
Figure 2: [Legend text].

### serotyping agreement plot
[Text].

## Interpretation
[Text].

### Agreement indices
#### ICC
[Text].
#### Cohen's kappa
[Text].
#### Light's kappa
[Text].

## Produce an Agreement plot with your own data!
[Upload a CSV and create a plot directly in your browser](https://wmiellet.github.io/data_upload.html).

[new version](https://wmiellet.github.io/data_upload2.html).

[newer version](https://wmiellet.github.io/data_upload3.html).

## Limitations
[Text].

## Recommendations & concluding remarks
We encourage others to routinely monitor agreement between genetic markers. Due to spatiotemporal variation in sample composition or study group composition, the diagnostic specificity of molecular assays fluctuates. This phenomenon is known as the spectrum effect and is an important source of methodological bias across studies and inter study variation [5]. To avoid these pitfalls, we recommend assessing agreement between genetic markers on a per study subgroup basis, and for annual cross sectional studies, on a yearly basis within a single subgroup.

### Reference list
1. Miellet, Willem R., et al. "It takes two to tango: combining conventional culture with molecular diagnostics enhances accuracy of Streptococcus pneumoniae detection and pneumococcal serogroup/serotype determination in carriage." Frontiers in microbiology 13 (2022): 859736.
2. Bland, J. Martin, and Douglas G. Altman. "Comparing methods of measurement: why plotting difference against standard method is misleading." The Lancet 346.8982 (1995): 1085-1087.
3. Miellet, Willem R., et al. "Streptococcus pneumoniae carriage studies in adults: Importance, challenges, and key issues to consider when using quantitative PCR-based approaches." Frontiers in Microbiology 14 (2023): 1122276.
4. Bland, J. Martin, and Douglas G. Altman. "Measuring agreement in method comparison studies." Statistical methods in medical research 8.2 (1999): 135-160.
5. Mulherin, Stephanie A., and William C. Miller. "Spectrum bias or spectrum effect? Subgroup variation in diagnostic test evaluation." Annals of Internal Medicine 137.7 (2002): 598-602.

To be included: 
- add visual figure to explain the problem of molecular detection of bacteria in polymicrobial settings. 
- reference to Marshall paper.
- 'BN' rule.
- example data.
- options to assess ICC[3,1] (as quantitive agreement index), Cohen's kappa coefficients (as binary classification index).
- options to compare correlation plot to X/Y plot.
- options to transform BA plot to non-parametric LoAs or MAD-based LoAs.
- options to enable 95% CI intervals of bias (mean/median difference) and LoAs.
- options to enable predefined acceptable limits and adjust values.
- data upload option for users to explore graphical tools with their own lab data.
- section on Cq tresholds upon discovery of multi-modal Cq distribution.
- section on linkage analysis with digital PCR.
- link to online laboratory protocol (to be published).

##### correspondence

