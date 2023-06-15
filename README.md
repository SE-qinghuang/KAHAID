# KAHAID
Due to the limitations of GitHub repository capacity (individual files must not exceed 25MB), you can download the complete code using the following link: https://drive.google.com/drive/folders/1VlZDWIpth_VM4gJXC0E1ljIrueGUCt9P?usp=sharing.
This code is part of the reproducibility package for the paper "Answering Uncertain, Under-Specified API Queries Assisted by Knowledge-Aware Human-AI Dialogue".

It consists of four folders:

* data/ - Some dependency files used by the KAHAID system.

* experiment/ - Scripts to run and evaluate ZaCQ, such as RQ1, RQ2, RQ3, RQ4.

* intent_clarification/ - Implementation of the KAHAID system, including the construction of a knowledge graph and the implementation of the human-AI dialogue process.

* output/ - This folder stores the key data inputs and outputs for each stage of KAHAID, including APIs extracted from API documentation along with their descriptions, extracted entities and relationships, and data required for the human-machine interaction process.

# Setup
In order to set up the KAHAID system and implement the human-AI dialogue service, you need to follow the following steps:
1. Install the Python environment required to run the code. The version of Python interpreter we are using in this system is 3.7.1.

`pip install -r requirement.txt`

2. Construct and load the knowledge graph.

For Linux or Mac devices, follow these steps:

```
cd intent_clarification/import2neo4j/neo4j-import
sh import.sh
sh run.sh
```

For Windows devices, follow these steps:

```
cd intent_clarification/interaction
import2neo4j.py
```

3. Run the Human-AI dialogue process

```
cd intent_clarification/interaction
run.py
```

# Evaluation
To evaluate the KAHAID, you may use the following:

RQ1 and RQ2
```
cd experiment/RQ1_RQ2
evaluation_mrr_map.py
evalutation_precision_recall.py
```

RQ3
```
cd experiment/RQ3_RQ4
cd RQ3
evaluate_exp.py
execute_exp.py
```

RQ4
```
cd RQ4
get_data.py
execute_exp.py
```

# Appendix
In addition, we also provide the Appendix.pdf, which contains more details to supplement the paper.This file includes the following:

In this document you can view the following content:

* MOTIVATING EXAMPLE
* Knowledge Extraction
* Semantic Roles Annotation Details
* Syntactic Roles Annotation Details
* Template that generated according to the Aspects
* RQ: What is the Accuracy of Entity and Relation Extraction for Constructing API Behavior KG?
* User Study
