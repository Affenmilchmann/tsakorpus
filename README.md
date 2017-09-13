# Tsakorpus

## Overview

Tsakorpus is a linguistic corpus search platform which uses elasticsearch for storing and querying data. It consists of a set of source converters, an indexator and a web interface with a search engine. The source convertors transform a corpus in one of the several supported formats into a set of JSON documents in tsakorpus format. The indexator puts these documents into the database together with the frequency data for words that it calculates on the fly. The web interface, written in flask, allows the user to make complex queries using GUI and view the search results. The search queries are sent to the back-end as GET queries and transformed to JSON elasticsearch queries on the server. The search results are partly transformed to HTML on the server, sent back to the front-end as JSON through Ajax queries and displayed on the results page by a set of JavaScript functions.

Tsakorpus is under construction as of now. The pilot version supports corpora with morphological annotation, special gloss search, multi-word search, automatic transliteration, parallel corpora, and media-aligned corpora.

## Requirements

Tsakorpus was tested on Windows and Ubuntu. Its dependencies are the following:

* elasticsearch 5.x
* python >= 3.5
* python modules: flask, lxml, xlsxwriter
* for converting media-aligned corpora: ffmpeg
* it is recommended to deploy tsakorpus through apache2 with wsgi

