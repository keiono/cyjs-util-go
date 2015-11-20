# ___cxtool___: CX File Format Converter

## Introduction
This is a command line tool to convert [CX](https://docs.google.com/document/d/1kAUzVj6X86YCWHnTyZtybh1lt4zO-M6anCMJBD_PyG0/edit?usp=sharing) 
format into Cytoscape.js JSON and may others.

## Status
* 11/20/2015: Pre alpha.  Simply converts CX to basic Cytoscpae.js JSON.

### Supported Functions

* ___From CX___
    * Cytoscape.js (both Style and Graph)
    
* ___To CX___
    * SIF (Simple Interaction Format)
    * Cytoscape.js (ONGOING)

## How to Use
This is a small collection of tools to support round-trip for CX and 
related documents.
 
### Basic Usage

1. Convert CX file into Cytoscape.js

```bash
cxtool input_file
```

We recommend to install [jq](https://stedolan.github.io/jq/) for generating human-friendly output.
 
The following command creates nicely formatted Cytoscape.js JSON. 

```bash
cxtool input_file | jq
```

Or, use pipe for input

```bash
cat network.cx | cxtool | jq .
curl http://example.com/network.cx | cxtool | jq . > cytoscapejs1.json
```

2. Create CX from SIF

```bash
cxtool -f sif galFiltered.sif | jq | from_sif.cx
```


### Command Line Options
(TBD)

### License
MIT License

### Question?
Please send your question to (kono at ucsd edu).

----

&copy; 2015 The Cytoscape Consortium
