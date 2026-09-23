# Making Critical DNA Evidence Accessible: What Strong Statistics Can Leave Unsaid for the Defense

## With an AI Assistant and an Invitation to Open Review

Monte Miller, PhD; Forensic DNA Experts LLC

## Abstract

A correctly calculated DNA statistic need not answer the proposition a factfinder is being asked to decide. This applied-mathematical article connects three questions: which contributor configurations a comparison evaluates, what the observations resolve about genetic states, and which material conclusions a report expressly communicates. In a strict two-contributor construction, two named people receive separate likelihood ratios exceeding $10^{13}$ against a two-unknown alternative, while their complete-pair likelihood ratio is zero. The comparisons address different configurations; they are not exhaustive assessments of individual contribution. The same construction shows that large relative support can coexist with diffuse genotype uncertainty. Further synthetic examples distinguish population rarity, compatibility, and quantitative discrimination. A comparison of three reports, holding disclosed facts constant, separates derivability, a warning about evaluative scope, and an express joint assessment. Building on established assessment and reporting literature, the article identifies different responses to different overinterpretations: another proposition-specific assessment, clarification of genotype uncertainty, explicit communication of an available conclusion, or reevaluation under another model. It proposes a bounded transparency workflow rather than another statistic for every report. A short legal discussion advances, without attributing a holding, the unresolved hypothesis that McDaniel v. Brown’s concern with unsupported probabilistic meaning may also bear on overstatement of a comparison’s scope. Exact inputs and an accompanying implementation reproduce the central construction and six displayed quantitative settings. Operational validity, improved comprehension, reporting prevalence, and case-specific unfairness are not established.

**Keywords:** forensic DNA; likelihood ratio; joint contribution; genotype uncertainty; proposition selection; evidence communication; population conditioning; reporting.

# 1. Introduction

In my forensic practice, I have encountered cases in which assessments critical to the defense’s disputed proposition were not calculated or expressly reported. That experience motivates this article. A correctly calculated DNA statistic can leave consequential questions unanswered, and the ability to recognize and examine those questions should not be limited to specialists. This article uses explicit mathematical examples to show why the gap matters. The accompanying article-focused AI assistant, Rob, is intended to help readers with different backgrounds explore the reasoning, calculations, assumptions, and limitations. The work is offered for open examination and criticism; the examples do not measure how frequently these omissions occur in practice.

When the article and accompanying guidance are loaded into an AI system, lay readers, attorneys, judges, forensic scientists, and statistical reviewers can ask Rob to explain the calculations, describe the contribution relative to established approaches, and respond to challenges to the reasoning. The guidance includes a map connecting the article’s central arguments and calculations. If you also provide Rob with the computational supplement, he can use the supporting material—including the calculation code and recorded numerical results—to help explain the manuscript. Rob’s role is to explain and defend the arguments within their stated assumptions, acknowledge limitations, and identify where a question goes beyond what the article establishes. His responses may contain errors and should be checked against the manuscript and code. The invitation to open outside review extends to Rob’s explanations.

A DNA statistic becomes meaningful through the question it answers. A population frequency concerns a genetic event under a population model. A genotype posterior concerns uncertainty over genetic states under observations and a prior. A likelihood ratio compares observations under stated propositions. None automatically establishes personal contribution, activity, or guilt.

The difficulty is not always incorrect arithmetic. A calculation can be correct while an inference drawn from it concerns a different proposition. A report can also provide the facts needed to derive a material limitation without expressly reporting the limitation or whether the relevant question was evaluated.

Consider the construction developed below. At each of thirteen independently stipulated loci, the observed allele set is $\{1,2,3,4\}$. Person A carries $2/3$ and person B carries $1/3$. A fits with an unknown partner carrying $1/4$; B fits with an unknown carrying $2/4$. Together, however, A and B lack allele $4$.

Under the stated population and observation models, their separate comparisons yield approximately $6.69\times10^{13}$ and $3.80\times10^{14}$ against two unknown contributors. The complete named pair has likelihood ratio zero. The results do not contradict one another: their numerators describe different configurations.

## 1.1 Audience, precedents, and contribution

This article addresses forensic scientists, statistical researchers, and legal professionals who evaluate or communicate DNA evidence. It is an academic methodological analysis, not a validated courtroom presentation or a standalone reporting template.

Previous work establishes the importance of evaluating multiple persons of interest jointly and addresses how the resulting assessments should be reported. Slooten (2022) develops a hypothesis-based approach to evaluation and reporting, emphasizing the likelihoods of the relevant hypotheses and the additional weights needed for composite individual-contribution comparisons. Duke et al. (2022) investigate compound and conditioned likelihood-ratio behavior. Wivell et al. (2023) expressly recommend reporting when candidates cannot jointly be donors. The ASB 041 ballot draft also addresses proposition selection, attribution to legal parties, joint assessment, and reassessment.

The overlap therefore concerns reporting as well as calculation.

| Precedent | Relevant contribution | Relationship to this article |
|---|---|---|
| Slooten (2022), Introduction | Organizes evaluation around relevant hypotheses and their likelihoods; discusses reporting likelihood tables and the weights needed for composite individual-contribution LRs. | The proposition map below is a compact use of an established approach, not a new attribution method. |
| Duke et al. (2022), Introduction and Sections 3.3–3.7 | Investigates compound and conditioned LR behavior, including sampling-related zeros and atypical peak effects. | The exact structural zero below must be distinguished from computational or observation-model problems. |
| Wivell et al. (2023), Introduction and Section 5 | Discusses alternatives when the defense offers no proposition, joint versus individual evidential weight, and explicit reporting of joint incompatibility. | Explicit joint reporting and caution about party labels are acknowledged precedents. |
| AAFS Standards Board (2021), ASB 041 ballot draft, Foreword and clauses 4.3–4.5, 4.14–4.16 | Addresses party attribution, limitations of chosen propositions, joint assessment, additional comparisons, and reasonable reassessment requests. | The workflow proposed here shares this ground. The cited document is a ballot draft, not evidence of a binding or universally adopted requirement. |

The present contribution is a linked applied-mathematical explanation of three questions:

1. Which contributor configurations does a comparison evaluate?
2. What do the observations resolve about genetic states?
3. Which material conclusions does a report expressly communicate?

The strict construction links two distinct findings: strong support in selected comparisons can coexist with complete-pair incompatibility, and large relative support can coexist with diffuse genotype uncertainty. Example D changes signal strength while holding target rarity fixed; G examines changing quantitative patterns with population-weighted unknown co-contributors. The reporting comparison then holds disclosed facts constant to distinguish a derivable conclusion, a warning about evaluative scope, and an expressly reported assessment.

The analytical purpose is to identify which response a particular overinterpretation requires. A joint-contribution claim may require another proposition-specific assessment. A claim of genotype resolution may require examination of genotype uncertainty. An unstated material conclusion may require explicit reporting rather than another calculation. A conclusion transferred to a different observation mechanism requires reevaluation under that mechanism.

These responses are not interchangeable, and adding another statistic is not a universal remedy. The article develops this integration without claiming a new joint-assessment method, a historical first for each distinction, or an absence of earlier reporting recommendations.

## 1.2 Hierarchy of conclusions

| Evidentiary status | Component | Conclusion and boundary |
|---|---|---|
| Demonstrated mathematical results | Strict construction; matched posterior–LR identities; population-filter calculations | Results follow under the specified models. Application to an actual case requires separate justification. |
| Explanatory illustrations | Synthetic quantitative examples D and G | They distinguish rarity, discrimination, and genotype uncertainty. They do not validate laboratory methods or establish casework prevalence. |
| Constructed reporting analysis | Versions A–C under common disclosed facts | Derivability, a scope warning, and an express joint assessment are different report features. Reader effects are not measured. |
| Normative recommendation | Explicit communication of material assessments and limitations | The justification is transparency, not a demonstrated comprehension benefit or a universal legal obligation. |
| Unresolved applications and interpretation | Implementation-specific conditioning, actual reporting practices, and the proposed McDaniel connection | These require additional evidence or argument. They are not additional demonstrated defects. |

