# Cutter Plugins
This is a curated list of **Plugins** and **Scripts** written for the reverse engineering platform - Cutter.

Want to build your own Plugin for Cutter, or to port an existing one? Follow the tutorial in the official documentation: https://cutter.re/docs/plugins.html


## Table of Contents

  - [Integrations](#Integrations)
    - [Jupyter Plugin](#Jupyter-Plugin)
  - [Malware Analysis](#Malware-Analysis)
    - [APT32 Graph Deobfuscator](#APT32-Graph-Deobfuscator)
    - [Dropshot / StoneDrill Decrypter](#Dropshot--StoneDrill-Decrypter)
  - [Coverage](#Coverage)
    - [CutterDRcov](#CutterDRcov)
    - [Cutter Lighthouse](#Cutter-Lighthouse)
  - [Enhancements](#Enhancements)
    - [Assembly-reference](#Assembly-reference)
  - [Graphs](#Graphs)
    - [Cutter Deep Graphs](#Cutter-Deep-Graphs)
  - [Misc](#Misc)
    - [Cutter plugin templates](#Cutter-plugin-templates)
---

## Integrations
### [Jupyter Plugin](https://github.com/radareorg/cutter-jupyter  )

This plugin integrates the Jupyter notebook inside Cutter

**Status**: Maintained  



## Malware Analysis


### [APT32 Graph Deobfuscator](https://github.com/CheckPointSW/Cyber-Research/blob/master/Malware/APT32/APT32GraphDeobfuscator.py)
A plugin for Cutter and Radare2 to deobfuscate APT32 flow graphs
This is a python plugin for Cutter that is compatible as an r2pipe script for
radare2 as well. The plugin will help reverse engineers to deobfuscate and remove
junk blocks from APT32 (Ocean Lotus) samples.

**Status**: Maintained  
**Article**: [APT32 Flow Graphs with Cutter and Radare2](https://research.checkpoint.com/deobfuscating-apt32-flow-graphs-with-cutter-and-radare2/)


### [Dropshot / StoneDrill Decrypter](https://github.com/ITAYC0HEN/A-journey-into-Radare2/blob/master/Part%203%20-%20Malware%20analysis/decrypt_dropshot.py)
This is an r2pipe based script that is used to decrypt strings and resources in the Dropshot APT malware.

**Status**: Maintained  
**Articles**: 
 - [Decrypting APT33’s Dropshot Malware with Radare2 and Cutter – Part 1](https://www.megabeets.net/decrypting-dropshot-with-radare2-and-cutter-part-1)
 - [Decrypting APT33’s Dropshot Malware with Radare2 and Cutter – Part 2](https://www.megabeets.net/decrypting-dropshot-with-radare2-and-cutter-part-2)




## Coverage

### [CutterDRcov](https://github.com/oddcoder/CutterDRcov)
CutterDrcov is code coverage plugin that visualizes DynamoRIO drcov into Cutter static analysis.

**Status**: Maintained  

### [Cutter Lighthouse](https://github.com/gaasedelen/lighthouse)

This is still a work in progress on this [Pull Request](https://github.com/gaasedelen/lighthouse/pull/65).

**Status**: WIP  


## Enhancements

### [Assembly-reference](https://github.com/daringjoker/Assembly-refrence)

A plugin for Cutter that shows the information about the assembly instruction currently selected (only for x86 and x64)

**Status**: Maintained




## Graphs

### [Cutter Deep Graphs](https://github.com/JavierYuste/radare2-deep-graph)
A Cutter plugin to generate radare2 graphs. It also provides a new graph called Deep callgraph, which builds an in-depth callgraph from the current function, adding recursively its callees' callings.

**Status**: Maintained


## Misc
### [Cutter plugin templates](https://github.com/radareorg/cutter/tree/master/src/plugins)
Python and C++ sample plugins to start with.

**Status**: Maintained
