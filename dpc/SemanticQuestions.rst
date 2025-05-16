Semantic Questions
++++++++++++++++++++

One of the DPC goals is to evaluate Gemini's semantic capabilities. To address this goal, we generated four different but semantically similar questions to perform this task. These questions will broadly (“a pathway related to”) or specifically (“has a strong relationship to”) ask whether a particular pathway is involved in modulating a disease case. Additionally, the second variation focuses on whether the relevant findings can be found on PubMed by adding “<according to PubMed>”.

The resulting answers are categorised as 'Yes,' 'Possible,' 'Low evidence,' or 'No,' being counted and summarised in runs, models, cases, and pathway groups. 

To summarise, given the Ensemble or the MSD dataset, we formulated the 4DSSQ for each pathway by merging the pathway name and the disease case or subtype to be part of the query template. This task is performed for each disease case and LLM model at least twice (runs >= 2).

Below, we present the basic semantic query format:

“Answer in the first line: Yes, Possible, Low evidence, or No, and explain: Is <pathway> <related or have a strong relationship> to <disease> <severity> <age> <gender> <according to PubMed>? Context: <contextualise the disease> + <contextualise the pathway>.”

