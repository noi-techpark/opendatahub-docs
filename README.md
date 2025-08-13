<!--
SPDX-FileCopyrightText: NOI Techpark <digital@noi.bz.it>

SPDX-License-Identifier: CC0-1.0
-->
[![REUSE Compliance](https://github.com/noi-techpark/opendatahub-docs/actions/workflows/reuse.yml/badge.svg)](https://github.com/noi-techpark/opendatahub-docs/wiki/REUSE#badges)

Open Data Hub Documentation
=============================

This repository contains documentation about the Open Data Hub
project.

The documentation consists of two complimentary parts:

1. The 'stable' documentation, that does not change much over time,
   available at https://docs.opendatahub.com/en/latest/.  This
   documentation can be accessed by anyone to have an overview of the
   Open Data Hub and to discover if the project can interest them or
   if they can join or interact with the Team. In more details, this
   part contains:

   * An introduction about the project and its architecture, purpose,
     and the data available
   * A list of possibilities to collaborate with the Open Data Hub
     Team
   * Description of all the datasets included in the Open Data Hub
   * How-tos for interacting with the data and the available datasets  
   * More detailed technical insights on the project
   * Various additional information
  
2. A wiki, containing more 'volatile' information, that may change
   over time and is intended for DevOps and developers to quickly find
   'ready-to-use' information, like for example more detailed
   information about datasets, data records, API, FAQ, and
   troubleshooting.

   The wiki is included in this repository and can be freely accessed
   by anyone at https://github.com/noi-techpark/odh-docs/wiki/

*****

**Note:** If you experience any issue when using the APIs (like e.g.,
endpoints down or throwing errors, query outcome not meeting the
expected result), please send an email directly to
help@opendatahub.com. Your feedback or request will be processed
directly by the Customer Care Team and you will likely receive a quick
response!

### REUSE

This project is [REUSE](https://reuse.software) compliant, more information about the usage of REUSE in NOI Techpark repositories can be found [here](https://github.com/noi-techpark/odh-docs/wiki/Guidelines-for-developers-and-licenses#guidelines-for-contributors-and-new-developers).

Since the CI for this project checks for REUSE compliance you might find it useful to use a pre-commit hook checking for REUSE compliance locally. The [pre-commit-config](.pre-commit-config.yaml) file in the repository root is already configured to check for REUSE compliance with help of the [pre-commit](https://pre-commit.com) tool.

Install the tool by running:
```bash
pip install pre-commit
```
Then install the pre-commit hook via the config file by running:
```bash
pre-commit install
```