The organizing question is whether the assessment calculated supports the meaning attributed to it. A six-face analogy—observations, model, propositions, mathematics, reporting, and legal context—emphasizes their connections. As with a partially aligned Rubik’s cube, local correctness does not establish coherence of the whole arrangement. The analogy organizes the inquiry; it does not prove alignment or determine legal fairness.

A definite result under stated assumptions can coexist with uncertainty about those assumptions’ suitability for an application. Conversely, questioning applicability does not establish that a particular implementation or report is defective.

---

# Part I — Propositions and mathematical construction

# 2. Essential definitions and conditioning

Let $E$ denote the questioned observations and $I$ the relevant background information. A genotype is an unordered diploid allele pair at one locus. A multilocus profile is a vector of such genotypes. Different people can share a genotype or profile; a genetic state is not a uniquely identified person.

A likelihood ratio compares evidence likelihoods:

$$
\operatorname{LR}(H_1:H_0)
=
\frac{\Pr(E\mid H_1,I)}
{\Pr(E\mid H_0,I)}.
$$

Densities replace point probabilities for continuous observations. A finite reported ratio requires a positive denominator.

An LR does not establish which proposition is true. Posterior odds require prior odds. Contribution assumed within a proposition remains conditional; it is not an established identity. Whether a legal burden is satisfied is a further question.

## 2.1 A common genotype-replacement comparison

Let $\mathcal G$ be the declared genetic state space, $t$ a target state, and $\pi(g)$ the distribution assigned to an alternative person’s genetic state under the stated population and background assumptions.

Unless expressly identified as multilocus, states are single-locus genotypes. For a designated contributor position and contributor count, let $L(g)$ be the probability or density of $E$ when that position’s genotype is fixed at $g$, conditional on $I$. It includes the declared treatment of co-contributor genotypes and other nuisance quantities.

A common-model comparison fixes $t$ in that position and replaces it under the alternative with a population draw:

$$
R=
\frac{L(t)}
{\sum_{g\in\mathcal G}\pi(g)L(g)}.
$$

In these examples,

$$
f(t)=\pi(t).
$$

A person-level interpretation requires person propositions that justify this construction. Fixing a genotype in a position, stipulating that a named person occupies that position, and assessing whether the person contributed anywhere are distinct statements.

Identities using a common $L(g)$ require compatible state spaces, conditioning, and co-contributor and nuisance treatment.

## 2.2 Population assumptions

Under the stipulated Hardy–Weinberg model,

$$
f(a/b)=
\begin{cases}
2p_ap_b,&a\ne b,\\
p_a^2,&a=b.
\end{cases}
$$

For a multilocus profile, a product representation requires appropriate factorization:

$$
f(t)=\prod_{\ell=1}^{m}f_\ell(t_\ell).
$$

Allele frequencies, Hardy–Weinberg proportions, between-person independence, population relevance, and temporal stability are separate assumptions. Hardy–Weinberg proportions alone do not establish independence between relatives or justify using one population distribution for every alternative contributor. Population structure and relationships can require different conditional distributions (National Research Council, 1996, Chapter 4). Reference-selection circumstances also require separate consideration, as discussed in Section 2.3.

The examples stipulate frequencies; they do not estimate temporal change or local-population composition.

## 2.3 Different operations called conditioning

| Operation | What is specified | Consequence |
|---|---|---|
| Treating a reference genotype as background | An observed genetic state is known. | Under fixed frequencies and independence, it need not change another unrelated person’s genotype distribution. |
| Assuming a person contributed | A proposition assigns that person to the contributor configuration. | The evidence likelihood changes through that configuration, even if population frequencies remain fixed. |
| Conditioning on a family relationship | A pedigree or relationship connects observed and unobserved genotypes. | Unknown-genotype predictions can depend on observed family genotypes. |
| Updating shared population uncertainty | Relevant people share uncertain population parameters within a joint model. | Reference observations can affect predictive genotype distributions if their selection and relevance are modeled appropriately. |

Observed genotypes are not altered by these operations; distributions over unknown states may change.

Additional references are not automatically unbiased population samples. Relatives, randomly sampled residents, and people selected through a DNA match provide different information. Geographic proximity or the tested person’s ancestry does not, by itself, determine the appropriate alternative-contributor distribution.

Questioned-mixture alleles are evidence to explain, not automatic independent population draws. Reference information and selection circumstances must be treated coherently across propositions without double counting.

When LRs differ, identify whether the difference arises from propositions, observations, background, population or relationship distributions, or nuisance treatment. Numerical disagreement does not establish an error, and numerical agreement does not establish identical meaning.

This conditioning framework is conceptual. It establishes no particular correction, direction of LR change, or implementation defect.

# 3. Strong separate support with complete-pair incompatibility

## 3.1 Strict construction

Consider exactly two diploid contributors and an observation rule recording their complete allele set without dropout, drop-in, or error.

At every stipulated locus,

$$
E_\ell=\{1,2,3,4\}.
$$

A has genotype $2/3$ and B has genotype $1/3$. Frequencies for alleles $1$ through $5$ are

$$
(0.07,0.08,0.09,0.10,0.66).
$$

With four distinct observed alleles and two diploid contributors, every fitting configuration partitions the four alleles into two disjoint heterozygotes. There are three unordered partitions and six ordered assignments.

A requires a partner carrying $1/4$. B requires a partner carrying $2/4$. Together A and B supply alleles $1$, $2$, and $3$, but not allele $4$.

## 3.2 Proposition map

Under this two-person model, the following scenarios distinguish the named-person inclusion possibilities:

| Scenario | Complete contributor configuration | Unknown-person convention |
|---|---|---|
| $H_{AB}$ | A and B | Both named people form the complete pair. |
| $H_{AU}$ | A and one other person | The other person is neither A nor B. |
| $H_{BU}$ | B and one other person | The other person is neither A nor B. |
| $H_{UU}$ | Two other people | They are distinct people, neither of whom is A or B. |

Identity exclusion does not imply genotype exclusion. Under the fixed-frequency independent-person model, unknown genotypes remain population-distributed and may match either reference. Both references are background information under every scenario.

Writing

$$
L_{XY}=\Pr(E\mid H_{XY},I),
$$

the displayed comparisons are

$$
R_A=\frac{L_{AU}}{L_{UU}},\qquad
R_B=\frac{L_{BU}}{L_{UU}},\qquad
R_{AB}=\frac{L_{AB}}{L_{UU}}.
$$

The first two are selected comparisons. A composite assessment of “A contributed” would combine $H_{AB}$ and $H_{AU}$; its non-contribution alternative would combine $H_{BU}$ and $H_{UU}$. Calculating that comparison requires specified distributions within each side. The separate LR $R_A$ does not supply them. The corresponding distinction applies to B.

This follows the established distinction between likelihoods for specified configurations and composite individual-contribution comparisons discussed by Slooten (2022). No equal weighting of the four scenarios is assumed here.

## 3.3 Positions and assignment

The contributor positions are exchangeable bookkeeping labels, not empirically resolved major and minor roles. Let $L_{A,1}$ and $L_{A,2}$ be the full-profile likelihoods with A assigned to the first and second positions, respectively, and a population-weighted unknown in the other position. Symmetry gives

$$
L_{A,1}=L_{A,2}.
$$

Prespecified assignment weights therefore give

$$
\lambda L_{A,1}+(1-\lambda)L_{A,2}=L_{A,1},
\qquad 0\leq\lambda\leq1.
$$

This is a mixture over assignments, not the sum of two unweighted copies of the same likelihood. The assignment concerns the whole profile, not a different named-person position selected independently at each locus.

The equality is model-specific. It does not provide a general conversion for fraction-linked positions.

## 3.4 Separate and joint results

Each compatible ordered assignment has probability $4p_1p_2p_3p_4$ under two independent population draws. Thus the one-locus denominator is

$$
D=24p_1p_2p_3p_4=0.0012096.
$$

The separate numerator probabilities are

$$
L_A=2p_1p_4=0.014,
\qquad
L_B=2p_2p_4=0.016.
$$

