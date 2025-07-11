# Home Assistant Add-on: Grafana with VictoriaMetrics datasource

[![GitHub Release][releases-shield]][releases]
![Project Stage][project-stage-shield]
[![License][license-shield]](LICENSE.md)

![Supports aarch64 Architecture][aarch64-shield]
![Supports amd64 Architecture][amd64-shield]
![Supports armhf Architecture][armhf-shield]
![Supports armv7 Architecture][armv7-shield]
![Supports i386 Architecture][i386-shield]

[![Github Actions][github-actions-shield]][github-actions]
![Project Maintenance][maintenance-shield]
[![GitHub Activity][commits-shield]][commits]

The open platform for beautiful analytics and monitoring with VictoriaMetrics datasource support.

![Grafana in the Home Assistant Frontend](images/screenshot.png)

## About

**This is a fork of the original [Home Assistant Community Add-ons Grafana repository](https://github.com/hassio-addons/addon-grafana) with added VictoriaMetrics datasource plugin support.**

The analytics platform for all your metrics with enhanced VictoriaMetrics integration.

Grafana allows you to query, visualize, alert on and understand your metrics
no matter where they are stored. Create, explore, and share dashboards. Learn
about your Home Automation system using sexy and compelling graphs, and other
data visualizations.

This fork includes the VictoriaMetrics datasource plugin, providing native support for VictoriaMetrics as a data source in Grafana.

Combine this add-on with the InfluxDB add-on to get insanely powerful
insights to your home.

[:books: Read the full add-on documentation][docs]

## Fork Information

This repository is a fork maintained independently with the following additions:

- VictoriaMetrics datasource plugin integration

**Note**: Changes made in this fork are not intended to be merged back to the original repository.

## Acknowledgments

**Special thanks to the original authors and contributors of the [Home Assistant Community Add-ons Grafana repository](https://github.com/hassio-addons/addon-grafana).** This fork is based on their excellent work and wouldn't be possible without their contributions to the Home Assistant community.

## Support

Got questions?

You could [open an issue here][issue] GitHub.

## Contributing

This is an active open-source project. We are always open to people who want to
use the code or contribute to it.

Thank you for being involved! :heart_eyes:

## Authors & contributors

The original setup of this repository is by [Franck Nijhof][frenck].

For a full list of all authors and contributors,
check [the contributor's page][contributors].

## We have got some Home Assistant add-ons for you

Want some more functionality to your Home Assistant instance?

We have created multiple add-ons for Home Assistant. For a full list, check out
our [GitHub Repository][repository].

## License

MIT License

Copyright (c) 2018-2025 Franck Nijhof

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-no-red.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[commits-shield]: https://img.shields.io/github/commit-activity/y/ysm-hassio/addon-grafana.svg
[commits]: https://github.com/ysm-hassio/addon-grafana/commits/main
[contributors]: https://github.com/ysm-hassio/addon-grafana/graphs/contributors
[docs]: https://github.com/ysm-hassio/addon-grafana/blob/main/grafana/DOCS.md
[frenck]: https://github.com/frenck
[github-actions-shield]: https://github.com/ysm-hassio/addon-grafana/workflows/CI/badge.svg
[github-actions]: https://github.com/ysm-hassio/addon-grafana/actions
[i386-shield]: https://img.shields.io/badge/i386-no-red.svg
[issue]: https://github.com/ysm-hassio/addon-grafana/issues
[license-shield]: https://img.shields.io/github/license/ysm-hassio/addon-grafana.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2025.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-production%20ready-brightgreen.svg
[reddit]: https://reddit.com/r/homeassistant
[releases-shield]: https://img.shields.io/github/release/ysm-hassio/addon-grafana.svg
[releases]: https://github.com/ysm-hassio/addon-grafana/releases
[repository]: https://github.com/ysm-hassio/repository
