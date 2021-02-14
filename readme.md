# Elastic's Google Summer of Code

[Elastic](https://www.elastic.co) is excited to participate in the Google Summer of Code 2020 program and we hope that you are too!

This readme will get you started with project ideas, mentors, where to ask questions, and how to apply. Please note that this year we are only participating with the [Elastic UI repository](https://github.com/elastic/eui).



## What is the Elastic UI Framework and why are we excited about this project?

The Elastic UI framework (EUI) is at the :heart: of all interfaces at Elastic. It started as the design system for [Kibana](https://github.com/elastic/kibana) but has grown to be used by and shaped by teams across Elastic. Recently, EUI has been adopted by projects large and small outside of Elastic, and has welcomed contributions from designers and developers all over the world.

The teams that have adopted EUI move fast and are continuously releasing great features. What this means is that EUI is constantly improving and growing to support those teams. We often release updates weekly, and new features can have an immediate impact, leading to quick feedback cycles and new ideas. We take feature requests seriously and truly appreciate those that take time to help improve EUI.

We feel that the best way to keep improving EUI and supporting the growing number of teams adopting it is to

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
  Here is a starting point for issues you could dive into: [EUI `good first issue`](https://github.com/elastic/eui/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22)

If you want us to review your application before the final submission:

* Create a Google Doc.
* Add it as a draft in the [GSoC application](https://summerofcode.withgoogle.com) once you are ready for a review. Please, give it the permission `Can comment` for everybody with the link.

Elastic is always seeking to diversify its contributors and especially welcomes applications from women from all backgrounds and people of color.



## Team

* [Aravind Putrevu](https://github.com/aravindputrevu) admin
* [Philipp Krenn](https://github.com/xeraa) admin
* [Stephanie Nissen](https://github.com/Stephanie-Nissen) admin
* [Michail Yasonik](https://github.come/myasonik) mentor




## Ideas

These are suggestions that we think would make good Google Summer of Code projects.

Please start a question on our [GSoC Discuss group](https://discuss.elastic.co/c/elastic-community-ecosystem/elastic-gsoc) if you wish to propose your idea — there are also some [pointers for other ideas](#other). We value your initiative, so don't be shy.



### Project-1: Accessible combobox variants

#### Brief Explanation

EUI has several different variants of comboboxes (where a user types and options are presented) however each is build differently. We'd like to rebuild all of our existing patterns on top of the same base components to provide a unified and accessible experience.

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

### Other Ideas

You may get some inspiration from our [existing issues](https://github.com/elastic/eui/issues) but keep in mind that this year we are limiting our projects to having an accessibility focus.

Please discuss any project ideas on the [GSoC Discuss group](https://discuss.elastic.co/c/elastic-community-ecosystem/elastic-gsoc) with us before submitting to maximize your chances of being accepted.



## I Need Help

For all questions like the application process, your pull request,... head over to our [GSoC Discuss group](https://discuss.elastic.co/c/elastic-community-ecosystem/elastic-gsoc).