Here $D$, $L_A$, and $L_B$ denote the one-locus likelihoods for $H_{UU}$, $H_{AU}$, and $H_{BU}$, respectively.

| Comparison against two unknowns | One-locus LR | Thirteen independent loci |
|---|---:|---:|
| A with an unknown | Approximately $11.5741$ | Approximately $6.69\times10^{13}$ |
| B with an unknown | Approximately $13.2275$ | Approximately $3.80\times10^{14}$ |
| A and B as the complete pair | $0$ | $0$ |

The complete pair fails the observation rule. The separate results remain valid for their stated comparisons.

![Separate compatible pairs and incompatible named pair](figure-1.svg)

**Figure 1. Separate fit does not establish joint fit under the strict two-person model.** A’s genotype $2/3$ requires partner $1/4$, whereas B’s genotype $1/3$ requires partner $2/4$. Together, A and B fail to supply observed allele $4$. Each stated configuration is compared with two unknown contributors under the specified Hardy–Weinberg model. Both named references are background information; unknown identities exclude A and B but not their genotypes. Positions are exchangeable bookkeeping labels. Separate comparisons are selected scenarios, not exhaustive individual-contribution assessments. Symbols represent allele copies, not peak heights. Full-profile values refer to thirteen independent loci, not merely the illustrated locus. The joint zero concerns the complete pair under complete observation without dropout, drop-in, or error; it is not exclusion under every larger mixture or other model.

## 3.5 What the incompatibility does and does not establish

The joint result concerns the complete named pair, not the non-contribution of each individual. If the disputed proposition is that A and B form the complete pair, it directly challenges that proposition. If the dispute concerns A contributing with another person, it does not resolve it.

A larger contributor configuration or another mechanism capable of explaining the observed allele requires its own evaluation. Dropout alone cannot supply allele $4$, absent from both references.

A structural zero also differs from a computational failure to explore supported configurations. Duke et al. (2022) and Wivell et al. (2023) discuss sampling-related zeros in probabilistic-genotyping calculations; Duke et al. also examine atypical peak behavior. Their operational examples do not determine the likelihoods in this strict model, and this construction is not a contradiction of their empirical findings.

Thirteen loci amplify the contrast but are unnecessary for its existence. If a repeatable experiment has selected-scenario LRs $r_A>1$ and $r_B>1$, a zero joint likelihood, and a positive common alternative likelihood, independent identically specified repetitions give

$$
R_A^{(n)}=r_A^n,\qquad
R_B^{(n)}=r_B^n,\qquad
R_{AB}^{(n)}=0.
$$

This is a stipulated existence result, not a claim that arbitrarily many real forensic loci are available or that marginal likelihoods remain independent after integrating shared nuisance parameters.

# 4. Large relative support and genotype uncertainty

## 4.1 Matched posterior–likelihood identities

For genotype prior $q(g)$,

$$
w_q(g)=
\frac{q(g)L(g)}
{\sum_{h\in\mathcal G}q(h)L(h)},
$$

provided the normalizing likelihood is positive.

Under a uniform target-genotype prior,

$$
w_U(g)=\frac{L(g)}{\sum_{h\in\mathcal G}L(h)}.
$$

Under the alternative-person population prior,

$$
w_\pi(g)=
\frac{\pi(g)L(g)}
{\sum_{h\in\mathcal G}\pi(h)L(h)}.
$$

Consequently,

$$
R=\frac{w_\pi(t)}{f(t)},
$$

when $f(t)>0$, the normalizing likelihood is positive, and state spaces, conditioning, and conditional likelihoods are compatible.

This decomposes the same LR. It is not independent evidence, and $w_U(t)$ must not be substituted for $w_\pi(t)$.

A contributor position is occupied under the assumed model. Its genotype posterior describes uncertainty about that position’s genetic state; it does not establish which named person occupies it. The target frequency is not generally the mixture evidence-likelihood denominator, which averages observation likelihoods over states.

Recovery of likelihoods from exported weights requires additional conditions, addressed in Appendix A.1. A weight-table heading alone does not establish normalization, prior, completeness, state semantics, or nuisance treatment.

## 4.2 The strict construction

Under the two-unknown population model, the six compatible ordered assignments have equal prior products. Each compatible genotype in a designated position therefore has posterior probability $1/6$ at one locus.

For A,

$$
f_{A,\ell}=2p_2p_3,
\qquad
R_{A,\ell}=\frac{1}{12p_2p_3}
=\frac{1}{6f_{A,\ell}}.
$$

Similarly,

$$
R_{B,\ell}=\frac{1}{6f_{B,\ell}},
\qquad
f_{B,\ell}=2p_1p_3.
$$

Across thirteen independent loci,

$$
w_\pi(t)=6^{-13}\approx7.66\times10^{-11},
$$

for either specified compatible target profile in that position. There are

$$
6^{13}=13{,}060{,}694{,}016
$$

compatible profiles for the position. These are genetic states, not identifiable people.

Writing $f_A$ and $f_B$ for the target profile frequencies,

$$
R_A=\frac{6^{-13}}{f_A},
\qquad
R_B=\frac{6^{-13}}{f_B}.
$$

A small genotype posterior can be much larger than a still smaller population probability. Large relative support and diffuse genotype uncertainty are therefore compatible.

The posterior is relevant when the attributed claim is that the observations resolve the target genetic state. Under the specified model and prior, it describes how uncertainty remains distributed over genetic states in the designated position. The LR instead measures relative support for the stated comparison. These quantities are not rival estimates of named-person contribution, and the matched identity supplies neither a correction to the LR nor independent evidence.

Neither posterior is A’s or B’s contribution probability, and its complement is not a probability of innocence.

## 4.3 Different genotypes and different people

Another person may carry the target genotype. A comparison against other genotypes therefore differs from a comparison against another person.

For $0<f(t)<1$, let $A_{\ne t}$ be the mean likelihood over non-target genotypes under the alternative-person distribution conditional on not carrying $t$. The alternative-person likelihood is

$$
f(t)L(t)+\bigl(1-f(t)\bigr)A_{\ne t}.
$$

If $L(t)>0$ and $C=L(t)/A_{\ne t}$,

$$
R=
\frac{1}{f(t)+\bigl(1-f(t)\bigr)/C},
$$

with the limiting interpretation when $A_{\ne t}=0$.

The matching-genotype branch is already part of the alternative, not a missing independent factor. Since

$$
\sum_g\pi(g)L(g)\geq f(t)L(t),
$$

the matched comparison satisfies

$$
R\leq\frac{1}{f(t)}.
$$

This is not a universal bound for arbitrary person-level comparisons. It requires the stated matching branch and common conditional likelihood. If $f(t)=1$, the common-model LR is $1$ when the evidence likelihood is positive. If $f(t)=0$, use the underlying likelihoods directly; no finite reciprocal-frequency bound follows.

For later illustrations, define the uniform-reference different-genotype comparison

$$
B=
\frac{(M-1)L(t)}
{\sum_{g\ne t}L(g)},
\qquad M=|\mathcal G|>1.
$$

At fixed $M$,

$$
B=\frac{(M-1)w_U(t)}{1-w_U(t)}.
$$

This is a transformation of the target weight for a specified alternative, not additional independent evidence. Appendix A develops its boundaries and explains why it does not generally determine the different-person LR.

---

# Part II — What the statistics count and compare

# 5. Population filters count different sets

Return to the strict frequencies and observed set $\{1,2,3,4\}$.

A compatibility rule defines a set $\mathcal C(E)$ and assigns it population mass

$$
P_{\mathrm{comp}}(E)=\sum_{g\in\mathcal C(E)}\pi(g).
$$

The rule defining the set is essential.

For target $2/3$,

$$
f(2/3)=2p_2p_3=0.0144.
$$

Under the complete two-person rule, a contributor must carry one of the six heterozygotes

$$
1/2,\quad1/3,\quad1/4,\quad2/3,\quad2/4,\quad3/4.
$$

Their total population probability is

$$
P_{\mathrm{comp},2}
=\sum_{1\leq i<j\leq4}2p_ip_j
=0.0862.
$$

Requiring only that both alleles lie in the observed set additionally admits the four homozygotes. Its probability is

