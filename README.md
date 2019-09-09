# Cutter Plugins
This is a curated list of **Plugins** and **Scripts** written for the reverse engineering platform - Cutter.

Want to build your own Plugin for Cutter, or to port an existing one? Follow the tutorial in the official documentation: https://cutter.re/docs/plugins.html


## Table of Contents
- [Cutter Plugins](#Cutter-Plugins)
  - [Decompilers](#Integrations)
    - [Ghidra Decompiler](#Ghidra-Decompiler)
    - [r2dec](#r2dec)
  - [Integrations](#Integrations)
    - [Jupyter Plugin](#Jupyter-Plugin)
  - [Malware Analysis](#Malware-Analysis)
    - [APT32 Graph Deobfuscator](#APT32-Graph-Deobfuscator)
    - [Dropshot / StoneDrill Decrypter](#Dropshot--StoneDrill-Decrypter)
    - [Deobfuscate Bitpaymer API Calls](#Deobfuscate-Bitpaymer-API-Calls)
  - [Coverage](#Coverage)
    - [CutterDRcov](#CutterDRcov)
    - [Cutter Lighthouse](#Cutter-Lighthouse)
  - [Enhancements](#Enhancements)
    - [Assembly-reference](#Assembly-reference)
    - [Recovering Stack Strings](#Recovering-Stack-Strings)
  - [Graphs](#Graphs)
    - [Cutter Deep Graphs](#Cutter-Deep-Graphs)
  - [Misc](#Misc)
    - [Cutter plugin templates](#Cutter-plugin-templates)
---

## Decompilers

### [Ghidra Decompiler](https://github.com/thestr4ng3r/r2ghidra-dec)
This is an integration of the Ghidra decompiler for Cutter and radare2. It is solely based on the decompiler part of Ghidra, which is written entirely in C++, so neither Ghidra itself nor JAVA are required at all and the plugin can be built self-contained.

Due to its quality, the ghidra decompiler plugin is shipped by default in Cutter releases.

**Type**: Plugin  
**Status**: Maintained  
**Reference**: [r2ghidra plugin announced in Cutter v1.9](https://twitter.com/r2gui/status/1169912280001208321)

### [r2dec](https://github.com/wargio/r2dec-js)
r2dec converts the assembly of a function to a Pseudo-C code. Cutter integrates r2dec by default. 

**Type**: Plugin  
**Status**: Maintained  
**Talk**: [How not to write a decompiler - r2con 2018](https://www.youtube.com/watch?v=2siU7B0PjPI)

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

**Type**: Plugin  
**Status**: Maintained  
**Article**: [APT32 Flow Graphs with Cutter and Radare2](https://research.checkpoint.com/deobfuscating-apt32-flow-graphs-with-cutter-and-radare2/)


### [Dropshot / StoneDrill Decrypter](https://github.com/ITAYC0HEN/A-journey-into-Radare2/blob/master/Part%203%20-%20Malware%20analysis/decrypt_dropshot.py)
This is an r2pipe based script that is used to decrypt strings and resources in the Dropshot APT malware.

**Type**: Script  
**Status**: Maintained  
**Articles**: 
 - [Decrypting APT33’s Dropshot Malware with Radare2 and Cutter – Part 1](https://www.megabeets.net/decrypting-dropshot-with-radare2-and-cutter-part-1)
 - [Decrypting APT33’s Dropshot Malware with Radare2 and Cutter – Part 2](https://www.megabeets.net/decrypting-dropshot-with-radare2-and-cutter-part-2)


### [Deobfuscate Bitpaymer API Calls](https://github.com/mauronz/malware_analysis/blob/master/deobf_bitpaymer_cutter.py)
Deobfuscation script of API calls in Bitpaymer (v2)

**Type**: Script  
**Reference**: https://twitter.com/FraMauronz/status/1005138478261309440

## Coverage

### [CutterDRcov](https://github.com/oddcoder/CutterDRcov)
CutterDrcov is code coverage plugin that visualizes DynamoRIO drcov into Cutter static analysis.

**Type**: Plugin  
**Status**: Maintained  

### [Cutter Lighthouse](https://github.com/gaasedelen/lighthouse)

This is still a work in progress on this [Pull Request](https://github.com/gaasedelen/lighthouse/pull/65).

**Type**: Plugin  
**Status**: WIP  


## Enhancements

### [Assembly-reference](https://github.com/daringjoker/Assembly-refrence)

A plugin for Cutter that shows the information about the assembly instruction currently selected (only for x86 and x64)

**Type**: Plugin  
**Status**: Maintained

### [Recovering Stack Strings](https://github.com/securitykitten/cutter_scripts/blob/master/scripts/cutter_stackstrings.py)

Cutter script to comment value of strings that were manually created on the stack.

**Type**: Script  
**Status**: Maintained



## Graphs

### [Cutter Deep Graphs](https://github.com/JavierYuste/radare2-deep-graph)
A Cutter plugin to generate radare2 graphs. It also provides a new graph called Deep callgraph, which builds an in-depth callgraph from the current function, adding recursively its callees' callings.

**Type**: Plugin  
**Status**: Maintained


## Misc
### [Cutter plugin templates](https://github.com/radareorg/cutter/tree/master/src/plugins)
Python and C++ sample plugins to start with.

**Type**: Plugin  
**Status**: Maintained
