# Elastic's Google Summer of Code

[Elastic](https://www.elastic.co) is excited to participate in the Google Summer of Code 2018 program and we hope that you are too!

This readme will get you started with project ideas, mentors, where to ask questions, and how to apply.



## Application Instructions

Please read and apply via [https://summerofcode.withgoogle.com/get-started/](https://summerofcode.withgoogle.com/get-started/).

In your application tell us:

1. Who you are: Your name and how to contact you.
2. Which project idea you want to work on: Which of our ideas is it or describe in detail if it is your own.
3. How you will implement it: Provide a detailed work timeline that breaks the project into one week milestones and align it to the GSoC timeline.
4. Why you: Link to a pull request you have submitted to the project you want to work on. Here is a starting point for issues you could dive into:
  * [Elasticsearch `low hanging fruit`](https://github.com/elastic/elasticsearch/issues?q=is%3Aopen+is%3Aissue+label%3A%22low+hanging+fruit%22)
  * [Logstash `log hanging fruit`](https://github.com/elastic/logstash/issues?q=is%3Aopen+is%3Aissue+label%3A%22low+hanging+fruit%22)
  * [Kibana `low hanging fruit`](https://github.com/elastic/kibana/issues?q=is%3Aopen+is%3Aissue+label%3A%22low+hanging+fruit%22)
  * [Beats `good first issue`](https://github.com/elastic/beats/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22)

Elastic is always seeking to diversify its contributors and especially welcomes applications from women from all backgrounds and people of color.



## Mentors

* [Aravind Putrevu](https://github.com/aravindputrevu)
* [Igor Motov](https://github.com/imotov)
* [Jason Wong](https://github.com/logmonster)
* [Nicolas Ruflin](https://github.com/ruflin)
* [Nik Everett](https://github.com/nik9000)
* [Philipp Krenn](https://github.com/xeraa)
* [Steffen Siering](https://github.com/urso)
* More to follow



## Technologies Used

Depending on the project you want to work on you will need to use different technologies:

* Elasticsearch: Java, Gradle
* Logstash: JRuby, Java, Ruby
* Kibana: Node.js, AngularJS, React
* Beats: Go

While you do not need to be an expert, you need to be comfortable working with the technologies of your project. And you should not be a stranger to Git and GitHub.

You will need to show off your skills by linking to a pull request you have submitted to your project. The pull request does not need to be big or complex, but we want to be sure that you can hit the ground running and we won't be spending the first two weeks with tooling issues.

If you cannot find a suitable issue, get stuck on one, need help with your setup, or anything else where you are unsure how to proceed: We have created a [GSoC Discuss group](https://discuss.elastic.co/c/elastic-user-groups/elastic-gsoc) just for that and we will actively monitor any open questions there. [Discuss](https://discuss.elastic.co) is generally the best place for questions around all our open source projects, so we can get started with that workflow right away.



## Ideas

These are suggestions that we think would make good Google Summer of Code projects:

* TODO [Beats: Monitor your Java applications with JavaBeat](#beats_java)
* TODO [Beats: Integrate flows with protocol analyzers in Packetbeat](#beats_packet_protocol)
* TODO [Beats: More modules for Metricbeat](#beats_metric_modules)
* TODO [Beats: More modules for Filebeat](#beats_file_modules)
* TODO [Elasticsearch Clients: Update elasticsearch-lua](#elasticsearch_client_lua)
* TODO [Elasticsearch: Improve Painless's protection against long scripts](#elasticsearch_painless_limits)
* TODO [Elasticsearch: Make Painless's compiler easier to understand](#elasticsearch_painless_compiler)
* TODO [Elasticsearch: Speed up some highlighting](#elasticsearch_highlighting_order)

Please [open an issue](https://github.com/elastic/gsoc/issues) if you wish to discuss or propose your own idea — there are also some [pointers for other ideas](#other). We definitely value your initiative, so don't be shy.


### <a name="beats_java"></a>Beats: Monitor Your Java Applications with JavaBeat

#### Brief Explanation

While the Elastic Stack heavily relies on Java our monitoring capabilities in that area could use your help:

* Consume all metrics from verbose GC log.
* Collect thread counts and blocked threads.
* Track non heap memory allocations.
* Make it possible to compare sum of memory usages reported by the JVM versus what the operating system reports for the entire process.
* The Beat should handle JDK8 ad JDK9 for OpenJDK and Oracle JDK on Linux and Windows.

#### Expected Results

A working beat to extract the metrics on all supported JDKs for Linux and Windows. We have a lot of Java processes running and will use those to continuously test and improve your results. Improving the initial implementation is the explicit goal of this task.

Plus visualizations and a dashboard in Kibana.

#### Knowledge Prerequisites

* Go - medium
* Java internals - none required but you'll learn quite a bit by
  working on the problem and we'll happily teach you what we know
* Elasticsearch - none and we'll happily teach the little you'd need to learn

#### Skill Level

Medium

#### Mentor

Nicolas Ruflin



### <a name="beats_packet_protocol"></a>Beats: More Packetbeat Protocols

#### Brief Explanation

Packetbeat can be extended with additional protocols. Some of the most requested protocols can be found under [https://github.com/elastic/beats/issues?q=is%3Aopen+label%3APacketbeat+label%3Amodule](https://github.com/elastic/beats/issues?q=is%3Aopen+label%3APacketbeat+label%3Amodule). Please provide a list of the protocols you want to add and why you have selected them. Pick a sensible number of protocols and give a rough overview of the features you want to implement.

#### Expected Results

Modules for the selected applications, documentation, as well as visualizations and a dashboard in Kibana for each protocol.

#### Knowledge Prerequisites

* Go - medium
* Networking - medium
* Applications you will support - none required but you'll learn quite a bit by
  working on the problem and we'll happily teach you what we know
* Elasticsearch - none and we'll happily teach the little you'd need to learn

#### Skill Level

Medium

#### Mentors

Steffen Siering, Nicolas Ruflin



### <a name="beats_metric_modules"></a>Beats: More Modules for Metricbeat

#### Brief Explanation

Today Metricbeat supports around 30 modules like Apache HTTP, Couchbase, Docker, HAProxy, Kafka, Kubernetes, MongoDB, MySQL, nginx, PostgreSQL, Prometheus, Redis, and ZooKeeper. But we want more! Luckily it is fairly easy to add new modules to Metricbeat. The developer guide can be found at [https://www.elastic.co/guide/en/beats/devguide/current/creating-metricbeat-module.html](https://www.elastic.co/guide/en/beats/devguide/current/creating-metricbeat-module.html).

Here is a list of services we are still missing the most:

* Cassandra
* Consul
* CouchDB
* Jenkins
* Mesos
* Varnish

Your application must include, which module or modules you want to add, why you think they should be included, and which metrics you intend to collect.

#### Expected Results

Modules for the selected applications, documentation, as well as visualizations and a dashboard in Kibana for each application.

#### Knowledge Prerequisites

* Go - medium
* Applications you will support - at least a basic understanding so that you know what makes sense to monitor and how do display that information
* Elasticsearch - none and we'll happily teach the little you'd need to learn

#### Skill Level

Medium

#### Mentors

Nicolas Ruflin, Philipp Krenn



### <a name="beats_file_modules"></a>Beats: More Modules for Filebeat

#### Brief explanation

Filebeat modules are vital to provide a good out of the box experience. At the moment we support just over 10 modules like Apache HTTP, MySQL, nginx, and system logs. Good candidates for inclusion are the applications we already support in Metricbeat or the ones we would like to add in [Beats: More modules for Metricbeat](#beats_metric_modules).

Your application must include, which module or modules you want to add, why you think they should be included, and which information you intend to collect.

#### Expected Results

Modules for the selected applications, documentation, as well as visualizations and a dashboard in Kibana for each application.

#### Knowledge Prerequisites

* Go - medium
* Applications you will support - at least a basic understanding so that you know what makes sense to collect and how do display that information
* Elasticsearch - none and we'll happily teach the little you'd need to learn

#### Skill Level

Medium

#### Mentors

Nicolas Ruflin, Philipp Krenn



### <a name="elasticsearch_client_lua"></a>Update elasticsearch-lua

#### Brief Explanation

Currently, elasticsearch-lua is built on top of Elasticsearch 2.x but does not implement all possible Elasticsearch features. Moreover, Elasticsearch is already at version 6.1 and many new features are available.

This project aims to implement the missing features from 2.x and also add the new features from Elasticsearch 5.x and 6.x.

#### Expected Results

An updated Lua client to access the Elasticsearch REST API compatible with the latest version (currently 6.1).

#### Knowledge Prerequisites

* Lua - medium
* JSON - medium
* HTTP - medium
* Elasticsearch - medium

#### Skill Level

Medium

#### Mentor

Jason Wong



### <a name="elasticsearch_painless_limits"></a>Elasticsearch: Improve Painless's Protection Against Long Scripts

#### Brief Explanation

Elasticsearch contains Painless, a purpose built embedded language designed to
protect the process from malicious or mistaken scripts that run forever in an
attempt to starve server resources. This protection does a decent job right
now but there are places where it is too permissive. We'd love for someone to
investigate the problem in more depth then we have.

#### Expected Results

Both:
* Either
  * An improved defense mechanism merged into Painless.
  * A detailed explanation of why the current defense mechanisms are good
    enough.
* An expanded suite of tests for this defense mechanism.

#### Knowledge Prerequisites

* Java - medium
* ASM and byte code generation - none required but you'll learn quite a bit by
  working on the problem and we'll happily teach you what we know
* Elasticsearch - none and we'll happily teach the little you'd need to learn

#### Skill Level

Medium

#### Mentors

Nik Everett, Igor Motov



### <a name="elasticsearch_painless_compiler"></a>Elasticsearch: Make Painless's Compiler Easier to Understand

#### Brief Explanation

Elasticsearch contains Painless, a purpose built embedded language. The compiler
is run in four phases (Parse, Walk, Analyze, Code Generation) but has two
internal representations. The second representation is generated in the Walk
phase, modified in the Analyze phase and then generates code in the
Code Generation phase. The modification during the Analyze phase troubles us
because the bulk of the work when adding new features or debugging issues occurs
during this phase and the mutability makes the debugging more difficult. We
hypothesize that adding a second internal representation that is built during
the analyze phase would make the compiler easier to understand.

#### Expected Results

* Code that adds an internal representation between the Analyze and Code
  Generation phases or some other better solution we haven't thought of at
  this time.
* Bonus points for any new language features or improved error reporting that
  become "easy" as a side effect of this change.

#### Knowledge Prerequisites

* Java - medium
* ASM and byte code generation - none required but you'd learn some in the
  process
* Elasticsearch - none and we'll happily teach the little you'd need to learn

#### Skill Level

Medium

#### Mentors

Nik Everett, Igor Motov



### <a name="elasticsearch_highlighting_order"></a>Elasticsearch: Speed Up Some Highlighting

#### Brief Explanation

One of the things Elasticsearch can do is to "highlight" a snippet from a
matching document. Currently documents are highlighted one after another during
the highlighting phase. The trouble with this is that some of the
implementations of highlighting are more efficient if they highlight in a
different order.

#### Expected Results

* Change to Elasticsearch to allow sending all documents to highlight to the
  highlighters at a time.
* Change to built in highlighters to support this and make intelligent
  decisions about the order. There are four builtin highlighters, two of which
  will likely see significant benefit from this change.
* Benchmarking to show the performance improvements this brings.

#### Knowledge Prerequisites

* Java - medium
* Lucene - none and you'll get a good introduction to the project by working on
  this project
* Elasticsearch - none and we'll happily teach the little you'd need to learn

#### Skill Level

Medium

#### Mentors

Nik Everett, Igor Motov



### <a name="other"></a>Other Ideas

You may get some inspiration from our issues:

* [Elasticsearch `high hanging fruit`](https://github.com/elastic/elasticsearch/issues?q=is%3Aopen+is%3Aissue+label%3A%22high+hanging+fruit%22).
* [Logstash `high hanging fruit`](https://github.com/elastic/logstash/issues?q=is%3Aopen+is%3Aissue+label%3A%22high+hanging+fruit%22)
* [Kibana `high hanging fruit`](https://github.com/elastic/kibana/issues?q=is%3Aopen+is%3Aissue+label%3A%22high+hanging+fruit%22)
* [Beats](https://github.com/elastic/beats/issues)

Please discuss any of these in an [issue](https://github.com/elastic/gsoc/issues) with us before submitting to maximize your chances of being accepted.



## I Need Help

If you want to discuss a specific project idea, use the [issues](https://github.com/elastic/gsoc/issues).

For all other questions like the application process, your pull request,... head over to [Discuss](https://discuss.elastic.co/c/elastic-user-groups/elastic-gsoc).