$$
P_{\mathrm{set}}
=(p_1+p_2+p_3+p_4)^2
=0.1156.
$$

A homozygote passes the outer rule but cannot, with one other diploid contributor, explain four distinct observed alleles under the strict model.

| Population event | States counted | Probability |
|---|---|---:|
| Exact target genotype | One genotype | $0.0144$ |
| Strict two-person compatibility | Six heterozygotes | $0.0862$ |
| Both alleles inside the observed set | Ten genotypes | $0.1156$ |

The squared allele-frequency sum is associated with single-locus inclusion calculations in the combined-probability-of-inclusion literature, subject to the assumptions governing eligible alleles and loci (Bieber et al., 2016, Rule R5 and principle P1). The six-heterozygote quantity here is explicitly called strict two-person compatibility rather than assigned a guideline label.

![Three nested population genotype filters](figure-2.svg)

**Figure 2. Three population filters count different genotype sets.** For observed alleles $\{1,2,3,4\}$, target $2/3$ has population probability $0.0144$. Under exactly two diploid contributors, complete allele observation, and no dropout, drop-in, or error, the six heterozygotes each admit a complementary partner; their total population probability is $0.0862$. Requiring only that both alleles belong to the observed set also admits four homozygotes, giving $0.1156$. Probabilities use the stated Hardy–Weinberg model. Cell areas do not represent probabilities, and outside-set genotypes are not displayed. These are population events, not posterior probabilities of contribution.

The differences arise from different counted events, not competing estimates of one probability. A mechanism such as dropout may change the relevant compatibility set; these rules must not be transferred without reevaluation.

# 6. Fixed rarity with changing quantitative signal: example D

Examples D and G use a Gaussian observation model, not the strict rule.

D uses six allele categories with frequencies

$$
(0.30,0.24,0.18,0.13,0.09,0.06),
$$

giving twenty-one unordered genotypes.

The known major genotype is $1/2$. The target in the designated minor position is $5/6$, with

$$
f(t)=2(0.09)(0.06)=0.0108.
$$

The target proposition fixes $5/6$ in that position. The alternative replaces it with a population-distributed genotype. The known major and prescribed fractions remain the same.

Observations are deterministic synthetic signals. Evaluation uses independent Gaussian channel errors with $\sigma=0.035$. Fractions are inputs, not estimates. These are settings at one toy locus, not independent loci. Section 14 gives exact signals and the likelihood specification.

| Setting | Exact minor fraction | Signal at each target allele | $R$ | $w_U(t)$ |
|---|---:|---:|---:|---:|
| D1 | $0$ | $0$ | $1$ | $0.047619$ |
| D6 | $1/9$ | $1/18$ | $27.9507$ | $0.541729$ |
| D10 | $1/5$ | $1/10$ | $91.9453$ | $0.997158$ |

At zero minor fraction, varying the genotype in that position changes no predicted signal. Thus,

$$
R=1,\qquad
w_U(t)=\frac{1}{21},\qquad
w_\pi(t)=f(t).
$$

This is an uninformative boundary, not dropout, exclusion, or evidence of a detectable second contributor.

As signal increases, the observations distinguish the target genotype more strongly under the model, while its population rarity remains unchanged.

![Fixed rarity with changing minor signal](figure-3.svg)

**Figure 3. Fixed genotype rarity with changing quantitative discrimination in example D.** Three settings at one synthetic locus use known major genotype $1/2$, target $5/6$ in the minor position, and prescribed fractions. Heights represent supplied deterministic channel signals. The LR $R$ compares the target genotype in that position with a population-distributed replacement, retaining the same major genotype, fractions, and Gaussian model. The target population probability remains $0.0108$. The weight $w_U$ uses a uniform target-genotype prior and is not a named-person contribution probability. Zero minor fraction is an uninformative boundary, not dropout or exclusion. Evaluation uses independent Gaussian channel errors with $\sigma=0.035$. Widths and shapes are schematic, not simulated laboratory electropherograms. Statistics are rounded; settings are not independent loci.

The choice of prior remains consequential. At D6,

$$
w_U(t)\approx0.541729,
\qquad
w_\pi(t)\approx0.301868.
$$

These are different model-dependent quantities, not inconsistent estimates of one posterior.

# 7. The same alleles with different quantitative information: example G

G uses the same population frequencies and Gaussian error scale. Synthetic signals are generated from

$$
5/6,\qquad3/4,\qquad1/2,
$$

in that fraction order.

During evaluation, all contributor genotypes are unknown except where the target proposition fixes $5/6$ in the first position. Other genotypes are population-weighted. Under the alternative, all three positions are population-weighted.

Prescribed fractions remain the same under both propositions. Unequal fractions distinguish positions, so the strict construction’s assignment symmetry must not be assumed.

| Setting | Exact contributor fractions | $R$ | $w_U(t)$ |
|---|---|---:|---:|
| G1 | $(1/3,1/3,1/3)$ | $6.17284$ | $0.201837$ |
| G4 | $(19/45,29/90,23/90)$ | $63.6999$ | $0.826856$ |
| G10 | $(3/5,3/10,1/10)$ | $92.5924$ | $0.99999875$ |

Every setting has the same six positive channels. The quantitative pattern changes. At G10,

$$
y=(0.05,0.05,0.15,0.15,0.30,0.30).
$$

Under the prescribed fractions and error model, the highest channels strongly distinguish the target in the first position.

Equal-height observations do not require equal marginal genotype likelihoods: population weighting of complementary co-contributor configurations matters.

The target probability remains $0.0108$, and

$$
R\leq\frac{1}{0.0108}\approx92.59.
$$

The final result approaches this common-model bound. The final uniform-reference different-genotype comparison is approximately

$$
B=1.5974\times10^7.
$$

Its greater magnitude does not make it a better answer to the different-person question. At fixed genotype-universe size, it is a transformation of $w_U(t)$.

![The same alleles with changing quantitative patterns](figure-4.svg)

**Figure 4. The same six allele channels can support different quantitative discrimination in example G.** Three settings at one synthetic locus are generated from $5/6$, $3/4$, and $1/2$ in the displayed fraction order. Generator truth is not treated as known contributor information during evaluation. The target proposition fixes $5/6$ in the first position and population-weights the other genotypes; the alternative population-weights all three positions. Fractions are prescribed under both propositions. All channels have positive signal, but their relative heights change. The target probability remains $0.0108$; $w_U$ uses a uniform target-genotype prior with population-weighted co-contributors and is not a personal contribution probability. Gaussian channel errors have $\sigma=0.035$. Heights represent supplied signals; widths and shapes are schematic. Fractions and statistics are rounded, and settings are not independent loci.

# 8. What each quantity contributes

| Quantity | Question answered | What it does not supply by itself |
|---|---|---|
| Population genotype probability | How frequent is the target genotype under the declared distribution? | Contribution probability or evidence-based genotype resolution |
| Population compatibility | What population mass belongs to a rule-defined genotype set? | Identification of actual alternative contributors |
| Genotype posterior | How is uncertainty distributed over genetic states under a prior and model? | Automatic named-person attribution |
| Likelihood ratio | How do observations compare under stated propositions? | Posterior odds without prior odds; for these contributor-level comparisons, activity attribution or a legal decision |

The Gaussian model assigns positive density to every finite observation under every genotype configuration. Small likelihoods in D and G are not the strict model’s structural impossibilities.

The examples therefore require different interpretive safeguards. A rare target may receive no support when its position has no signal. A strongly discriminating observation may approach the matching-genotype bound. A large LR may coexist with diffuse genotype uncertainty. None of those observations supplies the result for a different contributor proposition.

---

# Part III — Reporting the disputed proposition

# 9. A bounded comparison of three reports

This part compares constructed reports under common evidence and assumptions. It examines:

1. Information sufficient for an informed reader to derive a conclusion.
2. Explicit warnings about the scope of reported comparisons.
3. Express reporting of the assessment relevant to the dispute.

Actual reader understanding and legal adequacy are separate questions. This is neither a comprehension experiment nor a survey of laboratory practice.

The principal dispute is whether A and B form the complete two-person configuration under the strict model.

