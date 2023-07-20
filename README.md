# overview
Reviewing a scientific findings with collective intelligence.

## Abstract 
### Current Review Challenges
Accurately assessing the quality and significance of scientific papers is of utmost importance, yet the current review process proves unsustainable.

A startling **10% of reviewers handle half of all review** requirements[]. The **average number of refusals** before securing a reviewer for a paper has increased by 46% between 2013 and 2017[]. As such, it has become increasingly challenging to find suitable reviewers for new papers.

But the solution may not be implementing incentives of reviewing, as 70.4% of researchers answer they reject invitations **because "the article is out of my area of expertise."**[]

### The question
The question, then, is how can we maintain a reliable assessment framework to distinguish between impactful, reliable papers and those of lesser importance?

### Collective Review: A Solution?
In the search for solutions, academia is turning towards aggregating individual assessments, as seen in practices like open review. Such assessments using collective intelligence are referred to as "Collective Review". It is characterized by:

- Large number of individuals contributing to the assessment
- Each individual reviewing a small part or subset of a paper
- Gradual validation of the paper through the aggregation of reviews.

In this context, we propose the concept of 'push citation' as a foundation for collective review. We begin by defining push citation, followed by a description of its functionality. We subsequently examine the issues in a naive implementation of push citation and discuss enhancements. Finally, we explore potential drawbacks and unsuitable conditions.

see also: https://gnt.place

## Push Citation 
In the push citation methodology, an author presents her work to ongoing research projects. These projects then have the option to either accept or reject the proposal. If a project accepts her work, it incorporates her research into its list of contributions (citations). Consequently, the reliability and impact of a project can be measured through its acceptance rate.

> Pull citation is building a new block on the previous research, and<br>
> Push citation is improving a current research project by proposing a project.

## Issues and improvements in naive implementation
There are several problems for naive push citaion.
### Issues
- Plagiarism
Consider the scenario where Researcher A proposes thier research results to Project X. After X rejects the proposal, researcher B, a member of X, copied the whole content of A. Then X accepts the suggestion from B. Furthermore, B might also suggest duplicated content to many other projects.
Plagiarism also occurs before A's proposal especially if A is opening her project to publc and accepting other's suggestion.

- Unreliable acceptance metrics
Publication rates and average citations vary across disciplines. As such, it is challenging to determine a universally applicable and reliable acceptance count for a paper.

- Reciprocal citation
A project can have unreasonably high acceptance if some group of people mutually accept their projects. This could disrupt the priority of recommendations and potentially compromise the integrity of the entire review system.

### Response

- Plagiarism:
To combat plagiarism, we should implement tamper-proof timestamps for each phase: the creation of a project, visibility alterations of the project, and the submission and accept/reject status of proposals. Additionally, we could employ plagiarism detectors capable of identifying paraphrasing[].

- Metrics:
Citation disparity is a recognized issue, with citation averages varying across fields. For instance, Engineering and Aerospace average 5.65 citations, while Developmental Biology stands at 38.67. Nonetheless, citation networks form distinctive clusters and it is possible to compute the mean citation count within these clusters. When normalized, the distribution of citations across all articles aligns almost perfectly with a single curve[].

- Reciprocal citation:
Transparency is the key to tackling reciprocal citations. Thanks to advancements in network science and scientometrics, we are now able to detect the "rich-club phenomenon" and quantify its prevalence. As long as researchers are alerted about potential cheating, they can conduct investigations.

Although Reciprocal citation might indicate foul play, it could be a result of close relation between projects. In fact, an estimated one in five citations from 1950 to 2010 are reciprocated[].

> There are many issues not covered here which can be found on our [issues](https://github.com/CollectiveReview/overview/issues) page. If you encounter any problems not mentioned there, feel free to propose your own.

## Potential drawbacks
- 
