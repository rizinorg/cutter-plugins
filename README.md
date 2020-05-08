# Cutter Plugins
This is a curated list of **Plugins** and **Scripts** written for the reverse engineering platform - Cutter.

Want to build your own Plugin for Cutter, or to port an existing one from other disassemblers? It is easy! Follow the tutorial in the official documentation: https://cutter.re/docs/plugins.html


## Table of Contents
- [Cutter Plugins](#cutter-plugins)
  - [Table of Contents](#table-of-contents)
  - [Decompilers](#decompilers)
    - [Ghidra Decompiler](#ghidra-decompiler)
    - [RetDec Decompiler](#retdec-decompiler)
    - [r2dec](#r2dec)
  - [Integrations](#integrations)
    - [Jupyter Plugin](#jupyter-plugin)
    - [x64dbgcutter](#x64dbgcutter)
    - [Yara Plugin](#yara-plugin)
    - [AngrCutter](#angrcutter)
    - [Hobbits Plugin](#hobbits-plugin)
  - [Malware Analysis](#malware-analysis)
    - [APT32 Graph Deobfuscator](#apt32-graph-deobfuscator)
    - [Dropshot / StoneDrill Decrypter](#dropshot--stonedrill-decrypter)
    - [Deobfuscate Bitpaymer API Calls](#deobfuscate-bitpaymer-api-calls)
  - [Coverage](#coverage)
    - [CutterDRcov](#cutterdrcov)
    - [Cutter Lighthouse](#cutter-lighthouse)
  - [Enhancements](#enhancements)
    - [CutterRef](#cutterref)
    - [Assembly-reference](#assembly-reference)
    - [Recovering Stack Strings](#recovering-stack-strings)
  - [Graphs](#graphs)
    - [Cutter Deep Graphs](#cutter-deep-graphs)
  - [Misc](#misc)
    - [Cutter plugin templates](#cutter-plugin-templates)
---

## Decompilers

### [Ghidra Decompiler](https://github.com/radareorg/r2ghidra-dec)
This is an integration of the Ghidra decompiler for Cutter and radare2. It is solely based on the decompiler part of Ghidra, which is written entirely in C++, so neither Ghidra itself nor JAVA are required at all and the plugin can be built self-contained.

Due to its quality, the ghidra decompiler plugin is shipped by default in Cutter releases.

**Type**: Plugin  
**Status**: Maintained  
**Reference**: [r2ghidra plugin announced in Cutter v1.9](https://twitter.com/r2gui/status/1169912280001208321)

### [RetDec Decompiler](https://github.com/avast/retdec-r2plugin)
The plugin integrates RetDec decompiler into Cutter.

With the bundled version of RetDec you can decompile the following architectures:

   - 32-bit: Intel x86, ARM, MIPS, PIC32, and PowerPC.
   - 64-bit: x86-64, ARM64 (AArch64).
  
**Type**: Plugin  
**Status**: Maintained  


### [r2dec](https://github.com/wargio/r2dec-js)
r2dec converts the assembly of a function to a Pseudo-C code. Cutter integrates r2dec by default. 

**Type**: Plugin  
**Status**: Maintained  
**Talk**: [How not to write a decompiler - r2con 2018](https://www.youtube.com/watch?v=2siU7B0PjPI)

## Integrations
### [Jupyter Plugin](https://github.com/radareorg/cutter-jupyter  )

This plugin integrates the Jupyter notebook inside Cutter

**Status**: Maintained  

### [x64dbgcutter](https://github.com/yossizap/x64dbgcutter)

Allows the import and export of x64dbg comments and breakpoints in Cutter

**Status**: Maintained

### [Yara Plugin](https://github.com/JannisKirschner/Cutter-Yara-Plugin)

A Cutter plugin to match project with Yara rules at runtime. 

**Status**: Maintained

### [AngrCutter](https://github.com/yossizap/angrcutter)

A plugin that adds dynamic symbolic execution to Cutter's debugger using Angr.

**Status**: Maintained

### [Hobbits Plugin](https://github.com/Mahlet-Inc/hobbits-cutter-plugin)

A plugin that adds [Hobbits](https://github.com/Mahlet-Inc/hobbits) displays to to Cutter.

**Status**: WIP

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

### [CutterRef](https://github.com/yossizap/cutterref)

Cutter Full Instruction Reference Plugin. The plugin will monitor the location for your cursor and display the full documentation of the instruction. At the moment it only supports x86-64, ARM and MIPS 32bit, however adding support for other architectures is relatively easy.

**Type**: Plugin  
**Status**: Maintained

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
