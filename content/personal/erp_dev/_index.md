---
title: ERP
prev: algo
next: personal
publishDate: 2023-08-21
weight: 2
---

The first ERP platform I developed for was [1C](https://1c.ru), back in 2004. At that time, version 7.5 was still in use. Many companies were transitioning to the new version 7.7. For a long time, it virtually dominated enterprises across all industries. Much later, a fundamentally new version 8.0 appeared. It developed slowly and painfully, and only by versions 8.2 and 8.3 did it begin to massively replace the older versions.

The standard version 7.7 struggled with large volumes of data and was poorly suited as a unified ERP system for large enterprises. As a result, customization at the time went far beyond typical limits. Enthusiasts essentially deconstructed the platform brick by brick and reassembled it, fixing key architectural issues:
- global locking of unified journal and constant tables was replaced with virtual locking;
- external modules were developed for parallel calculation of large data volumes for planning purposes;
- heavy calculation logic was often offloaded directly to MSSQL;
- solutions such as web portals even began to emerge around the platform;
- added RLS and much more.

{{< cards cols="1">}}
  {{< card link="https://infostart.ru/profile/22078/" title="Some of my apps for 7.7 platform can still be usefull. Visit infostart.ru" subtitle="" icon="globe-alt" >}}
{{< /cards >}}

After the era of 1C came the time of MS Dynamics Axapta and SAP S/4 HANA. These solutions were affordable only for the [largest enterprises](/enterprise) in the country. This was due not so much to their cost, but rather to the limited number of specialists capable of developing and maintaining solutions on these platforms.

