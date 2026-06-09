# Bland–Altman Agreement Analysis for Molecular Carriage Surveillance of Bacteria in Polymicrobial Samples – A Tutorial

<i>Disclaimer: This page is being worked on. The page is currently incomplete and the text is somewhat rough around the edges.</i>

## Overview
The human oral cavity and gut is composed of a plethora of bacterial species, which have adapted to specific micro-sites, different bacterial communities, or metabolic niches. It has been estimated that the oral cavity contains approx. 700 bacterial species [<i>ref</i>], many of which are present in low abundance and frequently co-occur with closely-related species. In such settings, confidently identifying a target bacterial population becomes difficult when closely-related bacteria frequently engage in gene exchange or share a high degree of genomic similarity due to ancestral recombination or a common ancestor. Examples include <i>Streptococcus pneumoniae</i>, <i>Neisseria meningitidis</i>, <i>Haemophilus influenzae</i> and <i>Streptococcus pyogenes</i> in saliva, as well as pathogenic <i>Escherichia coli</i> in the gut. To address this, we have developed a sensitive culture-independent detection strategy termed the dual-target (or "Two-to-Tango") approach [1].

The dual-target approach uses agreement statistics (Fig. 1) to determine whether two genetic markers exhibit conditional dependence. Demonstrating such dependence between genetic markers in highly polymicrobial specimens can be used to confirm that a specific bacterial population can be individually quantified. While correlation quantifies the strength of a relationship, agreement assesses whether two methods are likely to measure the same quantity of a kind [2]. This distinction reveals whether the genetic markers are jointly measuring the abundance of strains from a single bacterial population, or instead reflecting two distinct populations.

<iframe src="https://wmiellet.github.io/assets/schematic_fig.html" width="100%" height="350" frameborder="0"></iframe> 

###### Fig. 1: Molecular detection challenged when facing different specimens with differing degree of polymicrobial composition. (A) Suspension of a pure culture with bacterial strain possessing two genes, gene A and B, which are used to detect presence of bacterial population. (B) Suspension of mixed bacterial community with bacterial strain present from panel A as well as other bacterial strains, all of which contain neither gene A or gene B. (C) Suspension of mixed bacterial community, containing bacterial strain from panel A, as well as other bacterial strains, including strains positive for either gene A or gene B. By adapting the method proposed by Bland and Altman and applying a believe-the-negative rule [3], we can monitor whether paired measurements of genetic markers exhibit conditional dependence. When applied to a set of samples positive for both targets, this information can be used to assess whether both targets are derived from the same bacterial population. <i>AI-produced illustration.</i>

## Producing an Agreement Plot
Unlike a correlation plot, where each axis represents one genetic marker, an agreement plot readily allows one to inspect two assays for conditional dependence. In an agreement plot the <i>x</i>-axis represents the mean of the two measurements (from marker A and marker B), and the <i>y</i>-axis represents the difference between them. The limits of agreement (LoAs) define the interval within which 95% of the differences fall. To evaluate the precision of these limits, 95% confidence intervals can be added. If the limits of agreement exceed a predefined acceptable range, the two genetic markers cannot be considered reliable for detecting a single bacterial species with sufficient confidence. As a rule of thumb, we recommend a predefined acceptable limit of 2 Cq (equivalent to a 4 fold difference in concentration) [2]. When the LoAs (and their respective 95% CIs) don't exceed the predefined limits, the two targets can be said to exhibit conditional dependence in the set of samples. 
##### <i>mention that by comparing acceptable limits against bias (mean/median difference) we can account for slight differences in amplification efficiency between assays, as we are not setting the acceptible limits around the limit of equality (LoE) but rather around bias</i>

### Assumptions of the Method
The proposed method rests on two assumptions: (I) the differences between genetic marker measurements are non normally distributed, and (II) the difference between the two markers is not proportional to the mean of the two measurements [2]. When one of the two markers exhibits reduced specificity and samples often contain strains that are positive for only one of the markers, non parametric limits of agreement should be considered [5]. When using non-parametric limits, the median difference is indicated in the agreement plot as well as the limits of agreement based on the 2.5 and 97.5th percentile. <i>low degree of proportionality is to be expected among weakly positive samples due to Poisson sampling variation. Moreover, slight differences in PCR efficiency may contribute to proportionality among strongly positive samples.</i>

## Types of Agreement Plots
We distinguish between two types of agreement plots: the <i>population-specific agreement plot</i> and the <i>serotyping agreement plot</i>. In the former, two genetic markers with presumed population-specific accuracy are compared, whereas in the latter, serotype-specific markers are ranked by abundance in each sample and primary serotypes are compared against a population-specific marker. Serotype-specific markers are allowed to have lower abundance than population-specific markers to account for multiple serotype carriage. However, when the abundance of a serotype-specific marker strongly exceeds that of the population-specific marker, this finding suggests conditional independence, i.e., the two markers are not measuring the same bacterial population. In such cases, the serotype-specific quantification can be attributed to confounding by a different bacterial population. For the serotype agreement plot, the acceptable limit can be either 2 Cq or the limits of agreement derived from markers A and B themselves [4].

