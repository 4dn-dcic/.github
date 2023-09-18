# Fourfront Metadata Database 

The [**Fourfront Metadata Database**](https://cgap.hms.harvard.edu),
or just "**Fourfront**", is an open-source platform developed 
at the [Park Lab](https://compbio.hms.harvard.edu/index) 
in Harvard's [Department of Biomedical Informatics (DBMI)](https://dbmi.hms.harvard.edu/)
as part of our service in the role of 
**[Data Coordination and Integration Center (DCIC)](https://data.4dnucleome.org/help/about/about-dcic)**
for the [4D Nucleome Network](https://www.4dnucleome.org/),
one of the **[NIH Common Fund](https://commonfund.nih.gov/programs)** programs.

The **4D Nucleome Network** aims to understand the principles behind the three-dimensional
organization of the nucleus in space and time (the 4th dimension), and the role nuclear
organization plays in gene expression and cellular function. 
The Network uses existing omics and imaging technologies, and develops new ones to generate data
and create resources to enable the study of the 4D Nucleome.

More information about the 4D Nucleome program can be obtained at:

* the [4DN portal](http://www.4dnucleome.org/) and
* the [NIH program website](https://commonfund.nih.gov/4Dnucleome/index),
  which also lists the [funded research centers](https://commonfund.nih.gov/4Dnucleome/FundedResearch).

Information about our implementation can be found at:

* our **GitHub repositories**, detailed below, and
* our **online documentation**, detailed below, but including particularly:

  * [Fourfront](https://fourfront.readthedocs.io) - metadata portal
  * [Submit4DN](https://github.com/4dn-dcic/Submit4DN/blob/master/README.md) - data submission tools

Please address all questions and comments to [support@4dnucleome.org](mailto:support@4dnucleome.org)

## Repositories

### Overview

Fourfront consists of multiple repositories which support a complex ecosystem of 
applications and tools that implement
**Fourfront** (the portal itself), 
**Tibanna** (the genomics pipeline),
**Foursight** (tools for monitoring and service actions), and
**Submit4DN** (a command line tool to aid in metadata and data file submission).

### History

Work on the Fourfront portal began in 2015 as a fork of earlier work on [ENCODE-DCC/encoded](https://github.com/ENCODE-DCC/encoded) and
[ENCODE-DCC/snovault](https://github.com/ENCODE-DCC/snovault),
developed by the [Stanford ENCODE team](https://cherrylab.stanford.edu/people/encode-staff)
The initial base and has been substantially developed and changed since then.
However, the two teams stay in periodic touch and share ideas since the
work is related.

In turn, our later work on the [CGAP Portal](https://github.com/dbmi-bgm/cgap-portal)
and [SMaHT Portal](https://github.com/smaht-dac/smaht-portal) build on this work.
Using a common codebase, especially based on our shared
[dcicutils](https://github.com/4dn-dcic/utils)
and [snovault](https://github.com/4dn-dcic/snovault) repositories,
we have refactored all three systems to no longer use AWS ElasticBeanstalk instances,
and instead to use a more modern architecture based on
Docker containers and AWS Fargate.

### Pipelines & Analysis

* **[tibanna](https://github.com/4dn-dcic/tibanna)** - Core software that runs pipelines on Amazon Web Services (AWS).
* [tibanna_ff](https://github.com/4dn-dcic/tibanna_ff) - An extension of Tibanna that works with the 4DN data portal.

### Portal Infrastructure

* **[fourfront](https://github.com/4dn-dcic/fourfront)** - The primary codebase of the Fourfront portal.
* [utils](https://github.com/4dn-dcic/utils) - A set of utility functions & scripts which are used in the Fourfront Portal and others.
* [snovault](https://github.com/4dn-dcic/snovault) - Contains abstractions for communicating with our databases, including PostgreSQL and ElasticSearch. A major dependency of CGAP Portal. Originally this was forked from ENCODE Project in ~2015.
* [react-workflow-viz](https://github.com/4dn-dcic/react-workflow-viz) - A React component/library for visualizing workflow runs.

### Monitoring

* **[foursight](https://github.com/4dn-dcic/foursight)** - Tools for monitoring and periodic service actions
* [foursight-core](https://github.com/4dn-dcic/foursight-core) - Core software supporting Foursight.

### Applications

* **[Submit4DN](https://github.com/4dn-dcic/Submit4DN)** - Command-line tools for submitting and uploading metadata and data files to Fourfront.

## Administrative

* [Governance](https://github.com/4dn-dcic/fourfront-governance) - Repository of governance, legal and policy information for our projects.
* [Legal Notices](https://data.4dnucleome.org/legal) - Legal notices for portal users.
