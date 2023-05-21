# How to Contribute

Inspired by [pyvideo](https://github.com/pyvideo/data/blob/main/CONTRIBUTING.rst), this folder contains the index files for videos, each video's details are stored in a JSON file.

## JSON data structure

To contribute the file, please refer to [pyvideo](https://github.com/pyvideo/data/blob/main/CONTRIBUTING.rst#json-objects)'s JSON object definition.

Required fields for the JSON object are:

| key           | value type       | details      |
| ----------- | ---------- | ------- |
| description   | rST string       | (see below)  |
| speakers      | array of strings |              |
| thumbnail_url | string           |              |
| title         | string           |              |
| recorded      | string           | (YYYY-MM-DD) |
| videos        | array of objects |         |
