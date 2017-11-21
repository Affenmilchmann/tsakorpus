# Tsakorpus

If you want to use tsakorpus, please download [the latest stable version (1.0)](https://bitbucket.org/tsakorpus/tsakonian_corpus_platform/get/1.0.zip).

## Overview

Tsakorpus is a linguistic corpus search platform which uses elasticsearch for storing and querying data. It consists of a set of source convertors, an indexator and a web interface with a search engine. The source convertors transform a corpus in one of the several supported formats into a set of JSON documents in tsakorpus format. The indexator puts these documents into the database together with the frequency data for words that it calculates on the fly. The web interface, written in python+flask, allows the user to make complex queries using GUI and view the search results. The search queries are sent to the back-end as GET queries and transformed to JSON elasticsearch queries on the server. The search results are partly transformed to HTML on the server, sent back to the front-end as JSON through Ajax requests and displayed on the results page by a set of JavaScript/jQuery functions.

Tsakorpus is still being developed. Current stable version (1.0) supports corpora with morphological annotation, special gloss search, multi-word search, subcorpus selection, automatic transliteration, word distribution charts, parallel corpora, and media-aligned corpora. Multiple interface languages are supported with Flask-Babel.

See ``docs/faq.md`` (or its Russian version, ``docs/faq_ru.md``) for a short FAQ list. See ``docs/pipeline.md`` for an overview of how to use tsakorpus.

## Requirements

Tsakorpus was tested on Windows and Ubuntu. Its dependencies are the following:

* elasticsearch 5.x
* python >= 3.5
* python modules: flask, lxml, ijson, Flask-Babel, xlsxwriter
* for converting media-aligned corpora: ffmpeg
* it is recommended to deploy tsakorpus through apache2 with wsgi

The following resources are used by tsakorpus, but do not need to be installed:

* [jQuery](https://jquery.com/) library
* [video.js](http://videojs.com/) media player
* [videojs-youtube](https://github.com/videojs/videojs-youtube) plugin
* [bootstrap](http://getbootstrap.com/) toolkit
* [D3.js](https://d3js.org/) visualization library

## License

The software is distributed under MIT license (see LICENSE.md).