## 9.1 Common information

All versions receive:

- The observed allele sets and both reference genotypes.
- The strict two-contributor observation rule.
- The fixed-frequency independent population model.
- The exclusion of A and B as unknown identities, not genotypes.
- The selected-scenario status of the separate comparisons.
- The independent-locus assumption for full-profile values.

All therefore contain the facts needed to derive the named-pair incompatibility.

The quoted passages are read with this common information. They are not standalone reporting templates.

## 9.2 Version A — Accurate baseline report

> Under the stated model, the observed thirteen-locus allele sets are approximately $6.69\times10^{13}$ times as likely if A and one unknown person contributed as if two unknown people contributed.
>
> Separately, the observations are approximately $3.80\times10^{14}$ times as likely if B and one unknown person contributed as if two unknown people contributed.
>
> Each result compares the likelihood of the observations under its stated propositions. Neither number is a probability that A or B contributed, or a probability of guilt.

This constructed baseline has not been established as representative of a particular laboratory’s practice.

## 9.3 Version B — Baseline plus explicit interpretation

Version B includes A and adds:

> The two results concern different configurations. The unknown partner in A’s comparison need not be the partner in B’s comparison. Neither separate numerator proposes A and B together.
>
> Consequently, the size of these separate results does not determine the result of a comparison concerning A and B as the complete contributor pair.
>
> Another person may share a named person’s genotype. These calculations must therefore not be described as identifying a unique person merely by distinguishing a genotype.
>
> Even establishing DNA contribution would not, by itself, establish the activity responsible for deposition or guilt.

B adds interpretation without additional numerical results.

## 9.4 Version C — Clarification plus the joint assessment

Version C includes B and adds:

> We also evaluated A and B as the complete two-person contributor configuration, against the same two-unknown alternative.
>
> At each locus, A’s genotype $2/3$ requires a partner carrying $1/4$. B’s genotype $1/3$ requires a partner carrying $2/4$.
>
> Together, A and B supply alleles $1$, $2$, and $3$, but not observed allele $4$.
>
> The named pair therefore has zero likelihood under this strict model, and its joint LR is $0$.
>
> This result concerns A and B as the complete two-person configuration. It does not exclude their contribution somewhere within a larger mixture or under a different observation model.

C reports the joint assessment, its basis, and its limits.

# 10. Reporting analysis and a bounded recommendation

## 10.1 What C adds to B

All three versions disclose the common information needed to derive the joint incompatibility. None adds new biological observations.

Version A reports accurate selected comparisons but does not expressly identify their joint limitation. Version B makes a substantive improvement: it warns that the separate numerators evaluate different configurations and do not determine the result for the named pair. B must not be grouped with a presentation that invites an unqualified joint-contribution inference.

C goes further. It expressly states that the joint configuration was assessed, reports the incompatibility, explains the missing allele, and identifies the model-specific scope. Its increment over B is the joint conclusion and its basis, not the first warning against combining the separate results.

An explicit assessment identifies the assessor’s evaluation rather than requiring the recipient to reconstruct both the result and whether the disputed proposition was evaluated. That is a transparency rationale. It does not establish that C improves comprehension or that A or B is legally inadequate.

## 10.2 Relevance and factorization

The relevant assessment depends on the dispute. If A’s contribution is accepted and B’s disputed, comparing A and B with A and an unknown addresses a different question from comparing A and B with two unknowns. This does not justify assuming A’s contribution when it remains disputed.

The separate LRs in Section 3 cannot simply be multiplied to obtain the named-pair LR. Their numerators describe different configurations and do not provide the conditional likelihood factors required for that calculation.

This does not deny valid factorization among appropriately matched compound and conditional comparisons, as discussed by Wivell et al. (2023, Section 2.3 and Appendix B). It rejects multiplication of these particular selected results as independent factors for the named pair.

Nor is the joint zero universally “defense evidence.” Its legal significance must be tied to the proposition challenged; it does not identify which individual contributed or establish either person’s exoneration.

## 10.3 Existing reporting recommendations

The distinction between evaluation and communication is analytically useful but is not itself a novelty claim. Wivell et al. (2023, Section 5) expressly state that when candidates cannot jointly be donors, or the compound LR strongly disfavors their joint contribution, “it is still necessary to state this explicitly.”

Slooten (2022, Introduction) advocates keeping the relevant hypothesis likelihoods central and reporting their table, while allowing individual LRs as well. That approach can preserve information obscured by isolated scalar comparisons.

The ASB 041 ballot draft addresses limitations of selected propositions and their possible divergence from parties’ positions, joint assessment, and reasonable reassessment requests. Clause 4.14 requires documenting why a subset of evaluative LRs is selected for reporting and noting the existence of additional LRs in the case file; it does not require every numerical result to appear in the report. Its Foreword discusses avoiding unintended attribution of propositions to prosecution or defense.

These are direct precedents. Acknowledging them does not require endorsing every proposed conditioning practice or assuming a disputed person contributed. The contribution here is the linked analysis of different interpretive problems and the distinct responses they require.

## 10.4 Bounded transparency workflow

For this recommendation, an assessment is material when it addresses a proposition actually advanced or contested, or supplies a limitation needed to avoid overstating the meaning attributed to a reported result. The proposition or attributed meaning must be identified. This is a working criterion, not a legal materiality test.

The recommendation does not require an analyst to anticipate every possible defense or require a defendant to disclose a theory. Responsibility is bounded by the question communicated, the work performed, the method’s capabilities, and relevant information subsequently received.

Issuing a report, giving testimony, and advocating from another person’s assessment are distinct communicative acts. Under this recommendation, responsibility attaches to the assessment and meaning a person communicates in context. A later speaker’s overstatement is not automatically an analytical or reporting error by the original assessor. When a broader proposition is subsequently put to the assessor, however, the assessor should identify whether the existing evaluation addresses it and communicate any established limitation material to that question.

For example, if separate results are used to support A and B as the complete named pair, their established joint incompatibility directly limits that attributed meaning. If only a selected individual-with-unknown comparison is at issue and no broader meaning is identifiable, the mere existence of a known joint result does not automatically make it material. The recommendation distinguishes communicating an established limitation from undertaking a new evaluation.

| Situation | Recommended reporting response |
|---|---|
| A material limitation is already established | State the limitation, its basis, and model-specific scope. Do not leave an incompatible broader interpretation unqualified. |
| A relevant comparison has not been evaluated | Identify non-evaluation where needed to prevent the result from being understood as answering that question. Non-evaluation is not an adverse result. |
| A reasonable later request or changed proposition arises | Provide a route for reassessment. Identify changed assumptions or comparisons and explain whether earlier conclusions retain their scope. |
| The available method cannot validly assess the comparison | State the limitation. Do not substitute a computable but materially different comparison without identifying the difference. |
| A speculative configuration has not been made material | No general obligation to calculate it follows. Reconsider that status if later information makes it relevant. |

The practical sequence is to record the question, identify the propositions assessed, state established material limitations, identify relevant non-evaluation or methodological inability, and provide a route for reasonable reassessment.

A numerical LR is not always necessary. In the strict example, explaining that the complete named pair cannot supply an observed allele communicates the essential incompatibility. If a numerical comparison is given, its alternative and model must be clear.

The appropriate detail may differ among a technical report, lawyer-facing explanation, testimony, and a jury-facing exhibit. The figures here are scholarly illustrations, not validated exhibits for those other settings.

# 11. The separate role of genotype uncertainty

The genotype-posterior discussion addresses claims about genotype resolution. It is not an alternative route to a probability of innocence.

Two potential supplements remain distinct:

- An express assessment of the complete named pair.
- A description of genotype uncertainty under a declared prior and model.

A–C examines the first. It does not demonstrate the practical or legal value of the second.

A genotype posterior may expose an unsupported assertion that the mixture resolves a particular genotype. It does not follow that every large LR requires a posterior display. Alternative-genotype likelihoods and the matching-genotype branch may already be included in the LR denominator, even when their distribution is not displayed.

