# How Does Gesture Help Children Learn Math?

Children learn more from math instruction when the teacher gestures, but *why*? This project tests three processes that gesture might change: how children encode problems, how they evaluate strategies, and how they categorize problems. It then tests whether those changes explain gesture's effect on learning.

**Methods:** randomized pretest–posttest experiment · mixed-effects logistic regression · mediation analysis with bootstrapped confidence intervals · matching (balance vs. sample-size tradeoffs) · R (`lme4`, `emmeans`, `lavaan`, `MatchIt`, `tidyverse`)

## 

## The study

* **Participants:** 64 second and third graders, randomly assigned to watch math instruction with gesture (n = 32) or the same instruction without gesture (n = 32).
* **Design:** pretest → training (instructional video plus a practice problem, repeated three times) → posttest.
* **Measures, collected before and after instruction:**

  * **Problem solving:** equivalence problems such as `3 + 6 + 5 = 3 + \_\_`.
  * **Encoding:** children saw a problem for 5 seconds and then wrote it from memory. Responses were scored by the number of changes needed to match the original, ignoring number errors (adapted from McNeil \& Alibali, 2004).
  * **Strategy evaluation:** children rated four strategies as "very smart," "kind of smart," or "not so smart" (adapted from Siegler \& Crowley, 1994). Two strategies are correct (Equivalence, Grouping) and two are common errors (Add All, Add to Equal).
  * **Problem categorization:** children sorted problems into groups.

All posttest models control for pretest performance and a math fluency (speed) test.

## 

## Key findings

* **Gesture improved learning:** children taught with gesture solved more training and posttest problems correctly.
* **Gesture improved encoding:** they made fewer encoding errors on right-blank problems, the problem type most likely to be misread as ordinary arithmetic.
* **Gesture changed strategy evaluation:** children taught with gesture rated the taught Equivalence strategy more favorably and the incorrect Add-to-Equal strategy less favorably. Ratings of the other correct strategy (Grouping) didn't change, suggesting the effect is specific to the instructed strategy rather than a general preference for correct answers.
* **Encoding and strategy evaluation both predicted problem solving,** and mediation models tested whether they explain gesture's effect. The mediation model showed that encoding and strategy evaluation were both partial mediators of gesture's effect on problem-solving. Therefore, one way that gesture causes children to solve problems better is through aiding children's ability to encode problems and through helping children to evaluate different strategies. 
##

## Designing a matched comparison for a follow-up study

A follow-up experiment adds a third condition (a non-gesture visual indicator) that can't be randomized alongside the original two groups. The matching notebook builds the comparison strategy: it tests matching schemes (optimal vs. nearest-neighbor, with and without exact grade matching, different covariate sets) across caliper widths. Each scheme is scored on covariate balance (standardized mean differences) and on how many participants it keeps. The tradeoff plots in the notebook informed the scheme chosen for the preregistration: nearest-neighbor Mahalanobis matching on pretest problem solving with a 0.5 SD caliper.

## 

## Repository contents

|File|What it does|
|-|-|
|[`analysis/01\_behavioral\_analyses.Rmd`](analysis/01_behavioral_analyses.Rmd)|Problem-solving, encoding, and strategy-rating models; mediation models; problem-grouping analysis; figures|
|[`analysis/02\_matching\_design.Rmd`](analysis/02_matching_design.Rmd)|Comparison of matching schemes and caliper widths for the follow-up study|

## 

## Data

Participant data are not included because they come from child participants and are covered by IRB protections. The notebooks document every processing step.

## 

## About

Part of my dissertation research in the Communication, Cognition, and Learning Lab at the University of Iowa (advisor: Susan Wagner Cook).

