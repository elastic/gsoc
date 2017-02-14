# Elastic's Google Summer of Code

[Elastic](https://www.elastic.co) is excited to participate in the Google Summer of Code 2017 program and we hope that you are too!

This readme will get you started with project ideas, mentors, and how to apply. Feel free to open an issue to ask questions or discuss other ideas.


## Application Instructions

Please read and apply via [https://summerofcode.withgoogle.com/get-started/](https://summerofcode.withgoogle.com/get-started/).

In your application tell us:

1. Who you are: Your name and how to contact you.
2. Which project idea you want to work on: Which of our ideas is it or describe in detail if it is your own.
3. How will you implement it: Provide a detailed work timeline that breaks the project into one or two week milestones and align it to the GSoC timeline.
4. Why you: Link to a pull request you have submitted to the project (Elasticsearch, Logstash, Kibana, or Beats) you want to work on. Here is a starting point for issues you could dive into:
  * [Elasticsearch `low hanging fruit`](https://github.com/elastic/elasticsearch/issues?q=is%3Aopen+is%3Aissue+label%3A%22low+hanging+fruit%22)
  * [Logstash `log hanging fruit`](https://github.com/elastic/logstash/issues?q=is%3Aopen+is%3Aissue+label%3A%22low+hanging+fruit%22)
  * [Kibana `low fruit`](https://github.com/elastic/kibana/issues?q=is%3Aopen+is%3Aissue+label%3A%22low+fruit%22)
  * [Beats](https://github.com/elastic/beats/issues)

Elastic is always seeking to diversify its contributors and especially welcomes applications from women from all backgrounds and people of color.


## Mentors

* [Igor Motov](https://github.com/imotov)
* [Jason Wong](https://github.com/logmonster)
* [Konrad Beiske](https://github.com/beiske)
* [Nicolas Ruflin](https://github.com/ruflin)
* [Nik Everett](https://github.com/nik9000)
* [Pablo Musa](https://github.com/pmusa)
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

You will need to show off your skills by linking to a pull request you have submitted to your project. The pull request does not need to be huge or complex, but we want to be sure that you can contribute fully.


## Ideas

These are suggestions that we think would make good Google Summer of Code projects. Feel free to open an issue if you wish to discuss or propose your own idea.

* [Beats: Monitor your Java applications with JavaBeat](#beats_java)
* [Beats: Integrate flows with protocol analyzers in Packetbeat](#beats_packet_protocol)
* [Beats: Reimplement Packetbeat sniffers](#beats_packet_sniffers)
* [Beats: More modules for Metricbeat](#beats_metric_modules)
* [Elasticsearch Clients: Update elasticsearch-lua](#esclients_update_eslua)
* [Elasticsearch: Improve Painless's protection against long scripts](#painless_improve_time_limits)
* [Elasticsearch: Make Painless's compiler easier to understand](#painless_improve_guts)
* [Elasticsearch: Speed up some highlighting](#highlighting_order)

##

### <a name="beats_java"></a>Beats: Monitor your Java applications with JavaBeat

While the Elastic Stack heavily relies on Java our monitoring capabilities in that area could use your help:

* Consume all metrics from verbose GC log.
* Collect thread counts and blocked threads.
* Track non heap memory allocations.
* Make it possible to compare sum of memory usages reported by the JVM versus what the operating system reports for the entire process.
* The Beat should handle JDK8 ad JDK9 for OpenJDK and Oracle JDK on Linux and Windows.

##

### <a name="beats_packet_protocol"></a>Beats: Integrate flows with protocol analyzers in Packetbeat

todo

##

### <a name="beats_packet_sniffers"></a>Beats: Reimplement Packetbeat sniffers

Today the sniffers are not based on a go-packet.

todo

##

### <a name="beats_metric_modules"></a>Beats: More modules for Metricbeat

Today Metricbeat supports Apache HTTP, Couchbase, Docker, HAProxy, Kafka, MongoDB, MySQL, nginx, PostgreSQL, Prometheus, Redis, and ZooKeeper. But we want more!

Your application must include, which module or modules you want to add, why you think they should be included, and which metrics you intend to collect.

##

### <a name="esclients_update_eslua"></a>Update elasticsearch-lua

#### Brief explanation

Currently, elasticsearch-lua is built on top of Elasticsearch 2.x but does not implement all possible Elasticsearch features. Moreover, Elasticsearch is already in version 5.2 and many new features are available.

This project aims to implement the missing features from 2.x and also add the new features from Elasticsearch 5.2.

#### Expected results

An updated Lua client to access the Elasticsearch REST API compatible with the latest version (currently 5.2).

#### Knowledge prerequisites

* Lua - medium
* JSON - medium
* HTTP - medium
* Elasticsearch - medium

#### Skill level

Medium

#### Mentor

Pablo Musa

##

### <a name="painless_improve_time_limits"></a>Improve the purpose built embedded language Painless's defense against long scripts

#### Brief explanation

Elasticsearch contains Painless, a purpose built embedded language designed to
protect the process from malicious or mistaken scripts that run forever in an
attempt to starve server resources. This protection is does a decent job right
now but there are places where it is too permissive. We'd love for someone to
investigate the problem in more depth then we have.

#### Expected results

Both:
* Either
  * An improved defense mechanism merged into Painless.
  * A detailed explanation of why the current defense mechanisms are good
    enough.
* An expanded suite of tests for this defense mechanism.

#### Knowledge prerequisites

* Java - medium
* ASM and byte code generation - none required but you'll learn quite a bit by
  working on the problem and we'll happily teach you what we know
* Elasticsearch - none and we'll happily teach the little you'd need to learn

#### Skill level

Medium

#### Mentor

Nik Everett

##

### <a name="painless_improve_guts"></a>Improve the purpose built embedded language Painless's compiler internals

#### Brief explanation

Elasticsearch contains Painless, a purpose built embedded language. The compiler
is run in four phases (Parse, Walk, Analyze, Code Generation) but has two
internal representations. The second representation is generated in the Walk
phase, modified in the Analyze phase and then generates code in the
Code Generation phase. The modification during the Analyze phase troubles us
because the bulk of the work when adding new features or debugging issues occurs
during this phase and the mutability makes the debugging more difficult. We
hypothesize that adding a second internal representation that is built during
the analyze phase would make the compiler easier to understand.

#### Expected results

* Code that adds an internal representation between the Analyze and Code
  Generation phases or some other better solution we haven't thought of at
  this time.
* Bonus points for any new language features or improved error reporting that
  become "easy" as a side effect of this change.

#### Knowledge prerequisites

* Java - medium
* ASM and byte code generation - none required but you'd learn some in the
  process
* Elasticsearch - none and we'll happily teach the little you'd need to learn

#### Skill level

Medium

#### Mentor

Nik Everett

##

### <a name="highlighting_order"></a>Fix highlighting apis to highlight more than 1 doc at once

#### Brief explanation

One of the things Elasticsearch can do to is "highlight" a snippet from a
matching document. Currently documents are highlighted one after another during
the highlighting phase. The trouble with this is that some of the
implementations of highlighting are more efficient if they highlight in a
different order.

#### Expected results

* Change to Elasticsearch to allow sending all documents to highlight to the
  highlighters at a time.
* Change to built in highlighters to support this and make intelligent
  decisions about the order. There are four builtin highlighters, two of which
  will likely see significant benefit from this change.
* Benchmarking to show the performance improvements this brings.

#### Knowledge prerequisites

* Java - medium
* Lucene - none and you'll get a good introduction to the project by working on
  this project
* Elasticsearch - none and we'll happily teach the little you'd need to learn

#### Skill level

Medium

#### Mentor

Nik Everett

##

### <a name="highlighting_order"></a>Fix highlighting apis to highlight more than 1 doc at once

#### Brief explanation

One of the things Elasticsearch can do to is "highlight" a snippet from a
matching document. Currently documents are highlighted one after another during
the highlighting phase. The trouble with this is that some of the
implementations of highlighting are more efficient if they highlight in a
different order.

#### Expected results

* Change to Elasticsearch to allow sending all documents to highlight to the
  highlighters at a time.
* Change to built in highlighters to support this and make intelligent
  decisions about the order. There are four builtin highlighters, two of which
  will likely see significant benefit from this change.
* Benchmarking to show the performance improvements this brings.

#### Knowledge prerequisites

* Java - medium
* Lucene - none and you'll get a good introduction to the project by working on
  this project
* Elasticsearch - none and we'll happily teach the little you'd need to learn

#### Skill level

Medium

#### Mentor

Nik Everett

##

### Other Ideas

You may also get inspiration from our issues:

* [Elasticsearch `high hanging fruit`](https://github.com/elastic/elasticsearch/issues?q=is%3Aopen+is%3Aissue+label%3A%22high+hanging+fruit%22).
* [Logstash `high hanging fruit`](https://github.com/elastic/logstash/issues?q=is%3Aopen+is%3Aissue+label%3A%22high+hanging+fruit%22)
* [Kibana `high fruit`](https://github.com/elastic/kibana/issues?q=is%3Aopen+is%3Aissue+label%3A%22high+fruit%22)
* [Beats](https://github.com/elastic/beats/issues)

Please discuss any of these with us before submitting to maximize your changes of being accepted.
