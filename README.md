# Predictive Match

Predictive Match is an enterprise-strength predictive recommendation  analytics platform. It does three things:

1. Identifies your users, and tracks the way they engage with your website or application
2. Stores your users' behavioural data in a scalable "event data warehouse" you control
3. Lets you serve up real-tmie recommendations to your uses on your websites.

**To find out more, please check out the [PredictiveMatch website] [website] and the [PredictiveMatch wiki] [wiki].**

## Predictive Match technology 101

The repository structure follows the conceptual architecture of Predictive Match, which consists of five loosely coupled stages:

![architecture] [architecture-image]

To briefly explain these five sub-systems:

* **Trackers** fire Snowplow events. Currently we have a JavaScript tracker, a no-JavaScript (pixel) tracker and an Arduino tracker
* **Collectors** receive Predictive Match events from trackers. Currently we have a CloudFront-based collector and a Clojure-based collector
* **Enrich** cleans up the raw Predictive Match events, enriches them and puts them into storage. Currently we have a Hadoop-based enrichment processes
* **Storage** is where the Predictive Match events live. Currently we store the Predictive Match events in a real-time data store
* **Analytics** are performed on the Predictive Match events

**For more information on the current Predictive Match architecture, please see the [Technical architecture] [architecture-doc]**.

## Find out more

| Technical Docs                  | Setup Guide               | Roadmap                 | Contributing                      |
|---------------------------------|---------------------------|-------------------------|-----------------------------------|
| ![i1] [techdocs-image]          | ![i2] [setup-image]       | ![i3] [roadmap-image]   | ![i4] [contributing-image]        |
| **[Technical Docs] [techdocs]** | **[Setup Guide] [setup]** | **[Roadmap] [roadmap]** | **[Contributing] [contributing]** |

## Questions or need help?

Check out the **[Talk to us] [talk-to-us]** page on our wiki.

## Copyright and license

Predictive Match is copyright 2012-2013 Search Media Pty. Ltd.

Licensed under the **[Apache License, Version 2.0] [license]** (the "License");
you may not use this software except in compliance with the License.

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

[website]: http://predictivematch.com
[wiki]: https://github.com/predictivematch/predictivematch/wiki
[architecture-image]: https://d3i6fms1cm1j0i.cloudfront.net/github-wiki/images/technical-architecture.png
[architecture-doc]: https://github.com/predictivematch/predictivematch/wiki/Technical-architecture
[talk-to-us]: https://github.com/predictivematch/predictivematch/wiki/Talk-to-us
[contributing]: https://github.com/predictivematch/predictivematch/wiki/Contributing
[license]: http://www.apache.org/licenses/LICENSE-2.0
[setup]: https://github.com/predictivematch/predictivematch/wiki/Setting-up-PredictiveMatch
[tech-docs]: https://github.com/predictivematch/predictivematch/wiki/PredictiveMatch%20technical%20documentation
[tracker-protocol]: https://github.com/predictivematch/predictivematch/wiki/predictivematch-tracker-protocol
[collector-logs]: https://github.com/predictivematch/predictivematch/wiki/Collector-logging-formats
[data-structure]: https://github.com/predictivematch/predictivematch/wiki/canonical-event-model

[techdocs-image]: https://d3i6fms1cm1j0i.cloudfront.net/github/images/techdocs.png
[setup-image]: https://d3i6fms1cm1j0i.cloudfront.net/github/images/setup.png
[roadmap-image]: https://d3i6fms1cm1j0i.cloudfront.net/github/images/roadmap.png
[contributing-image]: https://d3i6fms1cm1j0i.cloudfront.net/github/images/contributing.png

[techdocs]: https://github.com/predictivematch/predictivematch/wiki/PredictiveMatch-technical-documentation
[setup]: https://github.com/predictivematch/predictivematch/wiki/Setting-up-PredictiveMatch
[roadmap]: https://github.com/predictivematch/predictivematch/wiki/Product-roadmap
[contributing]: https://github.com/predictivematch/predictivematch/wiki/Contributing