Let $G_j$ denote the genotype in position $j$, and let POI mean person of interest. The alternative $G_j\ne t$ does not exhaust non-contribution by the POI: another person can carry $t$. If contribution anywhere is disputed, uncertainty over positions also matters.

Similarly, a relative’s possession of some alleles does not establish a matching profile or a compatible mixture explanation. Under ordinary inheritance without mutation, parents collectively carry alleles transmitted to a child, but neither necessarily has the child’s profile, and a parental mixture generally includes additional alleles. Any such contributor explanation requires its own evaluation. Appendix B.4 provides a limited transmission illustration.

These distinctions identify when uncertainty may matter to an attributed meaning. They do not establish a general requirement to eliminate every alternative genotype before DNA evidence supports contribution. Weak discrimination may be uninformative rather than strongly exclusionary.

# 12. McDaniel: legal context and an interpretive hypothesis

In McDaniel v. Brown, the Supreme Court distinguished random match probability from the probability that the defendant was not the DNA source, and distinguished source attribution from guilt, 558 U.S. 120, 128 (2010). It also emphasized the importance of fair and reliable presentation of persuasive DNA evidence, id. at 136. These statements provide context for careful probabilistic communication; they do not prescribe this article’s reporting format.

The procedural setting matters. The Court required consideration of all admitted trial evidence in the sufficiency analysis, id. at 131. It did not resolve the experts’ relative credibility and explained that the claim failed even assuming Mueller’s estimate, id. at 132 and n.5. It treated the separately advanced DNA due-process claim as forfeited and reversed and remanded, with ineffective-assistance issues remaining, id. at 134–136.

Justice Thomas, joined by Justice Scalia, objected to the extended discussion of the post-trial Mueller report because it had no place in the relevant sufficiency inquiry, id. at 137–138. He declined to join the discussion he characterized as dicta concerning that report’s effect on the constitutional analysis. That objection should not be described as a general rejection of accurate probabilistic communication.

An RMP is a probability, whereas $H_d$ is a proposition. In an appropriately specified ideal resolved-match model, the RMP may equal $\Pr(E\mid H_d,I)$. It does not thereby equal $\Pr(H_d\mid E,I)$. Nor does its use establish that the selected scientific alternative represents a defendant’s adopted explanation or exhausts relevant non-contribution scenarios. A logical complement also does not supply every distribution required to calculate its evidence likelihood.

We do not attribute to McDaniel a holding that an RMP-based likelihood ratio is improper, or that the Court prescribed the scope of a defense proposition. We advance a narrower interpretive hypothesis: its concern with assigning unsupported meaning to DNA statistics may also bear on presenting a restricted scientific comparison as though it evaluates a materially different defense explanation.

The proposed connection has a reasoned basis. Probability transposition and overstatement of evaluative scope can both assign a statistic a meaning its calculation does not establish. They are nevertheless different errors, and a decision addressing one does not automatically establish a legal principle governing the other. General language about fair presentation is not sufficient by itself to resolve that question.

If supported, the extension could matter even where the reported statistic is correctly calculated: the concern would be the broader assessment attributed to it. Neither that legal extension nor its application to an actual report is established here. The proposed connection does not establish an admissibility rule, a constitutional violation, or a basis for relief in any particular proceeding; those conclusions would require additional authority and case-specific analysis. The mathematical results and independent transparency rationale do not depend on acceptance of the hypothesis.

# 13. Synthesis and conclusion

The integrated analysis separates problems that should not be addressed as though they were interchangeable.

| Attributed meaning that requires examination | Relevant response |
|---|---|
| Separate support is treated as joint support | Evaluate the joint configuration or identify its non-evaluation. |
| A selected comparison is treated as an exhaustive individual-attribution assessment | Identify the additional scenarios and distributions required for a composite comparison. |
| A large LR is treated as genotype resolution | Examine genotype uncertainty under the declared prior and model. |
| Derivable information is treated as an expressly reported assessment | State the material conclusion and its scope. |
| A strict-model impossibility is transferred to another observation mechanism | Reevaluate under that mechanism rather than importing the zero. |

This is the practical purpose of the integrated mathematical treatment. The strict construction demonstrates a proposition mismatch and, through the matched posterior identity, a separate resolution distinction. D and G show why rarity alone does not determine discrimination. A–C isolates an explicit-reporting difference without changing biological information.

The six-face organization is useful insofar as it tracks dependencies. Changing the contributor count can change likelihoods and exclusion language. Changing the prior can change a genotype posterior without changing conditional likelihoods. Changing the dispute can change which comparison matters. Changing population or relationship assumptions requires reconsidering the affected distributions rather than applying an unexplained final-number adjustment.

The analysis does not establish how frequently these issues arise in practice, whether a particular report creates an unsupported inference, or whether additional explanation improves understanding. Actual reporting records, operational validation, implementation documentation, participant research, or case-specific legal analysis would be required for those different claims. No probabilistic-genotyping export or population-conditioning implementation was audited here.

Correct calculation does not, by itself, establish that an assessment addresses the disputed proposition or supports the meaning attributed to it. That question concerns the calculation’s propositions and assumptions as well as its communicated scope. Equally, a mathematical illustration alone does not establish impaired fairness. Existing practices may already handle the relevant distinctions, and a report need not contain every computable statistic to communicate adequately.

The linked results make the distinction concrete. Strong selected separate support does not establish complete-pair contribution; large relative support does not establish genotype resolution; and disclosing facts sufficient to derive a conclusion is not identical to expressly reporting its assessment. These are different limitations, not cumulative proof of one operational defect. The proposed response is to identify the material question, determine whether the assessment performed addresses it, and communicate the conclusion and its limits.

# 14. Methods and numerical reproducibility

## 14.1 Strict enumeration

The strict observation likelihood is one for configurations whose allele-set union equals the observed complete set and zero otherwise. Unknown genotypes are independent Hardy–Weinberg draws from the fixed frequencies. Full-profile products use stipulated locus independence.

The accompanying implementation enumerates fifteen unordered genotypes and all 225 ordered contributor pairs using exact rational arithmetic. It checks the denominator, separate numerators, named-pair incompatibility, designated-position posterior, profile count, and matched posterior–frequency identities.

Reference independence is a separate stipulation, not a consequence of Hardy–Weinberg proportions alone.

## 14.2 Quantitative likelihood

Each allele copy contributes half its contributor fraction to the corresponding channel:

$$
\mu_a=\sum_j\frac{\phi_j}{2}n_a(g_j),
$$

where $n_a(g_j)$ counts allele copies.

Observations are deterministic signals constructed from the generating genotypes and prescribed fractions. Evaluation uses

$$
K(y\mid\mathbf g,\boldsymbol\phi)
\propto
\exp\left[
-\frac{\sum_a(y_a-\mu_a)^2}{2\sigma^2}
\right],
\qquad
\sigma=0.035.
$$

The omitted Gaussian factor is common to the configurations and comparisons in each setting.

For D, with known major genotype $m=1/2$,

$$
L_D(g)=K(y\mid m,g;\boldsymbol\phi).
$$

For G,

$$
L_G(g)=
\sum_{h,k\in\mathcal G}
\pi(h)\pi(k)
K(y\mid g,h,k;\boldsymbol\phi).
$$

The quantities $R$, $w_U(t)$, $w_\pi(t)$, and $B$ are then calculated from the common $L_D$ or $L_G$ using Section 4’s definitions. All twenty-one target-position genotypes are included; G enumerates all ordered co-contributor pairs.

This model has no stutter, censoring, degradation, laboratory dropout, or drop-in mechanism. It permits negative observations and has positive density at every finite signal vector. It is a mathematical toy model, not validated casework software.

## 14.3 Exact inputs

All population frequencies and $\sigma$ stated above are treated as exact decimals before floating-point likelihood evaluation.

Signal arrays use allele-channel order $1$ through $6$.

