# Elastic's Google Summer of Code

[Elastic](https://www.elastic.co) is excited to participate in the Google Summer of Code 2019 program and we hope that you are too!

This readme will get you started with project ideas, mentors, where to ask questions, and how to apply.



## Application Instructions

Please read and apply via [https://summerofcode.withgoogle.com/get-started/](https://summerofcode.withgoogle.com/get-started/).

In your application please tell us about:

1. **You**: Your name and how to contact you.
1. **Project**: Which of our project ideas you want to be working on or if it is your own, describe it in detail.
1. **Deliverables**: What is the outcome of your project. The more technical details the better.
1. **Timeline**: Provide a detailed work timeline that breaks the project into one-week milestones and align them to the GSoC timeline.
1. **Availability**: Describe your time commitment and be very explicit about any other engagements — both related to work and holidays or trips. No surprises, please.
1. **Pull request**: Link to a pull request you have submitted to the project you want to work on. If you are applying to work on the Lua client, the pull request would make the most sense to be against the current Lua client and not Elasticsearch itself; the same applies for all other projects — we want to see you working on the codebase where you will be spending your time.
  It is not required to have the pull request merged since reviewing can take time and we do not rush that process. We want to see that you can contribute in a meaningful way to the project you want to be working on. Start small and only add more complex tasks later on. And while documentation fixes or enhancement are welcome, showing your programming skills will earn you bonus points.
  Here is a starting point for issues you could dive into:
  * [Elasticsearch `good first issue`](https://github.com/elastic/elasticsearch/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22+)
  * [Logstash `good first issue`](https://github.com/elastic/logstash/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22+)
  * [Kibana `good first issue`](https://github.com/elastic/kibana/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22+)
  * [Beats `good first issue`](https://github.com/elastic/beats/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22+)

If you want us to review your application before the final submission:

* Create a Google Doc and add it as a draft in the [GSoC application](https://summerofcode.withgoogle.com).
* Once you are ready for a review, share the document with the mentors listed for your project with the permission `Can comment` — see the screenshot below.

![](share.png)

Elastic is always seeking to diversify its contributors and especially welcomes applications from women from all backgrounds and people of color.



## Team

* [Aravind Putrevu](https://github.com/aravindputrevu) admin
* [Carlos Pérez-Aradros](https://github.com/exekias) mentor
* [Dhaval Kapil](https://github.com/DhavalKapil) mentor
* [Emanuil Tolev](https://github.com/emanuil-tolev) mentor
* [Igor Motov](https://github.com/imotov) mentor
* [Nicolas Ruflin](https://github.com/ruflin) mentor
* [Nik Everett](https://github.com/nik9000) mentor
* [Ning Chang](https://github.com/cforchangning) admin
* [Pablo Musa](https://github.com/pmusa) mentor
* [Philipp Krenn](https://github.com/xeraa) admin
* [Ry Biesemeyer](https://github.com/yaauie) mentor
* [Steffen Siering](https://github.com/urso) mentor



## Technologies Used

Depending on the project you want to work on you will need to use different technologies:

* Elasticsearch: Java, Gradle
* Logstash: JRuby, Java, Ruby
* Kibana: Node.js, AngularJS, React
* Beats: Go

While you do not need to be an expert, you need to be comfortable working with the technologies of your project. And you should not be a stranger to Git and GitHub.

You will need to show off your skills by linking to a pull request you have submitted to your project. The pull request does not need to be big or complex, but we want to be sure that you can hit the ground running and we won't be spending the first two weeks with tooling issues.

If you cannot find a suitable issue, get stuck on one, need help with your setup, or anything else where you are unsure how to proceed: We have created a [GSoC Discuss group](https://discuss.elastic.co/c/elastic-community-ecosystem/elastic-gsoc) just for that and we will actively monitor any open questions there. [Discuss](https://discuss.elastic.co) is generally the best place for questions around all our open source projects, so we can get started with that workflow right away.



## Ideas

These are suggestions that we think would make good Google Summer of Code projects:

* [Beats: Monitor your Java applications with JavaBeat](#beats_java)
* [Beats: Enhance Packetbeat Flows with Application Layer metrics](#beats_packet_flows)
* [Beats: More application layer protocols for Packetbeat](#beats_packet_protocol)
* [Beats: Pure go packet sniffer](#beats_go_packet_sniffer)
* [Beats: More modules for Metricbeat, Filebeat and Heartbeat](#beats_modules)
* [Elasticsearch Clients: Update elasticsearch-lua](#elasticsearch_client_lua)
* [Elasticsearch: Speed up some highlighting](#elasticsearch_highlighting_order)
* [Logstash: Java Plugin API](#logstash_java_plugin_api)

Please start a question on our [GSoC Discuss group](https://discuss.elastic.co/c/elastic-community-ecosystem/elastic-gsoc) if you wish to propose your own idea — there are also some [pointers for other ideas](#other). We definitely value your initiative, so don't be shy.



### <a name="beats_java"></a>Beats: Monitor Your Java Applications with JavaBeat

#### Brief Explanation

While the Elastic Stack heavily relies on Java our monitoring capabilities in that area could use your help:

* Consume all metrics from verbose GC log.
* Collect thread counts and blocked threads.
* Track non-heap memory allocations.
* Make it possible to compare the sum of memory usages reported by the JVM versus what the operating system reports for the entire process.
* The Beat should handle JDK8 and JDK11 for OpenJDK and Oracle JDK on Linux and Windows.

#### Expected Results

A working beat to extract the metrics on all supported JDKs for Linux and Windows. We have a lot of Java processes running and will use those to continuously test and improve your results. Improving the initial implementation is the explicit goal of this task.

Plus visualizations and a dashboard in Kibana.

#### Knowledge Prerequisites

* Go - medium
* Java internals - none required but you will learn quite a bit by
  working on the problem and we will happily teach you what we know
* Elasticsearch - none and we will happily teach the little you would need to learn

#### Skill Level

Medium

#### Mentor

Nicolas Ruflin, Carlos Pérez-Aradros



### <a name="beats_packet_flows"></a>Beats: Enhance Packetbeat Flows with Application Layer metrics

#### Brief Explanation

Packetbeat can parse and analyze application layer protocols, but also collect
flow metrics. As of today, flows and application layer support are two very
independent features in Packetbeat. As flows summarise the communication
between two endpoints, and protocol analyzers log only single transactions as events.
There exists a parent-child relationship between flows and transactions.
And Packetbeat should make use of this relationship, so to enhance a flows
lifetime and provide application-specific metrics, based on transport layer and
application layer protocol support, already available in Packetbeat.

See also the [Packetbeat enhancement request on flows](https://github.com/elastic/beats/issues/3444).

The Packetbeat documentations lists [all protocols](https://www.elastic.co/guide/en/beats/packetbeat/master/configuration-protocols.html#configuration-protocols) currently being available in Packetbeat.

#### Expected Results

* Integration of all protocol analyzers with flows, documentation, as well as updates to visualizations, and dashboards.
* Integration of transport layer protocols with flows, documentation, visualizations and dashboards.
* Enhance a flows lifetime to be aware of the transport layers connection state.

#### Knowledge Prerequisites

* Go - medium
* Networking - medium
* Applications you will support - none required but you will learn quite a bit by
  working on the problem and we will happily teach you what we know
* Elasticsearch - none and we will happily teach the little you would need to learn

#### Skill Level

Medium

#### Mentors

Steffen Siering, Nicolas Ruflin



### <a name="beats_packet_protocol"></a>Beats: More application layer protocols for Packetbeat

#### Brief Explanation

Packetbeat can be extended with additional protocols and there is a list with some of the [most requested protocols](https://github.com/elastic/beats/issues?q=is%3Aopen+label%3APacketbeat+label%3Amodule). Please provide a list of the protocols you want to add and why you have selected them. Pick a sensible number of protocols and give a rough overview of the features you want to implement.

#### Expected Results

Modules for the selected applications, documentation, as well as visualizations and a dashboard in Kibana for each protocol.

#### Knowledge Prerequisites

* Go - medium
* Networking - medium
* Applications you will support - none required but you will learn quite a bit by
  working on the problem and we will happily teach you what we know
* Elasticsearch - none and we will happily teach the little you would need to learn

#### Skill Level

Medium

#### Mentors

Steffen Siering, Nicolas Ruflin



### <a name="beats_modules"></a>Beats: More modules for Metricbeat, Filebeat and Heartbeat

Modules in Filebeat, Metricbeat, and Heartbeat are vital to providing a good out of the box experience. Today Metricbeat and Filebeat provide modules for around 30 services like Apache HTTP, Docker, Mysql, Nginx and more (See: [Filebeat module list](https://www.elastic.co/guide/en/beats/filebeat/master/filebeat-modules.html) and [Metricbeat module list](https://www.elastic.co/guide/en/beats/metricbeat/master/metricbeat-modules.html)). But we want more! We want to introduce more protocols and service types to Heartbeat. We want to add modules to Filebeat, that are available in Metricbeat only. And we want to add modules for new services to all Beats. Luckily it is fairly easy to add new Modules to Metricbeat and Filebeat. The [Beats Developer Guide](https://www.elastic.co/guide/en/beats/devguide/current/index.html) can be found in the Beats documentation.

Here is a list of services we are still missing the most:

* Cassandra
* Consul
* CouchDB
* Jenkins
* Mesos
* Varnish

Your application must include, which module or modules you want to add, why you think they should be included, and which metrics or logs you intend to collect.
The list of modules can contain modules already being available in Metricbeat, yet missing in Filebeat and Heartbeat.

#### Expected Results

- Introduce Services/Protocols to Heartbeat.
- Modules for the selected applications, documentation, as well as visualizations and a dashboard in Kibana for each application.

#### Knowledge Prerequisites

* Go - medium
* Applications you will support - at least a basic understanding so that you know what makes sense to collect and how do display that information
* Elasticsearch - none and we will happily teach the little you would need to learn

#### Skill Level

Medium

#### Mentors

Nicolas Ruflin, Carlos Pérez-Aradros, Steffen Siering



### <a name="beats_go_packet_sniffer"></a>Beats: Pure go packet sniffer

#### Brief Explanation

Packetbeat uses libpcap (via gopacket), to receive, filter and process packets
from network devices. Instead of relying on libpcap, it would be nice to have a
pure go based implementation, providing packet sniffing and filtering
capabilities for multiple platforms.

#### Expected Results

* Create go package, that provides a common packet sniffing and filtering API
* Support for Linux, MacOS, Windows (by integrating with WinPcap/WinPcap10/NPcap drivers)
* Support for multiple receive queues
* (Optional) Support for sniffers based on DPDK, netmap, and others
* Update Packetbeat

#### Knowledge Prerequisites

* Linux, Windows, MacOS/BSD networking - good
* Go - good

#### Skill Level

Advanced

#### Mentors

Steffen Siering, Nicolas Ruflin



### <a name="elasticsearch_client_lua"></a>Update elasticsearch-lua

#### Brief Explanation

Currently, [elasticsearch-lua](https://github.com/DhavalKapil/elasticsearch-lua) is built on top of Elasticsearch 2.x but does not implement all possible Elasticsearch features. Moreover, Elasticsearch is already at version 6.x and many new features are available.

This project aims to implement the missing features from 2.x and also add the new features from Elasticsearch 5.x and 6.x.

#### Expected Results

An updated Lua client to access the Elasticsearch REST API compatible with the latest version (currently 6.5).

#### Knowledge Prerequisites

* Lua - medium
* JSON - medium
* HTTP - medium
* Elasticsearch - medium

#### Skill Level

Medium

#### Mentor

Pablo Musa, Dhaval Kapil



### <a name="elasticsearch_highlighting_order"></a>Elasticsearch: Speed Up Some Highlighting

#### Brief Explanation

One of the things Elasticsearch can do is to "highlight" a snippet from a
matching document. Currently, documents are highlighted one after another during
the highlighting phase. The trouble with this is that some of the
implementations of highlighting are more efficient if they highlight in a
different order.

#### Expected Results

* Change to Elasticsearch to allow sending all documents to highlight to the
  highlighters at a time.
* Change to built-in highlighters to support this and make intelligent
  decisions about the order. There are four builtin highlighters, two of which
  will likely see significant benefit from this change.
* Benchmarking to show the performance improvements this brings.

#### Knowledge Prerequisites

* Java - medium
* Lucene - none and you will get a good introduction to the project by working on
  this project
* Elasticsearch - none and we will happily teach the little you would need to learn

#### Skill Level

Medium

#### Mentors

Nik Everett, Igor Motov



### <a name="logstash_java_plugin_api"></a>Logstash: Java Plugin API

#### Brief Explanation

Logstash began its life as a pure-ruby application, providing a ruby-based plugin API that enabled our users to extend Logstash functionality by providing their own configurable inputs, codecs, filters, and outputs with terse and expressive ruby code; in the years since, we have worked with our community to build and maintain [hundreds of plugins](https://github.com/logstash-plugins/) to handle an extremely diverse variety of data flows.

The application now runs in jruby on the JVM with a substantial portion of infrastructure written in pure Java, enabling type-safety and allowing us to leverage many concurrency tools available within the Java Standard Library and JVM ecosystem; we're in the process of defining a Java Plugin API, which will stand alongside the ruby-based plugin API to provide these same benefits for those who would prefer to develop their plugins in Java.

Since the best way to validate an API design is to use it extensively, this project will aim to port a number of existing, highly-used plugins to the new Java API; the lessons learned will apply the necessary pressure to help shape the Java Plugin API into a useful form.

#### Expected Results

 - Port several existing ruby-based Logstash plugins to use the proposed Java APIs in a variety of JVM languages,
 - Provide critical and constructive feedback about the use of the API,
 - File design bugs against the proposed Java API, and work with Logstash developers to improve it.

#### Knowledge Prerequisites

Participants should be familiar with Java, ideally open to exploring additional JVM languages like Kotlin.

#### Skill Level

Moderate

#### Mentors

Ry Biesemeyer, Jason Wong



### <a name="other"></a>Other Ideas

You may get some inspiration from our issues:

* [Elasticsearch `high hanging fruit`](https://github.com/elastic/elasticsearch/issues?q=is%3Aopen+is%3Aissue+label%3A%22high+hanging+fruit%22).
* [Logstash `high hanging fruit`](https://github.com/elastic/logstash/issues?q=is%3Aopen+is%3Aissue+label%3A%22high+hanging+fruit%22)
* [Kibana `high hanging fruit`](https://github.com/elastic/kibana/issues?q=is%3Aopen+is%3Aissue+label%3A%22high+hanging+fruit%22)
* [Beats](https://github.com/elastic/beats/issues)
* Any other open source project in the [Elastic organization on GitHub](https://github.com/elastic), for example [Ansible playbook for Elasticsearch](https://github.com/elastic/ansible-elasticsearch)

Please discuss any project ideas on the [GSoC Discuss group](https://discuss.elastic.co/c/elastic-community-ecosystem/elastic-gsoc) with us before submitting to maximize your chances of being accepted.



## I Need Help

For all questions like the application process, your pull request,... head over to our [GSoC Discuss group](https://discuss.elastic.co/c/elastic-community-ecosystem/elastic-gsoc).