### population-specific agreement plot
When both markers accurately detect the same bacterial population, the difference between their measurements shows minimal bias, and the limits of agreement (LoAs) stay within predefined acceptable thresholds (Fig. 2). In this case, data points tend to cluster along the x‑axis and lie close to the line of equality (LoE). This indicates that the two genetic markers are conditionally dependent, supporting the validity of the dual‑target combination.

<iframe src="https://wmiellet.github.io/assets/plot.html" width="100%" height="350" frameborder="0"></iframe>

###### Figure 2: [Legend text].

In some cases, binary agreement in classification may be suboptimal due to the presence of strains or closely related species that are positive for only one of the two markers. When such strains are common, the targeted bacterial population may co‑occur, further reducing agreement between the markers.

If two genetic markers are rarely found together in a given bacterial population, conditional independence between them is observed. Here, the bias between markers is often substantial, and the LoAs exceed the predefined acceptable limits (Fig. 3). Data points tend to scatter randomly across the Bland–Altman plot.

<iframe src="https://wmiellet.github.io/assets/plot2.html" width="100%" height="350" frameborder="0"></iframe>

###### Figure 3: [Legend text].

### serotyping agreement plot
While the population-specific agreement plot aims to validate the use of a dual-target combination for a given specimen type (and demographic group), the serotyping agreement plot serves to demonstrate that a serotype-specific marker is conditionally dependent on a population-specific marker. In other words, serotypes are only found as a subset of the targeted bacterial population. When this holds true, measurements from serotype-specific markers do not substantially exceed those from population-specific markers. This relationship can be evaluated by comparing measurements of the primary (i.e., dominantly detected) serotypes against those of the population-specific markers. Accordingly, the upper limit of agreement (LoA) must remain within the predefined acceptable limit. The lower LoA is not meaningful in this context, because secondary (subdominant) serotypes may occasionally be detected. Serotype-specific assays with suboptimal diagnostic specificity can be readily identified in this manner (Fig. 4}. 

<iframe src="https://wmiellet.github.io/assets/plot3.html" width="100%" height="350" frameborder="0"></iframe> 

###### Figure 4: [Legend text].

Importantly, assays must be evaluated at the assay level. Individual measurements cannot be interpreted in isolation, because even for suboptimal assays where strains of the targeted bacterial population are known to be present, good agreement for a single sample may simply occur by random chance.

### agreement indices
Agreement indices can be used to complement agreement plot and guide interpretation. Nevertheless, it's important to note that indices can never capture all the information displayed by an agreement plot. So at best, agreement indices can be used as complementary tool but not as replacement of agreement plots.

A comprehensive discussion of indices is not within the scope of this text, therefore discussion is limited to indices deemed useful for the current analysis.
<i>Refer to Bland-Altman paper on comparison to correlation coefficients.</i>

#### ICC
The intraclass correlation coefficient (ICC) is a measure of agreement for continuous measurements obtain from multiple methods. The ICC(3,1) is a specific type of ICC, namely a two-way mixed-effects model that treats methods as fixed effects and assesses consistency (rather than absolute agreement). Where absolute agreement measures whether two methods produce the same measurements, 'consistency' describes whether two methods are correlated in an additive manner. In other words, whether method 1 equates to method 2 plus some systematic error. This distinction is of importance for the dual-target approach as assays used two detect different genetic markers  often have minor differences in amplification efficiency (and probe quenching/hydrolysis, etc.). The ICC(3,1) index can account for such systematic bias. For this reason, we advocate the usage of the ICC(3,1) to describe quantitative agreement between paired measurements from two genetic markers.

#### Cohen's kappa
Cohen's kappa (κ) is a chance‑adjusted measure of agreement for categorical classifications (such as presence/absence) between two methods [<i>ref</i>]. It contrasts the observed agreement rate with the agreement anticipated by chance, where a κ value of 0.81 or higher typically indicates near‑perfect agreement. Such index values are anticipated when the two markers are assumed to show conditional dependence. The Cohen's kappa index can be a useful addition to the agreement plot, particularly when single‑positive and double‑negative samples are also displayed. In such cases, the agreement plot captures both the quantitative and the binary agreement between the two genetic markers.

#### Light's kappa
When two genetic markers exhibit poor agreement in binar classification due to one of two targets, an investigator can consider Light's kappa coefficient to assess whether validity of the target combination for a particular specimen type can be observed. Light's kappa coefficient is an assymetric kappa coefficient [6], that can be useful when a specimen type harbors a highly prevalent off-target bacterial population with one of two genetic markers present. Similar to Cohen's kappa coefficient, Light's kappa coefficient can only be used as complemtary tool to an agreement plot (and ICC index).

## Produce an agreement plot with your own data!
<i>Upload your data as CSV file and create your own agreement plots.</i>