| Setting | Exact fraction vector | Exact signal array |
|---|---|---|
| D1 | $(1,0)$ | $(1/2,1/2,0,0,0,0)$ |
| D6 | $(8/9,1/9)$ | $(4/9,4/9,0,0,1/18,1/18)$ |
| D10 | $(4/5,1/5)$ | $(2/5,2/5,0,0,1/10,1/10)$ |
| G1 | $(1/3,1/3,1/3)$ | $(1/6,1/6,1/6,1/6,1/6,1/6)$ |
| G4 | $(19/45,29/90,23/90)$ | $(23/180,23/180,29/180,29/180,19/90,19/90)$ |
| G10 | $(3/5,3/10,1/10)$ | $(1/20,1/20,3/20,3/20,3/10,3/10)$ |

D’s fraction order is known major $1/2$, then target-position genotype $5/6$. G’s generating order is $5/6$, $3/4$, $1/2$.

## 14.4 Implementation and numerical results

The implementation uses only the Python standard library. It uses exact rational arithmetic for the strict construction and explicit rational inputs for the quantitative examples. Gaussian calculations use floating-point log likelihoods and log-sum-exp marginalization.

| Quantity | Numerical result |
|---|---:|
| Strict denominator | $0.0012096$ |
| Strict A numerator | $0.014$ |
| Strict B numerator | $0.016$ |
| Strict joint LR | $0$ |
| Strict A thirteen-locus LR | $6.68838628684560\times10^{13}$ |
| Strict B thirteen-locus LR | $3.79504262792686\times10^{14}$ |
| Strict target-position profile posterior | $7.65656096662972\times10^{-11}$ |
| Compatible position profiles | $13{,}060{,}694{,}016$ |

| Setting | $R$ | $w_U(t)$ |
|---|---:|---:|
| D1 | $1$ | $0.0476190476190476$ |
| D6 | $27.9507017179653$ | $0.541728524905921$ |
| D10 | $91.9452838579187$ | $0.997158306143090$ |
| G1 | $6.17283949624454$ | $0.201837236145844$ |
| G4 | $63.6999391814617$ | $0.826855819812353$ |
| G10 | $92.5923708630398$ | $0.999998747977069$ |

At D6, the population-prior target posterior was $0.301867578554025$. The final G value of $B$ was $15{,}974{,}128.3188332$.

The recorded numerical results were obtained using CPython 3.11.14. All 132 programmed checks passed: 22 for the strict construction and population filters, 78 for the six D/G settings, and 32 for supporting examples. These are related assertions, not 132 independent validations.

The strict calculations use exact comparisons where applicable. Main-table D/G values are checked against their displayed rounding, with a small floating-point allowance. Higher-precision comparisons and numerical identities use explicit tolerances recorded in the script. The tested values agree with the displayed results.

The complete code, running instructions, and numerical-results record are included in the supplementary material.

## 14.5 Scope of the numerical checks

Supporting checks combine finite enumeration with direct formula evaluation. In particular, the source-posterior and occupancy examples, fifteen-locus population-filter products, and conditional-relatedness arithmetic are formula checks, not independent validation of their modeling assumptions. The programmed checks do not certify every general derivation or every possible application.

The quantitative calculations cover the six D/G settings specified in Section 14.3. They do not validate commercial software, actual laboratory observations, reader comprehension, or legal claims.

The reporting analysis compares constructed texts under common facts. It contains no participant observations.

Figure widths and shapes are illustrative; the statistical model uses channel heights, not drawn peak geometry.

---

# Appendix A. Genotype posteriors and uniform-reference comparisons

## A.1 Posterior recovery and marginal priors

For a complete posterior under known positive prior $q(g)$,

$$
w(g)=\frac{q(g)L(g)}{\sum_hq(h)L(h)},
\qquad
L(g)\propto\frac{w(g)}{q(g)}.
$$

Under a known positive prior, uncorrected posterior weights are proportional to likelihoods when the prior is constant over positive-likelihood states. Uniformity over zero-likelihood states is unnecessary.

State definitions, conditioning, and nuisance treatment must agree. Unknown omitted tails or incompatible aggregation prevent unrestricted recovery. Probabilistic-genotyping systems use differing approaches, making model-specific interpretation essential (Gill et al., 2021). No actual software export was examined here.

A flat joint distribution need not induce a flat marginal. With two labelled contributors whose genotypes are AA, AB, and BB, assign equal mass to the seven ordered configurations AA/AB, AA/BB, AB/AA, AB/AB, AB/BB, BB/AA, and BB/AB. The first contributor’s marginal probabilities are $2/7$, $3/7$, and $2/7$.

With a constant subsequent likelihood, those remain the posteriors. Treating them as uniform-prior likelihoods falsely favors AB. Dividing by the actual prior recovers equal likelihoods.

If configurations were selected using the evidence being evaluated, their distribution is conditional on that selection and cannot be reused as an unconditional prior for the same evidence.

## A.2 Uniform-reference comparison and a counterexample

For $M>1$ atomic states,

$$
B=\frac{(M-1)L(t)}{\sum_{g\ne t}L(g)}
=\frac{(M-1)w_U(t)}{1-w_U(t)}.
$$

Its inverse on the finite interior domain is

$$
w_U(t)=\frac{B}{B+M-1}.
$$

This is an application of the posterior-odds identity, not additional evidence (Kass and Raftery, 1995). At fixed $M$, rankings and receiver-operating-characteristic curves remain unchanged under corresponding threshold transformation. The same numerical threshold on different scales need not give the same decisions.

In general, $B$ and $f(t)$ do not determine $R$. Take three genotypes with population probabilities $0.1$, $0.8$, and $0.1$, the first being the target. Likelihoods $0.6$, $0.3$, and $0.1$ give $B=3$ and $R\approx1.935484$. Swapping the last two likelihoods leaves $B$ and $f(t)$ unchanged but gives $R\approx3.529412$.

The population weighting, not merely the sum of alternative likelihoods, matters.

## A.3 Universe definition and prior dilution

Adding zero-likelihood states while holding existing likelihoods fixed increases $B$ by spreading the uniform alternative’s mass more thinly. This is prior sensitivity, not new evidence. Its relationship to diffuse-prior discussions should not be mistaken for independent data support (Bartlett, 1957).

For twenty toy loci with twenty-five alleles per locus, each locus has $325$ unordered genotypes. The product of twenty factors of $324$ is approximately

$$
324^{20}\approx1.6251753\times10^{50}.
$$

This is the multiplier in a product of locus-specific comparisons against genotypes differing at every locus, subject to factorization. It is not the multiplier for a whole-profile alternative excluding only the target profile. Equal likelihoods cancel the multiplier exactly.

A physical allele ladder is not automatically a complete biological genotype universe.

## A.4 Structural support, truncation, and precision

If $k>1$ states have positive likelihood, including $t$, then $B$ factors into $(M-1)/(k-1)$ times the ratio of the target likelihood to the mean positive alternative likelihood. When every genotype has positive likelihood, $k=M$.

A threshold is not a structural zero. If the retained alternative likelihood sum is $A$ and the omitted sum is $T$,

$$
B=\frac{(M-1)L(t)}{A+T}.
$$

For $A>0$, this equals the truncated result multiplied by $A/(A+T)$. If $A=0<T$, calculate directly rather than multiplying an infinite value by zero.

Aggregation preserves the comparison only when atomic prior masses and likelihood contributions are retained. Treating displayed categories as newly equally weighted states changes the model.

Positive target likelihood with zero alternative likelihood gives an infinite $B$ under an extended-real convention. If all likelihoods are zero, the ratio is undefined.

A displayed posterior of $1.0000$ establishes neither condition. With nearest rounding of a complete posterior under a uniform target-genotype prior and $M=55$, it implies only the lower bound

$$
B\geq1{,}079{,}946.
$$

That bound does not apply to a posterior renormalized after truncation.

## A.5 Alternative-specific expectations

Consider fifty-five genotypes and fifty-five observations. Conditional on a genotype, its corresponding observation has probability $0.84$; each other observation has probability $0.16/54$. Fix the target before observing the evidence.

The uniform-reference $B$ is $283.5$ on the corresponding observation and approximately $0.160475483$ otherwise. Under its uniform different-genotype alternative, the first event has probability $0.002962963$, and the mean of $B$ is one.

Under a different-person alternative allowing all fifty-five genotypes uniformly, including the target, that event has probability $1/55$, and the mean of $B$ is approximately $5.312103$.

