<!--lint ignore awesome-github-->

# Awesome Web Archiving [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) with stars

Web archiving is the process of collecting portions of the World Wide Web to ensure the information is preserved in an archive for future researchers, historians, and the public. Web archivists typically employ Web crawlers for automated capture due to the massive scale of the Web. Ever-evolving Web standards require continuous evolution of archiving tools to keep up with the changes in Web technologies to ensure reliable and meaningful capture and replay of archived web pages.

## Contents

* [Training/Documentation](#trainingdocumentation)
* [Resources for Web Publishers](#resources-for-web-publishers)
* [Tools & Software](#tools--software)
  * [Acquisition](#acquisition)
  * [Replay](#replay)
  * [Search & Discovery](#search--discovery)
  * [Utilities](#utilities)
  * [WARC I/O Libraries](#warc-io-libraries)
  * [Analysis](#analysis)
  * [Quality Assurance](#quality-assurance)
  * [Curation](#curation)
* [Community Resources](#community-resources)
  * [Other Awesome Lists](#other-awesome-lists)
  * [Blogs and Scholarship](#blogs-and-scholarship)
  * [Mailing Lists](#mailing-lists)
  * [Slack](#slack)
  * [Discord](#discord)
  * [Twitter](#twitter)
* [Web Archiving Service Providers](#web-archiving-service-providers)
  * [Self-hostable, Open Source](#self-hostable-open-source)
  * [Hosted, Closed Source](#hosted-closed-source)
* [Public Data](#public-data)

## Training/Documentation

* Introductions to web archiving concepts:
  * [What is a web archive?](https://youtu.be/ubDHY-ynWi0) - A video from [the UK Web Archive YouTube Channel](https://www.youtube.com/channel/UCJukhTSw8VRj-VNTpBcqWkw)
  * [Wikipedia's List of Web Archiving Initiatives](https://en.wikipedia.org/wiki/List_of_Web_archiving_initiatives)
  * [Glossary of Archive-It and Web Archiving Terms](https://support.archive-it.org/hc/en-us/articles/208111686-Glossary-of-Archive-It-and-Web-Archiving-Terms)
  * [The Web Archiving Lifecycle Model](https://archive-it.org/blog/post/announcing-the-web-archiving-life-cycle-model/) - The Web Archiving Lifecycle Model is an attempt to incorporate the technological and programmatic arms of the web archiving into a framework that will be relevant to any organization seeking to archive content from the web. Archive-It, the web archiving service from the Internet Archive, developed the model based on its work with memory institutions around the world.
  * [Retrieving and Archiving Information from Websites by Wael Eskandar and Brad Murray](https://kit.exposingtheinvisible.org/en/web-archive.html/)
* Training materials:
  * [A Whirlwind Tour of Common Crawl's Datasets using Python](https://github.com/commoncrawl/whirlwind-python/) ⭐ 37 | 🐛 1 | 🌐 Python | 📅 2026-04-01
  * [UNT Web Archiving Course](https://github.com/vphill/web-archiving-course) ⭐ 23 | 🐛 10 | 📅 2024-03-04
  * [IIPC and DPC Training materials: module for beginners (8 sessions)](https://netpreserve.org/web-archiving/training-materials/)
  * [Continuing Education to Advance Web Archiving (CEDWARC)](https://cedwarc.github.io/)
* The WARC Standard:
  * The [warc-specifications](https://iipc.github.io/warc-specifications/) community HTML version of the official specification and hub for new proposals.
  * The [offical ISO 28500 WARC specification homepage](http://bibnum.bnf.fr/WARC/).
* For researchers using web archives:
  * [GLAM Workbench: Web Archives](https://glam-workbench.github.io/web-archives/) - See also [this related blog post on 'Asking questions with web archives'](https://netpreserveblog.wordpress.com/2020/05/28/asking-questions-with-web-archives/).
  * [Archives Unleashed Toolkit documentation](https://aut.docs.archivesunleashed.org/)
  * [Tutorial for Humanities researchers about how to explore Arquivo.pt](https://sobre.arquivo.pt/en/tutorial-for-humanities-researchers-about-how-to-use-arquivo-pt/)

## Resources for Web Publishers

These resources can help when working with individuals or organisations who publish on the web, and who want to make sure their site can be archived.

* [Definition of Web Archivability](https://nullhandle.org/web-archivability/index.html) - This describes the ease with which web content can be preserved. ([Archived version from the Stanford Libraries](https://web.archive.org/web/20230728211501/https://library.stanford.edu/projects/web-archiving/archivability))
* The [Archive Ready](http://archiveready.com/) tool, for estimating how likely a web page will be archived successfully.

## Tools & Software

This list of tools and software is intended to briefly describe some of the most important and widely-used tools related to web archiving. For more details, we recommend you refer to (and contribute to!) these excellent resources from other groups:

* [Awesome Website Change Monitoring](https://github.com/edgi-govdata-archiving/awesome-website-change-monitoring) ⭐ 513 | 🐛 3 | 📅 2025-10-17
* [Comparison of web archiving software](https://github.com/archivers-space/research/tree/master/web_archiving) ⭐ 99 | 🐛 8 | 📅 2018-09-27

### Acquisition

* [ArchiveBox](https://github.com/ArchiveBox/ArchiveBox) ⭐ 27,175 | 🐛 200 | 🌐 Python | 📅 2026-04-05 - A tool which maintains an additive archive from RSS feeds, bookmarks, and links using wget, Chrome headless, and other methods (formerly `Bookmark Archiver`). *(In Development)*
* [SingleFile](https://github.com/gildas-lormeau/SingleFile) ⭐ 20,840 | 🐛 127 | 🌐 JavaScript | 📅 2026-02-24 - Browser extension for Firefox/Chrome and CLI tool to save a faithful copy of a complete page as a single HTML file. *(Stable)*
* [monolith](https://github.com/Y2Z/monolith) ⭐ 14,961 | 🐛 75 | 🌐 Rust | 📅 2026-02-05 - CLI tool to save a web page as a single HTML file. *(Stable)*
* [DiskerNet](https://github.com/DO-SAY-GO/dn) ⭐ 3,899 | 🐛 25 | 🌐 JavaScript | 📅 2026-03-28 - A non-WARC-based tool which hooks into the Chrome browser and archives everything you browse making it available for offline replay. *(In Development)*
* [Heritrix](https://github.com/internetarchive/heritrix3/wiki) ⭐ 3,209 | 🐛 42 | 🌐 Java | 📅 2026-04-02 - An open source, extensible, web-scale, archival quality web crawler. *(Stable)*
  * [Heritrix Q\&A](https://github.com/internetarchive/heritrix3/discussions/categories/q-a) ⭐ 3,209 | 🐛 42 | 🌐 Java | 📅 2026-04-02 - A discussion forum for asking questions and getting answers about using Heritrix.
  * [Heritrix Walkthrough](https://github.com/web-archive-group/heritrix-walkthrough) ⭐ 10 | 🐛 2 | 🌐 Shell | 📅 2016-06-10 *(In Development)*
* [Wayback](https://github.com/wabarc/wayback) ⭐ 2,173 | 🐛 57 | 🌐 Go | 📅 2026-03-30 - A toolkit for snapshot webpage to Internet Archive, archive.today, IPFS and beyond. *(Stable)*
* [grab-site](https://github.com/ArchiveTeam/grab-site) ⭐ 1,559 | 🐛 98 | 🌐 Python | 📅 2025-05-23 - The archivist's web crawler: WARC output, dashboard for all crawls, dynamic ignore patterns. *(Stable)*
* [twarc](https://github.com/DocNow/twarc) ⭐ 1,392 | 🐛 48 | 🌐 Python | 📅 2025-10-31 - A command line tool and Python library for archiving Twitter JSON data. *(Stable)*
* [Auto Archiver](https://github.com/bellingcat/auto-archiver) ⭐ 1,063 | 🐛 18 | 🌐 Python | 📅 2026-04-02 - Python script to automatically archive social media posts, videos, and images from a Google Sheets document. Read the [article about Auto Archiver on bellingcat.com](https://www.bellingcat.com/resources/2022/09/22/preserve-vital-online-content-with-bellingcats-auto-archiver-tool/).
* [Browsertrix Crawler](https://github.com/webrecorder/browsertrix-crawler) ⭐ 1,014 | 🐛 131 | 🌐 TypeScript | 📅 2026-04-03 - A Chromium based high-fidelity crawling system, designed to run a complex, customizable browser-based crawl in a single Docker container. *(Stable)*
* [Brozzler](https://github.com/internetarchive/brozzler) ⭐ 795 | 🐛 57 | 🌐 Python | 📅 2026-03-26 - A distributed web crawler (爬虫) that uses a real browser (Chrome or Chromium) to fetch pages and embedded urls and to extract links. *(Stable)*
* [Wpull](https://github.com/ArchiveTeam/wpull) ⭐ 604 | 🐛 208 | 🌐 HTML | 📅 2024-04-29 - A Wget-compatible (or remake/clone/replacement/alternative) web downloader and crawler. *(Stable)*
* [Waybackpy](https://github.com/akamhy/waybackpy) ⭐ 568 | 🐛 21 | 🌐 Python | 📅 2024-02-26 -  Wayback Machine Save, CDX and availability API interface in Python and a command-line tool  *(Stable)*
* [Warcprox](https://github.com/internetarchive/warcprox) ⭐ 448 | 🐛 26 | 🌐 Python | 📅 2026-04-01 - WARC-writing MITM HTTP/S proxy. *(Stable)*
* [archivenow](https://github.com/oduwsdl/archivenow) ⭐ 432 | 🐛 18 | 🌐 Python | 📅 2024-01-23 - A [Python library](http://ws-dl.blogspot.com/2017/02/2017-02-22-archive-now-archivenow.html) to push web resources into on-demand web archives. *(Stable)*
* [WAIL](https://github.com/machawk1/wail) ⭐ 394 | 🐛 184 | 🌐 Roff | 📅 2025-03-12 - A graphical user interface (GUI) atop multiple web archiving tools intended to be used as an easy way for anyone to preserve and replay web pages; [Python](https://machawk1.github.io/wail/), [Electron](https://github.com/n0tan3rd/wail) ⭐ 128 | 🐛 34 | 🌐 JavaScript | 📅 2019-02-03. *(Stable)*
* [Obelisk](https://github.com/go-shiori/obelisk) ⭐ 309 | 🐛 10 | 🌐 Go | 📅 2026-02-01 - Go package and CLI tool for saving web page as single HTML file. *(Stable)*
* [freeze-dry](https://github.com/WebMemex/freeze-dry) ⭐ 302 | 🐛 21 | 🌐 TypeScript | 📅 2022-09-18 - JavaScript library to turn page into static, self-contained HTML document; useful for browser extensions. *(In Development)*
* [Scoop](https://github.com/harvard-lil/scoop) ⭐ 196 | 🐛 14 | 🌐 JavaScript | 📅 2025-09-03 - High-fidelity, browser-based, single-page web archiving library and CLI for witnessing the web. *(Stable)*
* [Squidwarc](https://github.com/N0taN3rd/Squidwarc) ⭐ 174 | 🐛 11 | 🌐 JavaScript | 📅 2020-05-19 - An [open source, high-fidelity, page interacting](http://ws-dl.blogspot.com/2017/07/2017-07-24-replacing-heritrix-with.html) archival crawler that uses Chrome or Chrome Headless directly. *(In Development)*
* [Chronicler](https://github.com/CGamesPlay/chronicler) ⚠️ Archived - Web browser with record and replay functionality. *(In Development)*
* [F(b)arc](https://github.com/justinlittman/fbarc) ⚠️ Archived - A commandline tool and Python library for archiving data from [Facebook](https://www.facebook.com/) using the [Graph API](https://developers.facebook.com/docs/graph-api). *(Stable)*
* [crau](https://github.com/turicas/crau) ⭐ 64 | 🐛 10 | 🌐 Python | 📅 2023-02-19 - crau is the way (most) Brazilians pronounce crawl, it's the easiest command-line tool for archiving the Web and playing archives: you just need a list of URLs. *(Stable)*
* [Warcworker](https://github.com/peterk/warcworker) ⭐ 62 | 🐛 6 | 🌐 Python | 📅 2024-07-09 - An open source, dockerized, queued, high fidelity web archiver based on Squidwarc with a simple web GUI. *(Stable)*
* [Cairn](https://github.com/wabarc/cairn) ⭐ 50 | 🐛 28 | 🌐 TypeScript | 📅 2026-04-02 - A npm package and CLI tool for saving webpages. *(Stable)*
* [crocoite](https://github.com/PromyLOPh/crocoite) ⚠️ Archived - Crawl websites using headless Google Chrome/Chromium and save resources, static DOM snapshot and page screenshots to WARC files. *(In Development)*
* [Web2Warc](https://github.com/helgeho/Web2Warc) ⭐ 25 | 🐛 1 | 🌐 Scala | 📅 2017-10-09 - An easy-to-use and highly customizable crawler that enables anyone to create their own little Web archives (WARC/CDX). *(Stable)*
* [Wget-lua](https://github.com/alard/wget-lua) ⭐ 24 | 🐛 0 | 🌐 C | 📅 2015-12-17 - Wget with Lua extension. *(Stable)*
* [html2warc](https://github.com/steffenfritz/html2warc) ⭐ 23 | 🐛 0 | 🌐 Python | 📅 2023-05-11 - A simple script to convert offline data into a single WARC file. *(Stable)*
* [ArchiveWeb.Page](https://webrecorder.net/archivewebpage/) - A plugin for Chrome and other Chromium based browsers that lets you interactively archive web pages, replay them, and export them as WARC & WACZ files. Also available as an Electron based desktop application.
* [Community Archive](https://www.community-archive.org/) - Open Twitter Database and API with tools and resources for building on archived Twitter data.
* [Crawl](https://git.autistici.org/ale/crawl) - A simple web crawler in Golang. *(Stable)*
* [HTTrack](http://www.httrack.com/) - An open source website copying utility. *(Stable)*
* [SiteStory](http://mementoweb.github.io/SiteStory/) - A transactional archive that selectively captures and stores transactions that take place between a web client (browser) and a web server. *(Stable)*
* [Social Feed Manager](https://gwu-libraries.github.io/sfm-ui/) - Open source software that enables users to create social media collections from Twitter, Tumblr, Flickr, and Sina Weibo public APIs. *(Stable)*
* [StormCrawler](http://stormcrawler.net/) - A collection of resources for building low-latency, scalable web crawlers on Apache Storm. *(Stable)*
* [WARCreate](http://matkelly.com/warcreate/) - A [Google Chrome](https://www.google.com/intl/en/chrome/browser/) extension for archiving an individual webpage or website to a WARC file. *(Stable)*
* [Web Curator Tool](https://webcuratortool.org) - Open-source workflow management for selective web archiving. *(Stable)*
* [WebMemex](https://github.com/WebMemex) - Browser extension for Firefox and Chrome which lets you archive web pages you visit. *(In Development)*
* [Wget](http://www.gnu.org/software/wget/) - An open source file retrieval utility that of [version 1.14 supports writing warcs](http://www.archiveteam.org/index.php?title=Wget_with_WARC_output). *(Stable)*

### Replay

* [PYWB](https://github.com/webrecorder/pywb) ⭐ 1,640 | 🐛 180 | 🌐 JavaScript | 📅 2026-04-03 - A Python 3 implementation of web archival replay tools, sometimes also known as 'Wayback Machine'. *(Stable)*
* [InterPlanetary Wayback (ipwb)](https://github.com/oduwsdl/ipwb) ⭐ 652 | 🐛 159 | 🌐 Python | 📅 2025-10-10 - Web Archive (WARC) indexing and replay using [IPFS](https://ipfs.io/).
* [OpenWayback](https://github.com/iipc/openwayback/) ⭐ 516 | 🐛 105 | 🌐 Java | 📅 2024-01-03 - The open source project aimed to develop Wayback Machine, the key software used by web archives worldwide to play back archived websites in the user's browser. *(Stable)*
* [warc2html](https://github.com/iipc/warc2html) ⭐ 51 | 🐛 5 | 🌐 Java | 📅 2025-09-18 - Converts WARC files to static HTML suitable for browsing offline or rehosting.
* [Reconstructive](https://oduwsdl.github.io/Reconstructive/) - Reconstructive is a ServiceWorker module for client-side reconstruction of composite mementos by rerouting resource requests to corresponding archived copies (JavaScript).
* [ReplayWeb.page](https://webrecorder.net/replaywebpage/) - A browser-based, fully client-side replay engine for both local and remote WARC & WACZ files. Also available as an Electron based desktop application. *(Stable)*

### Search & Discovery

* [hyphe](https://github.com/medialab/hyphe) ⭐ 376 | 🐛 51 | 🌐 JavaScript | 📅 2026-03-17 - A webcrawler built for research uses with a graphical user interface in order to build web corpuses made of lists of web actors and maps of links between them. *(Stable)*
* [SolrWayback](https://github.com/netarchivesuite/solrwayback) ⭐ 137 | 🐛 64 | 🌐 Java | 📅 2026-03-10 - A backend Java and frontend VUE JS project with freetext search and a build in playback engine. Require Warc files has been index with the Warc-Indexer. The web application also has a wide range of data visualization tools and data export tools that can be used on the whole webarchive. [SolrWayback 4 Bundle release](https://github.com/netarchivesuite/solrwayback/releases) ⭐ 137 | 🐛 64 | 🌐 Java | 📅 2026-03-10 contains all the software and dependencies in an out-of-the box solution that is easy to install.
* [webarchive-discovery](https://github.com/ukwa/webarchive-discovery) ⭐ 132 | 🐛 93 | 🌐 Java | 📅 2025-11-21 - WARC and ARC full-text indexing and discovery tools, with a number of associated tools capable of using the index shown below. *(Stable)*
* Other possible options for builting a front-end are listed on in the `webarchive-discovery` wiki, [here](https://github.com/ukwa/webarchive-discovery/wiki/Front-ends) ⭐ 132 | 🐛 93 | 🌐 Java | 📅 2025-11-21.
* [Mink](https://github.com/machawk1/Mink) ⭐ 58 | 🐛 95 | 🌐 JavaScript | 📅 2025-08-27 - A [Google Chrome](https://www.google.com/intl/en/chrome/) extension for querying Memento aggregators while browsing and integrating live-archived web navigation. *(Stable)*
* [Warclight](https://github.com/archivesunleashed/warclight) ⚠️ Archived - A Project Blacklight based Rails engine that supports the discovery of web archives held in the WARC and ARC formats. *(In Development)*
* [Shine](https://github.com/ukwa/shine) ⚠️ Archived - A prototype web archives exploration UI, developed with researchers as part of the [Big UK Domain Data for the Arts and Humanities project](https://buddah.projects.history.ac.uk/). *(Stable)*
* [Wasp](https://github.com/webis-de/wasp) ⭐ 27 | 🐛 3 | 🌐 Java | 📅 2022-10-14 - A fully functional prototype of a personal [web archive and search system](http://ceur-ws.org/Vol-2167/paper6.pdf). *(In Development)*
* [PANDORÆ](https://github.com/Guillaume-Levrier/PANDORAE) ⭐ 16 | 🐛 1 | 🌐 JavaScript | 📅 2025-12-09 - A desktop research software to be plugged on a Solr endpoint to query, retrieve, normalize and visually explore web archives. *(Stable)*
* [playback](https://github.com/wabarc/playback) ⭐ 13 | 🐛 7 | 🌐 Go | 📅 2024-04-19 - A toolkit for searching archived webpages from <!--lint ignore double-link-->[Internet Archive](https://web.archive.org), [archive.today](https://archive.today), [Memento](http://timetravel.mementoweb.org) and beyond. *(In Development)*
* [SecurityTrails](https://securitytrails.com/) - Web based archive for WHOIS and DNS records. REST API available free of charge.
* [Tempas v1](http://tempas.L3S.de/v1) - Temporal web archive search based on [Delicious](https://en.wikipedia.org/wiki/Delicious_\(website\)) tags. *(Stable)*
* [Tempas v2](http://tempas.L3S.de/v2) - Temporal web archive search based on links and anchor texts extracted from the German web from 1996 to 2013 (results are not limited to German pages, e.g., [Obama@2005-2009 in Tempas](http://tempas.l3s.de/v2/query?q=obama\&from=2005\&to=2009)). *(Stable)*

### Utilities

* [Go Get Crawl](https://github.com/karust/gogetcrawl) ⭐ 175 | 🐛 0 | 🌐 Go | 📅 2024-11-04 - Extract web archive data using <!--lint ignore double-link-->[Wayback Machine](https://web.archive.org/) and [Common Crawl](https://commoncrawl.org/). *(Stable)*
* [ArchiveTools](https://github.com/recrm/ArchiveTools) ⭐ 78 | 🐛 2 | 🌐 Python | 📅 2022-07-06 - Collection of tools to extract and interact with WARC files (Python).
* [har2warc](https://github.com/webrecorder/har2warc) ⭐ 56 | 🐛 3 | 🌐 Python | 📅 2018-10-21 - Convert HTTP Archive (HAR) -> Web Archive (WARC) format (Python).
* [duckdb-web-archive-cdx](https://github.com/midwork-finds-jobs/duckdb-web-archive) ⭐ 17 | 🐛 2 | 🌐 C++ | 📅 2026-02-03 - DuckDB extension to query the Internet Archive and CommonCrawl CDX APIs directly from SQL. *(In Development)*
* [gowarcserver](https://github.com/nlnwa/gowarcserver) ⭐ 17 | 🐛 10 | 🌐 Go | 📅 2025-03-31 - [BadgerDB](https://github.com/dgraph-io/badger) ⭐ 15,548 | 🐛 46 | 🌐 Go | 📅 2026-04-01-based capture index (CDX) and WARC record server, used to index and serve WARC files (Go).
* [bagnabit2warc](https://github.com/internetarchive/bagnabit2warc) ⭐ 1 | 🐛 0 | 🌐 Python | 📅 2026-03-09 - Convert a [bag-nabit](https://github.com/harvard-lil/bag-nabit) ⭐ 38 | 🐛 1 | 🌐 Python | 📅 2025-03-31 dataset stored in a ZIP into a full-content WARC.
* [cdx-toolkit](https://pypi.org/project/cdx-toolkit/) - Library and CLI to consult cdx indexes and create WARC extractions of subsets. Abstracts away Common Crawl's unusual crawl structure. *(Stable)*

<!--lint ignore double-link-->

* [Internet Archive Library](https://github.com/jjjake/internetarchive) ⭐ 1,846 | 🐛 94 | 🌐 Python | 📅 2026-04-02 - A command line tool and Python library for interacting directly with <!--lint ignore double-link-->[archive.org](https://archive.org). (Python). *(Stable)*
* [wikiteam](https://github.com/WikiTeam/wikiteam) ⭐ 830 | 🐛 172 | 🌐 Python | 📅 2026-01-10 - Tools for downloading and preserving wikis. *(Stable)*
* [warcdb](https://github.com/florents-Tselai/warcdb) ⭐ 405 | 🐛 8 | 🌐 Python | 📅 2024-07-13 - A command line utility (Python) for importing WARC files into a SQLite database. *(Stable)*
* [MemGator](https://github.com/oduwsdl/MemGator) ⭐ 78 | 🐛 47 | 🌐 Go | 📅 2025-03-04 - A Memento Aggregator CLI and Server (Golang). *(Stable)*
* [webarchive-indexing](https://github.com/ikreymer/webarchive-indexing) ⭐ 47 | 🐛 5 | 🌐 Python | 📅 2017-12-04 - Tools for bulk indexing of WARC/ARC files on Hadoop, EMR or local file system.
* [OutbackCDX](https://github.com/nla/outbackcdx) ⭐ 38 | 🐛 22 | 🌐 Java | 📅 2026-04-01 - RocksDB-based capture index (CDX) server supporting incremental updates and compression. Can be used as backend for OpenWayback, PyWb and [Heritrix](https://github.com/ukwa/ukwa-heritrix/blob/master/src/main/java/uk/bl/wap/modules/uriuniqfilters/OutbackCDXRecentlySeenUriUniqFilter.java) ⚠️ Archived. *(Stable)*
* [httrack2warc](https://github.com/nla/httrack2warc) ⭐ 34 | 🐛 2 | 🌐 Java | 📅 2024-08-06 - Convert HTTrack archives to WARC format (Java).
* [warc-safe](https://github.com/natliblux/warc-safe) ⭐ 18 | 🐛 1 | 🌐 Python | 📅 2025-12-16 - Automatic detection of viruses and NSFW content in WARC files.
* [py-wasapi-client](https://github.com/unt-libraries/py-wasapi-client) ⭐ 16 | 🐛 0 | 🌐 Python | 📅 2019-10-18 - Command line application to download crawls from WASAPI (Python). *(Stable)*
* [MementoMap](https://github.com/oduwsdl/MementoMap) ⭐ 11 | 🐛 0 | 🌐 Python | 📅 2021-06-15 - A Tool to Summarize Web Archive Holdings (Python). *(In Development)*
* [tikalinkextract](https://github.com/httpreserve/tikalinkextract) ⭐ 11 | 🐛 6 | 🌐 HTML | 📅 2025-04-26 - Extract hyperlinks as a seed for web archiving from folders of document types that can be parsed by Apache Tika (Golang, Apache Tika Server). *(In Development)*
* [HTTPreserve linkstat](https://github.com/httpreserve/linkstat) ⭐ 10 | 🐛 1 | 🌐 Go | 📅 2024-11-21 - Command line implementation of <!--lint ignore double-link-->[httpreserve.info](https://httpreserve.info) to describe the status of a web page. Can be easily scripted and provides JSON output to enable querying through tools like JQ. HTTPreserve Linkstat describes current status, and earliest and latest links on <!--lint ignore double-link-->[archive.org](https://archive.org/). (Golang). *(Stable)*
* [warcrefs](https://github.com/arcalex/warcrefs) ⭐ 10 | 🐛 11 | 🌐 Java | 📅 2018-10-18 - Web archive deduplication tools. *(Stable)*
* [warcbench](https://github.com/harvard-lil/warcbench) ⭐ 9 | 🐛 2 | 🌐 Python | 📅 2025-07-30 - A tool for exploring, analyzing, transforming, recombining, and extracting data from WARC (Web ARChive) files.
* [wasapi-downloader](https://github.com/sul-dlss/wasapi-downloader) ⭐ 7 | 🐛 25 | 🌐 Java | 📅 2025-11-17 - Java command line application to download crawls from WASAPI. *(Stable)*
* [node-cdxj](https://github.com/N0taN3rd/node-cdxj) ⭐ 2 | 🐛 0 | 🌐 JavaScript | 📅 2017-07-20 - [CDXJ](https://github.com/oduwsdl/ORS/wiki/CDXJ) ⭐ 15 | 🐛 6 | 📅 2018-11-28 file parser (Node.js). *(Stable)*
* [WarcPartitioner](https://github.com/helgeho/WarcPartitioner) ⭐ 1 | 🐛 0 | 🌐 Java | 📅 2017-02-13 - Partition (W)ARC Files by MIME Type and Year. *(Stable)*
* [httpreserve.info](https://httpreserve.info) - Service to return the status of a web page or save it to the Internet Archive. HTTPreserve includes disambiguation of well-known short link services. It returns JSON via the browser or command line via CURL using GET. Describes web sites using earliest and latest dates in the Internet Archive and demonstrates the construction of Robust Links in its output using that range. (Golang). *(Stable)*
* [The Unarchiver](https://theunarchiver.com/) - Program to extract the contents of many archive formats, inclusive of WARC, to a file system. Free variant of The Archive Browser (macOS only, Proprietary app).
* [Warchaeology](https://nlnwa.github.io/warchaeology/) - Warchaeology is a collection of tools for inspecting, manipulating, deduplicating and validating WARC-files. *(Stable)*
* [warcdedupe](https://gitlab.com/taricorp/warcdedupe) - WARC deduplication tool (and WARC library) written in Rust. *(In Development)*

### WARC I/O Libraries

* [warcio](https://github.com/webrecorder/warcio) ⭐ 452 | 🐛 61 | 🌐 Python | 📅 2026-03-31 - Streaming WARC/ARC library for fast web archive IO (Python). *(Stable)*
* [warctools](https://github.com/internetarchive/warctools) ⭐ 171 | 🐛 17 | 🌐 Python | 📅 2025-08-18 - Library to work with ARC and WARC files (Python).
* [Warcat](https://github.com/chfoo/warcat) ⭐ 165 | 🐛 15 | 🌐 Python | 📅 2024-10-11 - Tool and library for handling Web ARChive (WARC) files (Python). *(Stable)*
* [FastWARC](https://github.com/chatnoir-eu/chatnoir-resiliparse) ⭐ 135 | 🐛 0 | 🌐 Cython | 📅 2026-04-02 - A high-performance WARC parsing library (Python).
* [node-warc](https://github.com/N0taN3rd/node-warc) ⭐ 104 | 🐛 23 | 🌐 JavaScript | 📅 2025-01-29 - Parse WARC files or create WARC files using either [Electron](https://electron.atom.io/) or [chrome-remote-interface](https://github.com/cyrus-and/chrome-remote-interface) ⭐ 4,520 | 🐛 12 | 🌐 JavaScript | 📅 2026-02-09 (Node.js). *(Stable)*
* [warc](https://github.com/jedireza/warc) ⭐ 59 | 🐛 10 | 🌐 Rust | 📅 2024-11-27 - A Rust library for reading and writing WARC files. *(Stable)*
* [jwarc](https://github.com/iipc/jwarc) ⭐ 55 | 🐛 19 | 🌐 Java | 📅 2026-02-26 - Read and write WARC files with a type safe API (Java).
* [Warcat-rs](https://github.com/chfoo/warcat-rs) ⭐ 29 | 🐛 5 | 🌐 Rust | 📅 2025-06-02 - Command-line tool and Rust library for handling Web ARChive (WARC) files. *(In Development)*
* [webarchive](https://github.com/richardlehane/webarchive) ⭐ 20 | 🐛 0 | 🌐 Go | 📅 2023-04-03 - Golang readers for ARC and WARC webarchive formats (Golang).
* [Sparkling](https://github.com/internetarchive/Sparkling) ⭐ 16 | 🐛 1 | 🌐 Scala | 📅 2026-03-03 - Internet Archive's Sparkling Data Processing Library. *(Stable)*
* [Unwarcit](https://github.com/emmadickson/unwarcit) ⭐ 13 | 🐛 1 | 🌐 Python | 📅 2022-01-07 - Command line interface to unzip WARC and WACZ files (Python).
* [HadoopConcatGz](https://github.com/helgeho/HadoopConcatGz) ⭐ 9 | 🐛 1 | 🌐 Java | 📅 2018-02-07 - A Splitable Hadoop InputFormat for Concatenated GZIP Files (and `*.warc.gz`). *(Stable)*
* [Jwat-Tools](https://github.com/netarchivesuite/jwat-tools) ⭐ 5 | 🐛 3 | 🌐 Java | 📅 2023-12-13 - Tools for reading/writing/validating WARC/ARC/GZIP files (Java). *(Stable)*
* [Jwat](https://github.com/netarchivesuite/jwat) ⭐ 4 | 🐛 5 | 🌐 Java | 📅 2023-12-13 - Libraries for reading/writing/validating WARC/ARC/GZIP files (Java). *(Stable)*

### Analysis

* [ArchiveSpark](https://github.com/helgeho/ArchiveSpark) ⭐ 158 | 🐛 5 | 🌐 Scala | 📅 2025-10-08 - An Apache Spark framework (not only) for Web Archives that enables easy data processing, extraction as well as derivation. *(Stable)*
* [Archives Unleashed Toolkit](https://github.com/archivesunleashed/aut) ⭐ 155 | 🐛 5 | 🌐 Scala | 📅 2025-12-05 - Archives Unleashed Toolkit (AUT) is an open-source platform for analyzing web archives with Apache Spark. *(Stable)*
* [Common Crawl Jupyter notebooks](https://github.com/commoncrawl/cc-notebooks) ⭐ 65 | 🐛 0 | 🌐 Jupyter Notebook | 📅 2025-11-22 - A collection of notebooks using Common Crawl's various datasets. *(Stable)*
* [Archives Unleashed Notebooks](https://github.com/archivesunleashed/notebooks) ⭐ 26 | 🐛 0 | 🌐 Jupyter Notebook | 📅 2022-12-05 - Notebooks for working with web archives with the Archives Unleashed Toolkit, and derivatives generated by the Archives Unleashed Toolkit. *(Stable)*
* [Archives Research Compute Hub](https://github.com/internetarchive/arch) ⭐ 20 | 🐛 0 | 🌐 Scala | 📅 2026-03-24 - Web application for distributed compute analysis of Archive-It web archive collections. *(Stable)*
* [Tweet Archvies Unleashed Toolkit](https://github.com/archivesunleashed/twut) ⭐ 10 | 🐛 1 | 🌐 Scala | 📅 2026-03-17 - An open-source toolkit for analyzing line-oriented JSON Twitter archives with Apache Spark. *(In Development)*
* [Common Crawl Columnar Index](https://commoncrawl.org/tag/columnar-index/) - SQL-queryable index, with CDX info plus language classification. *(Stable)*
* [Common Crawl Web Graph](https://commoncrawl.org/category/web-graph/) - A host or domain-level graph of the web, with ranking information. *(Stable)*
* [Web Data Commons](http://webdatacommons.org/) - Structured data extracted from Common Crawl. *(Stable)*

### Quality Assurance

* [FlameShot](https://github.com/flameshot-org/flameshot) ⭐ 29,635 | 🐛 660 | 🌐 C++ | 📅 2026-04-04 - Screen capture and annotation on Ubuntu.
* [xDoTool](https://github.com/jordansissel/xdotool) ⭐ 3,757 | 🐛 323 | 🌐 C | 📅 2026-03-19 - Click automation on Ubuntu.
* [Chrome Check My Links](https://chromewebstore.google.com/detail/check-my-links/ojkcdipcgfaekbeaelaapakgnjflfglf) - Browser extension: a link checker with more options.
* [Chrome link checker](https://chromewebstore.google.com/detail/link-checker/aibjbgmpmnidnmagaefhmcjhadpffaoi) - Browser extension: basic link checker.
* [Chrome link gopher](https://chromewebstore.google.com/detail/bpjdkodgnbfalgghnbeggfbfjpcfamkf/publish-accepted?hl=en-US\&gl=US) - Browser extension: link harvester on a page.
* [Chrome Open Multiple URLs](https://chromewebstore.google.com/detail/open-multiple-urls/oifijhaokejakekmnjmphonojcfkpbbh?hl=de) - Browser extension: opens multiple URLs and also extracts URLs from text.
* [Chrome Revolver](https://chromewebstore.google.com/detail/revolver-tabs/dlknooajieciikpedpldejhhijacnbda) - Browser extension: switches between browser tabs.
* [PlayOnLinux](https://www.playonlinux.com/en/) - For running Xenu and Notepad++ on Ubuntu.
* [PlayOnMac](https://www.playonmac.com/en/) - For running Xenu and Notepad++ on macOS.
* [Windows Snipping Tool](https://support.microsoft.com/en-gb/help/13776/windows-use-snipping-tool-to-capture-screenshots) - Windows built-in for partial screen capture and annotation. On macOS you can use Command + Shift + 4 (keyboard shortcut for taking partial screen capture).
* [WineBottler](http://winebottler.kronenberg.org/) - For running Xenu and Notepad++ on macOS.
* [Xenu](http://home.snafu.de/tilman/xenulink.html) - Desktop link checker for Windows.

### Curation

* [Zotero Robust Links Extension](https://robustlinks.mementoweb.org/zotero/) - A [Zotero](https://www.zotero.org/) extension that submits to and reads from web archives. Source [on GitHub](https://github.com/lanl/Zotero-Robust-Links-Extension) ⭐ 21 | 🐛 3 | 🌐 JavaScript | 📅 2022-05-10. Supercedes [leonkt/zotero-memento](https://github.com/leonkt/zotero-memento) ⭐ 351 | 🐛 12 | 🌐 JavaScript | 📅 2022-06-08.

## Community Resources

### Other Awesome Lists

* [Web Archiving Community](https://github.com/ArchiveBox/ArchiveBox/wiki/Web-Archiving-Community) ⭐ 27,175 | 🐛 200 | 🌐 Python | 📅 2026-04-05
* [Awesome Memento](https://github.com/machawk1/awesome-memento) ⭐ 113 | 🐛 2 | 📅 2026-02-04
* [The WARC Ecosystem](http://www.archiveteam.org/index.php?title=The_WARC_Ecosystem)
* [The Web Crawl section of COPTR](http://coptr.digipres.org/Category:Web_Crawl)

### Blogs and Scholarship

* [IIPC Blog](https://netpreserveblog.wordpress.com/)
* [Web Archiving Roundtable](https://webarchivingrt.wordpress.com/) - Unofficial blog of the Web Archiving Roundtable of the [Society of American Archivists](https://www2.archivists.org/) maintained by the members of the Web Archiving Roundtable.
* [The Web as History](https://www.uclpress.co.uk/products/84010) - An open-source book that provides a conceptual overview to web archiving research, as well as several case studies.
* [WS-DL Blog](https://ws-dl.blogspot.com/) - Web Science and Digital Libraries Research Group blogs about various Web archiving related topics, scholarly work, and academic trip reports.
* [DSHR's Blog](https://blog.dshr.org/) - David Rosenthal regularly reviews and summarizes work done in the Digital Preservation field.
* [UK Web Archive Blog](https://blogs.bl.uk/webarchive/)
* [Common Crawl Foundation Blog](https://commoncrawl.org/blog) - [rss](http://commoncrawl.org/blog/rss.xml)

### Mailing Lists

* [Common Crawl](https://groups.google.com/g/common-crawl)
* [IIPC](http://netpreserve.org/about-us/iipc-mailing-list/)
* [OpenWayback](https://groups.google.com/g/openwayback-dev)
* [WASAPI](https://groups.google.com/g/wasapi-community)

### Slack

* [IIPC Slack](https://iipc.slack.com/) - Ask [@netpreserve](https://twitter.com/NetPreserve?s=20) for access.
* [Archives Unleashed Slack](https://archivesunleashed.slack.com/) - [Fill out this request form](http://slack.archivesunleashed.org/) for access to a researcher group of people working with web archives.
* [Archivers Slack](https://archivers.slack.com) - [Invite yourself](https://archivers-slack.herokuapp.com/) to a multi-disciplinary effort for archiving projects run in affiliation with [EDGI](https://envirodatagov.org/archiving/) and [Data Together](http://datatogether.org/).
* [Common Crawl Foundation Partners](https://ccfpartners.slack.com/) (ask greg zat commoncrawl zot org for an invite)

### Discord

* [Common Crawl Foundation](https://discord.gg/njaVFh7avF)

### Twitter

* [@commoncrawl](https://twitter.com/commoncrawl) - Official Common Crawl Foundation handle.
* [@NetPreserve](https://twitter.com/NetPreserve) - Official IIPC handle.
* [@WebSciDL](https://twitter.com/WebSciDL) - ODU Web Science and Digital Libraries Research Group.
* [#WebArchiving](https://twitter.com/search?q=%23webarchiving)
* [#WebArchiveWednesday](https://twitter.com/hashtag/webarchivewednesday)

## Web Archiving Service Providers

The intention is that we only list services that allow web archives to be exported in standard formats (WARC or WACZ). But this is not an endorsement of these services, and readers should check and evaluate these options based on their needs.

### Self-hostable, Open Source

* [Browsertrix](https://webrecorder.net/browsertrix/) - From [Webrecorder](https://webrecorder.net/), source available at <https://github.com/webrecorder/browsertrix> ⭐ 396 | 🐛 271 | 🌐 TypeScript | 📅 2026-04-02.
* [Conifer](https://conifer.rhizome.org/) - From [Rhizome](https://rhizome.org/), source available at <https://github.com/Rhizome-Conifer>.

### Hosted, Closed Source

* [Archive-It](https://archive-it.org/) - From the Internet Archive.
* [Arkiwera](https://arkiwera.se/wp/websites/)
* [Hanzo](https://www.hanzo.co/chronicle)
* [MirrorWeb](https://www.mirrorweb.com/solutions/capabilities/website-archiving)
* [PageFreezer](https://www.pagefreezer.com/)
* [Smarsh](https://www.smarsh.com/platform/compliance-management/web-archive)

## Public Data

This is a list of publicly available WARCs, Wayback Machines, CDX API endpoints, other indexes, and so on.

* [Common Crawl files](https://data.commoncrawl.org/) - WARCs, CDX files, parquet url index, parquet host index, etc.
* [Common Crawl CDX API](https://index.commoncrawl.org/)
* [End of Term Archive](https://eotarchive.org/) - WARCs, CDX files, parquet url index
* [Internet Archive Wayback](https://web.archive.org/)
* [Webrecorder US GovArchive](https://govarchive.us/) - high-fidelity replay
* [UK Government Web Archive](https://www.nationalarchives.gov.uk/webarchive/) - Wayback
