# overview
Reviewing a scientific findings with collective intelligence.

## Abstract 
### Current Review Challenges
Accurately assessing the quality and significance of scientific papers is of utmost importance, yet the current review process proves unsustainable.

A startling **10% of reviewers handle half of all review** requirements[[1]](https://publons.com/static/Publons-Global-State-Of-Peer-Review-2018.pdf). The **average number of refusals** before securing a reviewer for a paper has increased by 46% between 2013 and 2017[[1]](https://publons.com/static/Publons-Global-State-Of-Peer-Review-2018.pdf). As such, it has become increasingly challenging to find suitable reviewers for new papers.

But the solution may not be implementing incentives of reviewing, as 70.4% of researchers answer they reject invitations **because "the article is out of my area of expertise."**[[1]](https://publons.com/static/Publons-Global-State-Of-Peer-Review-2018.pdf)

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

<img src="https://github.com/CollectiveReview/overview/assets/94701070/e0a9ca76-7021-4ced-90bf-37630ca00d2b" height="300px">&emsp;&emsp;<img src="https://github.com/CollectiveReview/overview/assets/94701070/880e4b40-b356-44ab-a2ea-e25470522c14" height="300px">

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
To combat plagiarism, we should implement tamper-proof timestamps for each phase: the creation of a project, visibility alterations of the project, and the submission and accept/reject status of proposals. Additionally, we could employ plagiarism detectors capable of identifying paraphrasing[[2]](https://www.turnitin.com/solutions/ai-writing).

- Metrics:
Citation disparity is a recognized issue, with citation averages varying across fields. For instance, Engineering and Aerospace average 5.65 citations, while Developmental Biology stands at 38.67. Nonetheless, citation net
works form distinctive clusters and it is possible to compute the mean citation count within these clusters. When normalized, the distribution of citations across all articles aligns almost perfectly with a single curve[[3]](https://www.pnas.org/doi/10.1073/pnas.0806977105).

![Screenshot 2023-07-20 at 15 02 24](https://github.com/CollectiveReview/overview/assets/94701070/b9b7b4aa-a1df-423e-8192-7e25ccf600eb)

graph was cited from [[4]](https://www.dashunwang.com/book/the-science-of-science)

- Reciprocal citation:
Transparency is the key to tackling reciprocal citations. Thanks to advancements in network science and scientometrics, we are now able to detect the "rich-club phenomenon" and quantify its prevalence. As long as researchers are alerted about potential cheating, they can conduct investigations.

Although Reciprocal citation might indicate foul play, it could be a result of close relation between projects. In fact, an estimated one in five citations from 1950 to 2010 are reciprocated[[5]](https://epjdatascience.springeropen.com/articles/10.1140/epjds/s13688-019-0199-3).

The publishment of projects may look the following in the collective review on push citation. It is similar to distributed repository systems.

![image](https://github.com/CollectiveReview/overview/assets/94701070/6b16352d-5ec3-4f27-9baa-20d10d255cd9)

> There are many issues not covered here which can be found on our [issues](https://github.com/CollectiveReview/overview/issues) page. If you encounter any problems not mentioned there, feel free to propose your own.

## Potential drawbacks


[1] Publons Global Review Report https://publons.com/static/Publons-Global-State-Of-Peer-Review-2018.pdf<br>
[2] Turn it in https://www.turnitin.com/solutions/ai-writing<br>
[3] Universality of citation distributions: Toward an objective measure of scientific impact https://www.pnas.org/doi/10.1073/pnas.0806977105<br>
[4] The Science of Science https://www.dashunwang.com/book/the-science-of-science<br>
[5] Reciprocity and impact in academic careers https://epjdatascience.springeropen.com/articles/10.1140/epjds/s13688-019-0199-3<br>
