Digital Pathway Curation (DPC)
+++++++

Concepts
============

The Digital Pathway Curation (DPC) pipeline was designed and tested to answer the following questions:  

1. How can we demonstrate that a molecular biological pathway is related to a disease?  
2. How can we demonstrate whether a set of molecular biological pathways, calculated beyond the default cutoffs using GSEA, is related to a disease case?  
3. How can someone query Gemini in a natural language and retrieve reproducible answers without hallucinations?  
4. How can we quantify AI answers, make inferences, and calculate statistics?  
5. How can we demonstrate that Gemini delivers reproducible results using a set of systems biology questions?  

  
Regarding the relationship between a set of molecular biological pathways and a disease, we also considered the following questions:  

1. How can we calculate the accuracy of the answers provided by Gemini, PubMed, and humans?  
2. How do we uncover FP and FN in a given enriched table?  


DPC was written in Python and integrated with the Gemini AI tool and PubMed through their web services. It stores an Ensemble of questions and answers to perform counts, comparisons and statistical analyses.

In this study, we defined and measured the concepts of consensus, reproducibility, crowdsourcing, and accuracy. Using a smaller dataset with two disease cases, we calculated crowdsource consensus (CSC) and assessed the accuracy of each of the "3 Sources": Gemini, PubMed, and human evaluations. Our findings indicate that Gemini's consensus accuracy outperformed the PubMed and human accuracies. Additionally, using Gemini, we could uncover False Positive (FP) and False Negative (FN) pathways related to each disease case and confirm the True Positive (TP) and True Negative (TN) pathways.  


DPC aims to  

   1. calculate Gemini (LLM) reproducibility  
   2. calculate the consensus through the 4DSSQ  
   3. merge the "3 Sources" to calcualte the CSC  
   4. calculates each source accuracy.  



Options
=======


Goal
--------

Ensemble
---------------


Consensus
-----------------

3Sources
-----------------

CSC
-----------------


Results
-----------------


Conclusions
-----------------


