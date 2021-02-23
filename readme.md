# Elastic's Google Summer of Code

[Elastic](https://www.elastic.co) is excited to participate in the Google Summer of Code 2021 program and we hope that you are too!

This readme will get you started with project ideas, mentors, where to ask questions, and how to apply. Please note that this year we are only participating with the [Elastic UI](https://github.com/elastic/eui) and [Elastic Charts](https://github.com/elastic/elastic-charts) repositories.



## What are the Elastic UI and Charts Frameworks and why are we excited about this project?

The Elastic UI framework (EUI) is at the :heart: of all interfaces at Elastic. It started as the design system for [Kibana](https://github.com/elastic/kibana) but has grown to be used by and shaped by teams across Elastic. Recently, EUI has been adopted by projects large and small outside of Elastic, and has welcomed contributions from designers and developers all over the world. And Elastic Charts are following the same approach for creating advanced visualizations.

The teams that have adopted EUI and Charts move fast and are continuously releasing great features. What this means is that both projects are constantly improving and growing to support their users. We often release updates weekly, and new features can have an immediate impact, leading to quick feedback cycles and new ideas. We take feature requests seriously and truly appreciate those that take time to help improve EUI and Charts.

We feel that the best way to keep improving both projects and supporting the growing number of teams adopting it is to

1. stabilize our support for widely-used projects and platforms outside Elastic, and
2. continue to provide thorough, thoughtful, usable documentation.

In our attempt to solve a real need in the open source community, we want to be as helpful as possible in getting folks started the right way.



## Application Instructions

Please read and apply via [https://summerofcode.withgoogle.com/get-started/](https://summerofcode.withgoogle.com/get-started/).

In your application please tell us about:

1. **You**: Your name and how to contact you.
1. **Project**: Which of our project ideas you want to be working on or if it is your own, describe it in detail.
1. **Deliverables**: What is the outcome of your project. The more technical details are the better.
1. **Timeline**: Provide a detailed work timeline that breaks the project into one-week milestones and align them to the GSoC timeline.
1. **Availability**: Describe your time commitment and be very explicit about any other engagements — both related to work and holidays or trips. No surprises, please.
1. **Pull request**: Link to a pull request you have submitted to the project you want to work on.
  It is not required to have the pull request merged since reviewing can take time and we do not rush that process. We want to see that you can contribute in a meaningful way to the project you want to be working on. Start small and only add more complex tasks later on. And while documentation fixes or enhancement are welcome, showing your programming skills will earn you bonus points.
  Here is a starting point for issues you could dive into: [EUI `good first issue`](https://github.com/elastic/eui/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22) and [Elastic Charts `good first issue`](https://github.com/elastic/elastic-charts/issues?q=is:open+is:issue+label:%22good+first+issue%22)

If you want us to review your application before the final submission:

* Create a Google Doc.
* Add it as a draft in the [GSoC application](https://summerofcode.withgoogle.com) once you are ready for a review. Please, give it the permission `Can comment` for everybody with the link.

Elastic is always seeking to diversify its contributors and especially welcomes applications from women from all backgrounds and people of color.



## Team

* [Aravind Putrevu](https://github.com/aravindputrevu) admin
* [Jennifer Allen](https://github.com/jensallen) admin
* [Marco Vettorello](https://github.com/markov00) mentor
* [Michail Yasonik](https://github.come/myasonik) mentor
* [Philipp Krenn](https://github.com/xeraa) admin
* [Robert Monfera](https://github.com/monfera) mentor
* [Stephanie Nissen](https://github.com/Stephanie-Nissen) admin



## Ideas

These are suggestions that we think would make good Google Summer of Code projects.

Please start a question on our [GSoC Discuss group](https://discuss.elastic.co/c/elastic-community-ecosystem/elastic-gsoc) if you wish to propose your idea — there are also some [pointers for other ideas](#other). We value your initiative, so don't be shy.



### Project-1: Accessible Combobox Variants in EUI

#### Brief Explanation

[EUI](https://github.com/elastic/eui) has several different variants of comboboxes (where a user types and options are presented) however each is build differently. We'd like to rebuild all of our existing patterns on top of the same base components to provide a unified and accessible experience.

#### Expected Results

[EuiCombobox](https://eui.elastic.co/#/forms/combo-box), [multi-select Filter Groups](https://eui.elastic.co/#/forms/filter-group#multi-select), and [EuiSuggest](https://eui.elastic.co/#/forms/suggest) are all built on top of [EuiSelectable](https://eui.elastic.co/#/forms/selectable). A key point of this is to bring the accessibility of EuiSelectable to the other components.

#### Knowledge Prerequisites

* TypeScript
* React
* [Accessibility](https://eui.elastic.co/#/guidelines/accessibility) - none but be ready to learn about screen readers (VoiceOver or NVDA) and [WAI-ARIA Authoring Practices](https://www.w3.org/TR/wai-aria-practices-1.2/)

#### Skill Level

Medium-Hard

#### Mentors

Michail Yasonik



### Project-2: Alluvial Diagram in Elastic Charts

<img src="https://rawgraphs.io/static/alluvial_cover-5b6c32863e5a2afe77d0c41ea82504da.png" width="500px" />

Example: https://datavizcatalogue.com/methods/parallel_sets.html


#### Brief Explanation
Introduce the Alluvial diagram to [Elastic Charts](https://github.com/elastic/elastic-charts). These diagrams represent weighted flows among nodes, the links between nodes are proportional to the flow quantity.

#### Expected Results
A new Alluvial diagram type component that provides:
- a formalized but flexible data structure
- a set of interaction capabilities to explore the flow (tooltips, reordering nodes)
- a set of configuration options to tweak the visual aspect of the flow: space between nodes, initial sorting order, node, and link styles
- a set of usage examples and documentation

#### Knowledge Prerequisites
- SVG, Canvas2d or WebGL
- JavaScript (ideally TypeScript or ES2015)
- React, D3, or similar libraries
- Experience in dynamic content generation like data visualization, animation, or game development

#### Timeline (tentative)
- W1 familiarize with [Elastic Charts](https://github.com/elastic/elastic-charts) API and internals
- W2 familiarize with the alluvial diagram: gain a general understanding on when to use it and how to read it, what are the valuable interactions and evaluate good practices applied to that visualization.
- W3-W8 start from a barebone new chart type implementation provided by the mentor,  prototype and iterate on the data processing and data representation. Outcomes are an alpha version of an alluvial diagram component, with a flexible data structure, configuration options and, at least, tooltip interaction on elements/flows.
- W8-W10 clean up the code, provide good chart examples through Storybook with associated documentation

#### Skill Level
Medium

#### Mentors
Robert Monfera



### Project-3: Parallel Coordinates in Elastic Charts

<img src="https://datavizproject.com/wp-content/uploads/2015/11/Sk%C3%A6rmbillede-2016-02-01-kl.-18.31.24.png" width="500" />

Example: https://datavizcatalogue.com/methods/parallel_coordinates.html

#### Brief Explanation
Introduce the parallel coordinates chart in [Elastic Charts](https://github.com/elastic/elastic-charts). A parallel coordinates plot is a way to visualize high-dimensional multivariate datasets.
N-parallel lines are drawn to represent an n-dimensional space, and a data point is represented by the segments that connect the respective coordinate on each dimension space.

#### Expected Results
A new parallel coordinates component that provides:
- a formalized but flexible data structure
- a set of interaction capabilities to explore the data points (tooltips, data point highlights, dimension reordering via drag/drop, dimension filtering)
- a set of configuration options to tweak the visual aspect: polyline colors, dimensions labels)
- a set of usage examples and documentation

#### Timeline (tentative)
- W1 familiarize with [Elastic Charts](https://github.com/elastic/elastic-charts) API and internals
- W2 familiarize with the Parallel coordinates: gain a general understanding on when to use it and how to read it, what are the valuable interactions and evaluate good practices applied to that visualization.
- W3-W8 start from a barebone new chart type implementation provided by the mentor,  prototype and iterate on the data processing and data representation flow. Outcomes are an alpha version of a parallel coordinates component, with a flexible data structure, configuration options and, at least, highlight and tooltip interaction polylines.
- W8-W10 clean up the code, provide good chart examples through Storybook with associated documentation

#### Knowledge Prerequisites
- SVG, Canvas2d or WebGL
- JavaScript (ideally TypeScript or ES2015)
- React, D3, or similar libraries
- Experience in dynamic content generation like data visualization, animation, or game development

#### Skill Level
High

#### Mentors
Robert Monfera, TBD


### Project-4: Data Sonification

Inspirations:
* https://sonification.design
* https://www.ft.com/content/80269930-40c3-11e9-b896-fe36ec32aece

#### Brief Explanation
Sonification is the use of non-speech audio to convey information or perceptualize data. In the context of improving chart accessibility, we are looking to start adding simplified sonification using WebAudio to generate an audio track that represents slopes, twists, and trends in a cartesian chart.

#### Expected Results
Mapping functions that can transform a set of data points from a cartesian space into sounds, including sonic “tick marks” underlining the passage of time, text synthesis for values, and other embellishments.
That mapping functions should feed from the data source of a chart, as well as its axis and other data, to produce sounds that reflect the data and chart elements and, if possible, to represent annotations or relationships between data.

#### Knowledge Prerequisites
- Audio experience (any of composing, synthesizer tool or music-making, WebAudioAPI knowledge)
- JavaScript or Typescript

#### Timeline (tentative)
- W1 familiarize with [Elastic Charts](https://github.com/elastic/elastic-charts) API and internals
- W2 familiarize with data sonification: gain a general understanding of the various techniques used to map a datasource into synthesized sounds.
- W3-W4 create a prototype able to use the WebAudioAPI to produce sounds based on array of data points and annotations eg. axis ticks (not required to be linked with [Elastic Charts](https://github.com/elastic/elastic-charts) library at the beginning)
- W4-W6 iterate through the prototype refining the sound harmonics to improve and provide a pleasant experience.
- W7-W8 integrate that function into the chart library: an external action received by the chart library should trigger the sonification function for a cartesian chart rendered on screen.
- W9-W10 clean up the code, provide good chart examples through Storybook with associated documentation

#### Skill Level
Medium-High

#### Mentors
Robert Monfera, Michail Yasonik



### Other Ideas

You may get some inspiration from our [existing issues in EUI](https://github.com/elastic/eui/issues) but keep in mind that this year we are limiting our projects to having an accessibility focus. For [Elastic Charts issues](https://github.com/elastic/elastic-charts/issues) we are accepting a broader scope of features.

Please discuss any project ideas on the [GSoC Discuss group](https://discuss.elastic.co/c/elastic-community-ecosystem/elastic-gsoc) with us before submitting to maximize your chances of being accepted.



## I Need Help

For all questions like the application process, your pull request,... head over to our [GSoC Discuss group](https://discuss.elastic.co/c/elastic-community-ecosystem/elastic-gsoc).