The corresponding person-level LR is $46.2$ on the target observation and approximately $0.162962963$ otherwise, with mean one under that alternative.

An expectation property under one alternative therefore does not automatically transfer to another. This example does not establish comprehensive calibration or operational performance.

## A.6 Multilocus alternatives and descriptive summaries

Multiplying locus-specific uniform-reference comparisons tests the alternative that the genotype differs at every locus, provided likelihoods and alternative weights factorize. It does not test difference somewhere in the profile.

With two loci, two genotypes per locus, independent uniform priors, and factorizing likelihoods, target posterior $0.8$ at each locus gives joint posterior $0.64$. The every-locus alternative gives Bayes factor $16$; the uniform joint alternative excluding only the target profile gives $5.333333$.

Genetic independence does not establish marginal-likelihood factorization when nuisance parameters are shared across loci.

Target weight, rank, top-three mass, entropy, and reciprocal squared-weight effective counts can describe genotype uncertainty. They remain prior- and model-dependent; aggregation can change them. Multiplying posterior odds by an effective count creates no LR interpretation by itself.

# Appendix B. Supporting population and nuisance examples

## B.1 Occupancy and posterior source attribution

Under $K-1$ independent alternative persons, each with matching probability $f$, the probability that at least one matches is

$$
1-(1-f)^{K-1}.
$$

This is a pre-observation occupancy probability, not the probability another person contributed.

For a separate idealized source model, suppose exactly one of $K$ exchangeable candidates is the source, the person of interest was identified independently of the questioned DNA, and the other candidate profiles remain unobserved independent draws. For an error-free resolved match,

$$
\Pr(P\mid E,I)=\frac{1}{1+(K-1)f},
$$

where $P$ denotes the person of interest being the source.

For $f=10^{-6}$, the posterior is approximately $0.999901$ for $100$ candidates, $0.990100$ for $10{,}000$, and $0.50000025$ for one million. With one million candidates, the pre-observation probability of another matching carrier is approximately $0.632120$.

The quantities differ because their events and conditioning differ. This is not an instruction to determine prior odds by counting everyone who might conceivably have been nearby.

The ideal resolved-match LR is $1/f$. It incorporates match-frequency information but does not supply posterior source probability without prior odds.

## B.2 Binary-mixture nuisance treatment

Consider observed alleles $7$, $8$, $9$, and $10$ with frequencies $0.07$, $0.08$, $0.09$, and $0.10$, and target $8/9$.

Target probability is $0.0144$, allele-set inclusion is $0.1156$, and strict compatibility is $0.0862$. Under independent population draws, the target-plus-unknown likelihood is $0.014$, the two-unknown likelihood is $0.0012096$, and the LR is approximately $11.574074$.

For a separate uniform-reference illustration, define ten alleles: the four observed and six unobserved alleles collectively carrying mass $0.66$. They form fifty-five genotypes. The allocation among unobserved alleles does not affect this strict likelihood because configurations containing them are incompatible.

With a uniform target-genotype prior and population-weighted co-contributor, the six positive likelihoods are the complementary-genotype frequencies

$$
0.0180,\quad0.0160,\quad0.0144,\quad0.0140,\quad0.0126,\quad0.0112.
$$

They give $B\approx10.470914$. Making the co-contributor uniform instead equalizes the six likelihoods and gives $B=10.8$.

These are different nuisance models, not interchangeable calculations of one comparison.

## B.3 Multilocus population filters

Repeating Section 5’s frequencies at fifteen independent loci with target $2/3$ gives:

| Event | One locus | Fifteen loci |
|---|---:|---:|
| Target genotype | $0.0144$ | $2.373763\times10^{-28}$ |
| Strict two-person compatibility | $0.0862$ | $1.077976\times10^{-16}$ |
| Both alleles inside observed set | $0.1156$ | $8.797667\times10^{-15}$ |

The filters are nested but answer different questions. Multiplying a probability by an explicitly modeled candidate count gives an expected count, not identified alternative contributors or a source posterior.

This fifteen-locus illustration is separate from the thirteen-locus strict construction.

## B.4 Conditional relatedness

Take three allele sets with population masses $0.28$, $0.29$, and $0.32$. Under independent allele draws, an unrelated person’s inside-set probability is

$$
(0.28\times0.29\times0.32)^2=0.000675168256.
$$

If paternal transmission is inside each set with probability one and the other transmitted allele is an independent population draw, the child’s probability is

$$
0.28\times0.29\times0.32=0.025984.
$$

The unrelated probability is the square of the child probability under these assumptions. This is not a universal relationship for relatives and does not test parental contribution or identify a particular child.

---

# Data, code, and supplementary materials

All examples use synthetic finite models. No confidential casework records, laboratory exports, or participant data are used.

The model specifications and exact inputs are given in Section 14 and the appendices. The [supplementary material](supplemental.md) contains the complete standard-library Python implementation, instructions for running it, the numerical-results record, and a map connecting the supporting material to the article. No external dataset is required.

The accompanying vector figures are `figure-1.svg`, `figure-2.svg`, `figure-3.svg`, and `figure-4.svg`. Their captions specify the represented quantities and model boundaries. In Figures 2–4, $f(t)$ denotes the target genotype population probability, not a contribution posterior. Peak shapes and widths in Figures 3–4 are schematic.

**Declarations**

**Monte Miller PhD**

**No funding declared.**

**Author asserts no competing interest.**

**Ethics and consent:** The study uses synthetic models and no confidential casework or participant data. [Author confirmation and journal-required declaration to be completed.]

**AI assistance:** AI tools assisted with analytical framing, numerical implementation, drafting, figure programming, literature-comparison drafting, and revision.
# References

AAFS Standards Board. (2021). *Formulating Propositions for Likelihood Ratios in Forensic DNA Interpretations*. ASB Standard 041, First Edition 2021, ballot draft, file `041_Std_Ballot02.pdf`. The cited document is a ballot draft; no binding or adoption status is asserted. https://www.aafs.org/sites/default/files/media/documents/041_Std_Ballot02.pdf

Bartlett, M. S. (1957). A comment on D. V. Lindley’s statistical paradox. *Biometrika*, 44(3–4), 533–534. https://doi.org/10.1093/biomet/44.3-4.533

Bieber, F. R., Buckleton, J. S., Budowle, B., Butler, J. M., and Coble, M. D. (2016). Evaluation of forensic DNA mixture evidence: protocol for evaluation, interpretation, and statistical calculations using the combined probability of inclusion. *BMC Genetics*, 17, 125. https://doi.org/10.1186/s12863-016-0429-7

Duke, K., Cuenca, D., Myers, S., and Wallin, J. (2022). Compound and Conditioned Likelihood Ratio Behavior within a Probabilistic Genotyping Context. *Genes*, 13(11), 2031. https://doi.org/10.3390/genes13112031

Gill, P., Benschop, C., Buckleton, J., Bleka, Ø., and Taylor, D. (2021). A review of probabilistic genotyping systems: EuroForMix, DNAStatistX and STRmix. *Genes*, 12(10), 1559. https://doi.org/10.3390/genes12101559

Kass, R. E., and Raftery, A. E. (1995). Bayes factors. *Journal of the American Statistical Association*, 90(430), 773–795. https://doi.org/10.1080/01621459.1995.10476572

McDaniel v. Brown, 558 U.S. 120 (2010). https://www.govinfo.gov/content/pkg/USREPORTS-558/pdf/USREPORTS-558-120.pdf

National Research Council. (1996). *The Evaluation of Forensic DNA Evidence*. Washington, DC: National Academies Press. https://doi.org/10.17226/5141

Slooten, K. (2022). The comparison of DNA mixture profiles with multiple persons of interest. *Forensic Science International: Genetics*, 56, 102592. https://doi.org/10.1016/j.fsigen.2021.102592

Wivell, R., Kelly, H., Kokoszka, J., Daniels, J., Dickson, L., Buckleton, J., and Bright, J.-A. (2023). An Investigation into Compound Likelihood Ratios for Forensic DNA Mixtures. *Genes*, 14(3), 714. https://doi.org/10.3390/genes14030714