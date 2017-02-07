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
* Jason Wong
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


### Beats: Monitor your Java applications with JavaBeat

While the Elastic Stack heavily relies on Java our monitoring capabilities in that area could use your help:

* Consume all metrics from verbose GC log.
* Collect thread counts and blocked threads.
* Track non heap memory allocations.
* Make it possible to compare sum of memory usages reported by the JVM versus what the operating system reports for the entire process.
* The Beat should handle JDK8 ad JDK9 for OpenJDK and Oracle JDK on Linux and Windows.


### Beats: Integrate flows with protocol analyzers in Packetbeat

todo


### Beats: Reimplement Packetbeat sniffers

Today the sniffers are not based on a go-packet.

todo


### Beats: More modules for Metricbeat

Today Metricbeat supports Apache HTTP, Couchbase, Docker, HAProxy, Kafka, MongoDB, MySQL, nginx, PostgreSQL, Prometheus, Redis, and ZooKeeper. But we want more!

Your application must include, which module or modules you want to add, why you think they should be included, and which metrics you intend to collect.


### Other Ideas

You may also get inspiration from our issues:

* [Elasticsearch `high hanging fruit`](https://github.com/elastic/elasticsearch/issues?q=is%3Aopen+is%3Aissue+label%3A%22high+hanging+fruit%22).
* [Logstash `high hanging fruit`](https://github.com/elastic/logstash/issues?q=is%3Aopen+is%3Aissue+label%3A%22high+hanging+fruit%22)
* [Kibana `high fruit`](https://github.com/elastic/kibana/issues?q=is%3Aopen+is%3Aissue+label%3A%22high+fruit%22)
* [Beats](https://github.com/elastic/beats/issues)

Please discuss any of these with us before submitting to maximize your changes of being accepted.
