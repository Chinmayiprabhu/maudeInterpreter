### Introduction

PAOl is Privacy aware language that proposes an integration of privacy concepts into a core active object language to explore how language semantics can be used to ensure personal data handling by design and default. In this repository we provide formalisation  of PAOL semantics and Model checking Compliance property. 

### Download and Run:

To run and test the code, the rewriting tool [http://maude.cs.illinois.edu/][Maude version 3.1] is needed. To download, please refer to the documentation for installation instructions and further information., it's downloadable free of charge from the University of Illinois.



### PAOL's formalization in Maude

PAOL data types and Interpreter is specified in the file PAOLInterpreter.maude. Compliance formula are specified in the file PAOLModelchecker.maude. Example scenario from the paper is given as working configuration in the file workingconfig.maude.

#### Instructions

Download Maude 3.1 and the files listed on /maude in the same directory. After installing Maude, to run the model checker and test the properties for our hygienic program, use the following commands in your terminal:

sudo ./maude.darwin64
load PAOLInterpreter.maude
load workingconfig.maude
load model-checker.maude
load PAOLmodelchecker.maude