[population-specific agreement plot](https://wmiellet.github.io/assets/data_upload4.html). [example data](https://github.com/wmiellet/wmiellet.github.io/blob/9087058aa72a7267c7db94fe34eff3c2b88181f1/example_data/conditional_dependence_Bland_Altman.csv)

[test2](https://wmiellet.github.io/assets/data_upload5.html).

[serotyping agreement plot](https://wmiellet.github.io/assets/serotype_ranking4.html). [example data](https://github.com/wmiellet/wmiellet.github.io/blob/9087058aa72a7267c7db94fe34eff3c2b88181f1/example_data/example_serotype_bland_altman_data.csv)

## Limitations
While combining two genetic markers (particularly those belonging to different connectivity networks) can improve the specificity of molecular detection, the proposed method has a number of limitations. Importantly, diagnostic specificity can be excquisitely monitored but not controlled for when due to subgroup variation in bacterial composition, a specimen type exhibits lack of conditional dependence. In such instances, investigators can consider to redesign molecular targets in an attempt to improve diagnostic specificity or utilize alternative approaches, such a microfluidics-mediated linkage analysis [7]. Furthermore, it is important to recognize that agreement plots (and agreement indices) provide validatiy at the assay level (i.e., performance across a set of samples). They cannot distinguish between false-positive and true-positive results for individual samples, as good agreement for a single sample may occur by random chance. Finally, the predefined acceptable limits used to evaluate the limits of agreement (LoAs) are arbitrary, and the LoAs themselves are insufficient to guide interpretation on their own.

## Recommendations & Concluding Remarks
We encourage others to routinely monitor agreement between genetic markers. Due to spatiotemporal variation in sample composition or study group composition, the diagnostic specificity of molecular assays fluctuates. This phenomenon is known as the spectrum effect and is an important source of methodological bias across studies, study groups (e.g., age groups) and specimen types [8]. To avoid these pitfalls, we recommend assessing agreement between genetic markers on a per study subgroup basis, and for annual cross sectional studies, on a yearly basis within a single subgroup. In a similar vein, we recommend following the MIQE reporting guidelines for qPCR‑based analyses, as adherence to these guidelines may also help reduce interstudy variation [9].

We hope the information presented in this tutorial will help familiarize researchers with the dual-target approach and agreement analysis. In our view, these methods may help reduce variation across studies and enhance the quality of evidence generated by molecular carriage surveillance studies.

### Reference list
1. Miellet, Willem R., et al. "It takes two to tango: combining conventional culture with molecular diagnostics enhances accuracy of Streptococcus pneumoniae detection and pneumococcal serogroup/serotype determination in carriage." Frontiers in microbiology 13 (2022): 859736.
2. Bland, J. Martin, and Douglas G. Altman. "Comparing methods of measurement: why plotting difference against standard method is misleading." The Lancet 346.8982 (1995): 1085-1087.
3. Marshall, Roger J. "The predictive value of simple rules for combining two diagnostic tests." Biometrics (1989): 1213-1222.
4. Miellet, Willem R., et al. "Streptococcus pneumoniae carriage studies in adults: Importance, challenges, and key issues to consider when using quantitative PCR-based approaches." Frontiers in Microbiology 14 (2023): 1122276.
5. Light, Richard J. "Measures of response agreement for qualitative data: some generalizations and alternatives." Psychological bulletin 76.5 (1971): 365.
6. Bland, J. Martin, and Douglas G. Altman. "Measuring agreement in method comparison studies." Statistical methods in medical research 8.2 (1999): 135-160.
7. Miellet, Willem R., et al. "Digital PCR linkage analysis resolves Streptococcus pneumoniae signature from commensal interference in saliva samples: identifying wolves among sheep in wolf’s clothing." Microbiology spectrum 14.5 (2026): e03131-25.
8. Mulherin, Stephanie A., and William C. Miller. "Spectrum bias or spectrum effect? Subgroup variation in diagnostic test evaluation." Annals of Internal Medicine 137.7 (2002): 598-602.
9. Bustin, Stephen A., et al. "MIQE 2.0: revision of the minimum information for publication of quantitative real-time PCR experiments guidelines." Clinical chemistry 71.6 (2025): 634-651.

##### citation:
Miellet, Willem R., et al. "It takes two to tango: combining conventional culture with molecular diagnostics enhances accuracy of Streptococcus pneumoniae detection and pneumococcal serogroup/serotype determination in carriage." Frontiers in microbiology 13 (2022): 859736.


##### correspondence
email: w.r.miellet-2(at)umcutrecht.nl

##### other links
##### [PCR efficiency estimation](https://wmiellet.github.io/assets/pcr_efficiency.html). [example data](https://github.com/wmiellet/wmiellet.github.io/blob/9087058aa72a7267c7db94fe34eff3c2b88181f1/example_data/PCR_efficiency_example_data.csv)

##### [qPCR Cq multi-modality cutoff assessment](https://wmiellet.github.io/assets/bimodality_cutoff.html). [example data](https://github.com/wmiellet/wmiellet.github.io/blob/9087058aa72a7267c7db94fe34eff3c2b88181f1/example_data/Cq_bimodality_example_data.csv)
