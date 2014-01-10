# Parquet Proposal

## Abstract
Parquet is a columnar storage format for Hadoop.

## Proposal

We created Parquet to make the advantages of compressed, efficient columnar data representation available to any project in the Hadoop ecosystem, regardless of the choice of data processing framework, data model, or programming language.

## Background

Parquet is built from the ground up with complex nested data structures in mind, and uses the repetition/definition level approach to encoding such data structures, as popularized by [Google Dremel](https://blog.twitter.com/2013/dremel-made-simple-with-parquet). We believe this approach is superior to simple flattening of nested name spaces.

Parquet is built to support very efficient compression and encoding schemes. Parquet allows compression schemes to be specified on a per-column level, and is future-proofed to allow adding more encodings as they are invented and implemented. We separate the concepts of encoding and compression, allowing parquet consumers to implement operators that work directly on encoded data without paying decompression and decoding penalty when possible.

## Rationale

Parquet is built to be used by anyone. We believe that an efficient, well-implemented columnar storage substrate should be useful to all frameworks without the cost of extensive and difficult to set up dependencies.

Furthermore, the rapid growth of Parquet community is empowered by open source. We believe the Apache foundation is a great fit as the long-term home for Parquet, as it provides an established process for community-driven development and decision making by consensus. This is exactly the model we want for future Parquet development.

## Initial Goals

* Move the existing codebase to Apache
* Integrate with the Apache development process
* Ensure all dependencies are compliant with Apache License version 2.0
* Incremental development and releases per Apache guidelines

## Current Status

Parquet has undergone [2 major releases](https://github.com/Parquet/parquet-format/releases) of the core format and [22 releases](https://github.com/Parquet/parquet-mr/releases) of the supporting set of Java libraries. Parquet is being used in production by [many organizations](https://github.com/Parquet/parquet-mr/blob/master/PoweredBy.md). The Parquet source is currently hosted at github.com, which will seed the Apache git repository.

### Meritocracy

We plan to invest in supporting a meritocracy. We will discuss the requirements in an open forum. Several companies have already expressed interest in this project, and we intend to invite additional developers to participate. We will encourage and monitor community participation so that privileges can be extended to those that contribute.

### Community

There is a large need for an advanced columnar storage format for Hadoop. Parquet is currently being used by [several organizations](https://github.com/Parquet/parquet-mr/blob/master/PoweredBy.md). By bringing Parquet into Apache, we believe that the community will grow even bigger.

### Core Developers

Parquet was [initially developed](https://blog.twitter.com/2013/announcing-parquet-10-columnar-storage-for-hadoop) as a collaboration between Twitter, Cloudera and Criteo. 

### Alignment

We believe that having Parquet at Apache will help further the growth of the big-data community, as it will encourage cooperation within the greater ecosystem of projects spawned by Apache Hadoop. The alignment is also beneficial to other Apache communities (such as Hadoop, Hive, Avro).

## Known Risks

### Orphaned Products

The risk of the Parquet project being abandoned is minimal. There are many organizations using Parquet in production, including Twitter, Cloudera, Stripe, and [Salesforce](http://blog.cloudera.com/blog/2013/10/parquet-at-salesforce-com/). 

### Inexperience with Open Source

Parquet has existed as a healthy open source for one year. During that time, we have curated an open-source community successfully, attracting over [30 contributors](https://github.com/Parquet/parquet-mr/graphs/contributors) from a diverse group of companies.
Several of the core contributors to the project are deeply familiar with OSS and Apache specifically: Julien Le Dem is the current PMC Chair for Apache Pig, and Dmitriy Ryaboy, Aniket Mokashi, and Jonathan Coveney are also Apache Pig committers with contributions to several other Apache projects. Todd Lipcon and Tom White are committers to Apache Hadoop and multiple other related projects. Brock Noland is a Hive committer.

### Homogenous Developers

The initial committers come from a number of companies and countries. Parquet has an active community of developers, and we are committed to recruiting additional committers based on their contributions to the project. The java library component alone has contributions from 31 individual github accounts, 14 of which contributed over 1000 lines of code.

### Reliance on Salaried Developers

It is expected that Parquet development will occur on both salaried time and on volunteer time, after hours. The majority of initial committers are paid by their employers to contribute to this project. However, they are all passionate about the project, and we are confident that the project will continue even if no salaried developers contribute to the project. As evidence of this statement, we present the [GitHub "punchcard"](https://github.com/Parquet/parquet-mr/graphs/punch-card) showing that a lot of activity happens on weekends. We are committed to recruiting additional committers including non-salaried developers. 

### Relationships with Other Apache Products

As mentioned in the Alignment section, Parquet is closely related to Hadoop, Pig, Avro, Thrift, YARN and Mesos in a numerous ways. We look forward to collaborating with those communities, as well as other Apache communities (including Apache S4 which focuses on stateful low-latency processing).

### An Excessive Fascination with the Apache Brand

Parquet is an already healthy and well known open source project. This proposal is not for the purpose of generating publicity. Rather, the primary benefits to joining Apache are those outlined in the Rationale section.

## Documentation

Documentation is currently located as README markdown files:

* https://github.com/Parquet/parquet-format
* https://github.com/Parquet/parquet-mr

## Source and Intellectual Property Submission Plan

The Parquet codebase is currently hosted on Github: https://github.com/ParquetFormat. 

This is the exact codebase that we would migrate to the Apache foundation.

## External Dependencies

```
Project | License
Junit | EPL
Apache Commons | APL 2
Apache Thrift | APL 2
Apache Maven | APL 2
Apache Avro | APL 2
Apache Hadoop | APL 2
Google Guava | APL 2
```
More TODO



## Cryptography

We do not expect Parquet to be a controlled export item due to the use of encryption.

## Required Resources

### Mailing lists

parquet-dev
parquet-user

## Subversion Directory

Git is the preferred source control system: git://git.apache.org/parquet

## Issue Tracking

JIRA: Parquet (PARQUET)

## Initial Committers

* Aniket Mokashi
* Brock Noland
* Dmitriy Ryaboy <dmitriy@twitter.com>
* Julien Le Dem <julien@twitter.com>
* Marcel Kornacker 
* Mickael Lacour
* Nong Li 
* Tianshuo Deng
* Tom White
* Remy Pecqueur
* TODO

## Affiliations

* Aniket Mokashi - Twitter
* Brock Noland - Cloudera
* Julien Le Dem - Twitter
* Dmitriy Ryaboy - Twitter
* Marcel Kornacker - Cloudera
* Mickael Lacour - Criteo
* Nong Li - Cloudera
* Tianshuo Deng - Twitter
* Tom White - Cloudera
* Remy Pecqueur - Criteo
* TODO

## Sponsors

### Champion

TODO

### Nominated Mentors

TODO

### Sponsoring Entity

The Apache Incubator
