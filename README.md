# pnmcc-models-2018

Extracted models + oracles where available based on [MCC'2018](http://mcc.lip6.fr) competition.

This project automatically extracts and produces separate archives for each model of the competition, along with "oracle" files that describe the expected values as computed in "expected" by consensus among the competing tools in 2018.

The files are distributed here : [Generated Page](https://yanntm.github.io/pnmcc-models-2018) as 

* a set of individual model instances and formulas, packaged as a tar.gz per instance.
* a single archive [oracle.tgz](https://yanntm.github.io/pnmcc-models-2018/oracle.tar.gz) containing all non ambiguous property verdicts (no ? question mark in the raw results of MCC2018) and a set of *StateSpace* examination verdict files from previous years (these files cannot be directly generated from raw results of the contest, so I'm reusing some collected from previous editions).We additionally generated "GlobalProperties" files based on the 2018 "ReachabilityDeadlock" to be compliant with this updated category in 2019.  

The intent is to use these files for development and regression testing of any competing tool.
 
## Content of oracle files

The oracle files are simply a "virtual" trace of a correct answer of a tool, in expected MCC format. 
The first line defines the model instance and examination, then the results are provided with "ORACLE2018" as technique used.

e.g.

```
./runatest.sh ARMCacheCoherence-PT-none ReachabilityFireability
FORMULA ARMCacheCoherence-PT-none-ReachabilityFireability-00 FALSE TECHNIQUES ORACLE2018
FORMULA ARMCacheCoherence-PT-none-ReachabilityFireability-01 FALSE TECHNIQUES ORACLE2018
FORMULA ARMCacheCoherence-PT-none-ReachabilityFireability-02 TRUE TECHNIQUES ORACLE2018
FORMULA ARMCacheCoherence-PT-none-ReachabilityFireability-03 FALSE TECHNIQUES ORACLE2018
FORMULA ARMCacheCoherence-PT-none-ReachabilityFireability-04 FALSE TECHNIQUES ORACLE2018
FORMULA ARMCacheCoherence-PT-none-ReachabilityFireability-05 TRUE TECHNIQUES ORACLE2018
FORMULA ARMCacheCoherence-PT-none-ReachabilityFireability-06 FALSE TECHNIQUES ORACLE2018
... file shortened...
```

  
