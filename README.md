# Predictive Match

<img src="https://d3i6fms1cm1j0i.cloudfront.net/github-wiki/images/snowplow-logo-large.png"
 alt="Snowplow logo" title="Snowplow" align="right" />

Predictive Match is an enterprise-strength predictive recommendation  analytics platform. It does three things:

1. Identifies your users, and tracks the way they engage with your website or application
2. Stores your users' behavioural data in a scalable "event data warehouse" you control
3. Lets you serve up real-tmie recommendations to your uses on your websites.

**To find out more, please check out the [PredictiveMatch website] [website] and the [PredictiveMatch wiki] [wiki].**

## Snowplow technology 101

The repository structure follows the conceptual architecture of Snowplow, which consists of five loosely coupled stages:

![architecture] [architecture-image]

To briefly explain these five sub-systems:

* **Trackers** fire Snowplow events. Currently we have a JavaScript tracker, a no-JavaScript (pixel) tracker and an Arduino tracker
* **Collectors** receive Snowplow events from trackers. Currently we have a CloudFront-based collector and a Clojure-based collector
* **Enrich** cleans up the raw Snowplow events, enriches them and puts them into storage. Currently we have a Hadoop-based enrichment processes
* **Storage** is where the Snowplow events live. Currently we store the Snowplow events in a flatfile structure on S3, and in the Redshift and Infobright columnar databases
* **Analytics** are performed on the Snowplow events. Currently we have a cookbook of ad hoc analyses that work with Hive, Redshift and Infobright 

**For more information on the current Snowplow architecture, please see the [Technical architecture] [architecture-doc]**.

## Find out more

| Technical Docs                  | Setup Guide               | Roadmap                 | Contributing                      |
|---------------------------------|---------------------------|-------------------------|-----------------------------------|
| ![i1] [techdocs-image]          | ![i2] [setup-image]       | ![i3] [roadmap-image]   | ![i4] [contributing-image]        |
| **[Technical Docs] [techdocs]** | **[Setup Guide] [setup]** | **[Roadmap] [roadmap]** | **[Contributing] [contributing]** |

## Contributing

We're committed to a loosely-coupled architecture for Snowplow and would love to get your contributions within each of the five sub-systems.

If you would like help implementing a new tracker, adding an additional enrichment or loading Snowplow events into an alternative database, check out our **[Contributing] [contributing]** page on the wiki!

## Questions or need help?

Check out the **[Talk to us] [talk-to-us]** page on our wiki.

## Copyright and license

Snowplow is copyright 2012-2013 Snowplow Analytics Ltd.

Licensed under the **[Apache License, Version 2.0] [license]** (the "License");
you may not use this software except in compliance with the License.

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

![Tracker](https://collector.snplow.com/i?&e=pv&page=Root%20README&aid=snowplowgithub&p=web&tv=no-js-0.1.0)

[website]: http://snowplowanalytics.com
[wiki]: https://github.com/snowplow/snowplow/wiki
[architecture-image]: https://d3i6fms1cm1j0i.cloudfront.net/github-wiki/images/technical-architecture.png
[architecture-doc]: https://github.com/snowplow/snowplow/wiki/Technical-architecture
[talk-to-us]: https://github.com/snowplow/snowplow/wiki/Talk-to-us
[contributing]: https://github.com/snowplow/snowplow/wiki/Contributing
[license]: http://www.apache.org/licenses/LICENSE-2.0
[setup]: https://github.com/snowplow/snowplow/wiki/Setting-up-SnowPlow
[tech-docs]: https://github.com/snowplow/snowplow/wiki/SnowPlow%20technical%20documentation
[tracker-protocol]: https://github.com/snowplow/snowplow/wiki/snowplow-tracker-protocol
[collector-logs]: https://github.com/snowplow/snowplow/wiki/Collector-logging-formats
[data-structure]: https://github.com/snowplow/snowplow/wiki/canonical-event-model

[techdocs-image]: https://d3i6fms1cm1j0i.cloudfront.net/github/images/techdocs.png
[setup-image]: https://d3i6fms1cm1j0i.cloudfront.net/github/images/setup.png
[roadmap-image]: https://d3i6fms1cm1j0i.cloudfront.net/github/images/roadmap.png
[contributing-image]: https://d3i6fms1cm1j0i.cloudfront.net/github/images/contributing.png

[techdocs]: https://github.com/snowplow/snowplow/wiki/SnowPlow-technical-documentation
[setup]: https://github.com/snowplow/snowplow/wiki/Setting-up-SnowPlow
[roadmap]: https://github.com/snowplow/snowplow/wiki/Product-roadmap
[contributing]: https://github.com/snowplow/snowplow/wiki/Contributing
