---
title: Hadoop
---

## Hadoop

This is a stub. [Help our community expand it](https://github.com/freeCodeCamp/guide-articles/tree/master/articles/Data-Science/Hadoop/index.md).

[This quick style guide will help ensure your pull request gets accepted](https://github.com/freeCodeCamp/guide-articles/blob/master/README.md).

<!-- The article goes here, in GitHub-flavored Markdown. Feel free to add YouTube videos, images, and CodePen/JSBin embeds  -->

#### More Information:
<!-- Please add any articles you think might be helpful to read before writing the article -->

Origin of the Name Hadoop:

The name Hadoop is not an acronym; it’s a made-up name. The project’s creator, Doug Cutting, explains how the name came about: 
The name my kid gave a stuffed yellow elephant. Short, relatively easy to spell and pronounce, meaningless, and not used elsewhere: 
those are my naming criteria. Kids are good at generating such. Googol is a kid’s term. Subprojects and “contrib” modules in Hadoop 
also tend to have names that are unrelated to their function, often with an elephant or other animal theme (“Pig,” for example). 
Smaller components are given more descriptive (and therefore more mundane) names. This is a good principle, 
as it means you can generally work out what something does from its name. For example, the jobtracker9 keeps track of MapReduce jobs.

Hadoop at Yahoo
Building Internet-scale search engines requires huge amounts of data and therefore large numbers of machines to process it. 
Yahoo! Search consists of four primary components: the Crawler, which downloads pages from web servers; the WebMap, 
which builds a graph of the known Web; the Indexer, which builds a reverse index to the best pages; and the Runtime, 
which answers users’ queries. The WebMap is a graph that consists of roughly 1 trillion (1012) edges each representing a web link 
and 100 billion (1011) nodes each representing distinct URLs. Creating and analyzing such a large graph requires a large number of
computers running for many days. In early 2005, the infrastructure for the WebMap, named Dreadnaught, needed to be redesigned to scale
up to more nodes. Dreadnaught had successfully scaled from 20 to 600 nodes, but required a complete redesign to scale out further.
Dreadnaught is similar to MapReduce in many ways, but provides more flexibility and less structure. In particular, each fragment in a
Dreadnaught job can send output to each of the fragments in the next stage of the job, but the sort was all done in library code. In
practice, most of the WebMap phases were pairs that corresponded to MapReduce. Therefore, the WebMap applications would not require 
extensive refactoring to fit into MapReduce. Eric Baldeschwieler (Eric14) created a small team and we started designing and prototyping 
a new framework written in C++ modeled after GFS and MapReduce to replace Dreadnaught. Although the immediate need was for a new 
framework for WebMap, it was clear that standardization of the batch platform across Yahoo! Search was critical and by making the 
framework general enough to support other users, we could better leverage investment in the new platform. At the same time, we were 
watching Hadoop, which was part of Nutch, and its progress. In January 2006, Yahoo! hired Doug Cutting, and a month later we decided to 
abandon our prototype and adopt Hadoop. The advantage of Hadoop over our prototype and design was that it was already working with a 
real application (Nutch) on 20 nodes. That allowed us to bring up a research cluster two months later and start helping real customers 
use the new framework much sooner than we could have otherwise. Another advantage, of course, was that since Hadoop was already open 
source, it was easier (although far from easy!) to get permission from Yahoo!’s legal department to work in open source. So we set up a 
200-node cluster for the researchers in early 2006 and put the WebMap conversion plans on hold while we supported and improved Hadoop 
for the research users. 

