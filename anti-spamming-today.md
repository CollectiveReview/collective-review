# Abstract
This is for organizing current understanding of anti-spamming so that we can implement necessary counter-measure to push citation methodology.


# Spamming

## Terminology
 *"the act of spreading unsolicited and unrelated content"* ([Hayati, 2010](https://ieeexplore.ieee.org/document/5610590))
 - **Link spamming**  ([HayatiHenzinger, 2002](https://www.ijcai.org/Proceedings/03/Papers/278.pdf)), where web pages strategically manipulate their links to improve the result of search engines with link-based ranking algorithms (e.g., PageRank and HITS). Link spamming is performed mainly through *link farms* that artificially produces several new referring pages.
 - Link spamming is common even in scientific publications, where researchers may submit a number of incomplete papers for a higher citation-based index ([HernándezAlvarez & Gomez, 2016](https://psycnet.apa.org/record/2016-19366-003)).

## Potential Solutions
- **Resource testing** imposes some small cost on creating new contents, such as computational resources ([Back, 2002](http://www.hashcash.org/papers/hashcash.pdf)) and transaction fees ([Nakamoto, 2008](https://bitcoin.org/bitcoin.pdf)).
- Note that X(Twitter) Community Notes currently 


# Sybil Attack

## Terminology
*"the forging of multiple identities"* ([Douceur, 2002](https://link.springer.com/chapter/10.1007/3-540-45748-8_24))

## Potential Solutions
- Survey papaers: [Levine et al. (2006)](https://www.semanticscholar.org/paper/A-Survey-of-Solutions-to-the-Sybil-Attack-Levine-Shields/dd3fb51e02592dfa1a87c1e55b1a5dcf3edffa9d), [Mohaisen and Kim (2013)](https://arxiv.org/abs/1312.6349).
- **Resource testing** imposes some small cost on creating new peers, such as computational resources ([Borisov, 2006](https://ieeexplore.ieee.org/document/1698607); [Li et al., 2012](https://arxiv.org/abs/1201.2657)), human resources ([Von Ahn et al., 2003](https://link.springer.com/chapter/10.1007/3-540-39200-9_18)) and IP address ([Freedman & Morris, 2002](https://www.cs.princeton.edu/~mfreed/docs/tarzan-ccs02.pdf)).
- **Economic incentive** gives monetary rewards to peers who report malicious peers ([Margolin & Levine, 2007](https://link.springer.com/chapter/10.1007/978-3-540-77366-5_18))
- **Reputation system** detects Sybil attack by constructing a graph structure (referred to as social network or trust graph) from the activities of each peer ([Cheng & Friedman, 2005](https://dl.acm.org/doi/10.1145/1080192.1080202); [Yu, 2011](https://dl.acm.org/doi/10.1145/2034575.2034593)).
- Note that the above approaches have only increased the cost of Sybil attacks. [Douceur (2002)](https://link.springer.com/chapter/10.1007/3-540-45748-8_24) pointed out that we need the validation by centralized authority in order to completely solve Sybil attacks.   
- The proof-of-work, originally a method for spamming ([Back, 2002](http://www.hashcash.org/papers/hashcash.pdf)), in the Bitcoin protocol is very elegant because it eliminates the incentive for individuals to create multiple peers.


# Case Study

## [X(Twitter) Community Notes](https://communitynotes.twitter.com/guide/ja/contributing/sign-up)
- Using time constraint for Spamming, i.e., only accounts that have been registered for at least 6 months can evaluate community notes.
- Using phone number for Sybil attack, i.e., only accounts associated with unique phone number can evaluate community notes.

## [Gitcoin](https://www.gitcoin.co/)
- Under checking...
