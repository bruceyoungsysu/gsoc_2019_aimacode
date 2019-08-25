# `aima-python` [![Build Status](https://travis-ci.org/aimacode/aima-python.svg?branch=master)](https://travis-ci.org/aimacode/aima-python) [![Binder](http://mybinder.org/badge.svg)](http://mybinder.org/repo/aimacode/aima-python)


Python code for the book *[Artificial Intelligence: A Modern Approach 4th edition](http://aima.cs.berkeley.edu).* You can use this in conjunction with a course on AI, or for study on your own. We're looking for [solid contributors](https://github.com/aimacode/aima-python/blob/master/CONTRIBUTING.md) to help.



## Structure of the Project

When complete, this project will have Python implementations for all the pseudocode algorithms in the book, as well as tests and examples of use. For each major topic, such as `nlp` (natural language processing), we provide the following  files:

- `nlp4e.py`: Implementations of all the pseudocode algorithms in the 4th edition, and necessary support functions/classes/data.
- `tests/test_nlp4e.py`: A lightweight test suite, using `assert` statements, designed for use with [`py.test`](http://pytest.org/latest/), but also usable on their own.
- `notebooks/chapter22`: The Jupyter notebooks to demonstrate implementation and examples of algorithms. There is a separate notebook for each section in this chapter: `Grammar.ipynb` and `Pasring.ipynb`. For some chapters, there will be a brief introduction in `introduction.ipynb` and implementation of more example applications `nlp_apps.ipynb`.


## Python 3.4 and up

This code requires Python 3.4 or later, and does not run in Python 2. You can [install Python](https://www.python.org/downloads) or use a browser-based Python interpreter such as [repl.it](https://repl.it/languages/python3).
You can run the code in an IDE, or from the command line with `python -i filename.py` where the `-i` option puts you in an interactive loop where you can run Python functions. All notebooks are available in a [binder environment](http://mybinder.org/repo/aimacode/aima-python). Alternatively, visit [jupyter.org](http://jupyter.org/) for instructions on setting up your own Jupyter notebook environment.


## Installation Guide

To download the repository:

`git clone https://github.com/aimacode/aima-python.git`

Then you need to install the basic dependencies to run the project on your system:

`pip install -r requirements.txt`

You also need to fetch the datasets from the [`aima-data`](https://github.com/aimacode/aima-data) repository:

```
cd aima-python
git submodule init
git submodule update
```

Wait for the datasets to download, it may take a while. Once they are downloaded, you need to install `pytest`, so that you can run the test suite:

`pip install pytest`

Then to run the tests:

`py.test`

And you are good to go!


# Index of Algorithms

Here is a index of chapters implemeted for the 4th edition and their corresponding test file and notebook locations. The [aima-pseudocode](https://github.com/aimacode/aima-pseudocode) project describes all the algorithms from the book.

An asterisk next to the file name denotes the algorithm is not fully implemented. 

| **Chapter** |     **Name (in 4<sup>th</sup> edition)**      |                           **File**                           |                          **Tests**                           |                        **Notebook**                        | **Chpater in 3<sup>rd</sup> edition** |
| :---------: | :-------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :--------------------------------------------------------: | :-----------------------------------: |
|      7      |                Logical Agents                 |              [logic4e.py](../master/logic4e.py)              |   [tests/test_logic4e.py](../master/tests/test_logic4e.py)   |                                                            |                   7                   |
|      8      |               FIRST-ORDER LOGIC               |              [logic4e.py](../master/logic4e.py)              |   [tests/test_logic4e.py](../master/tests/test_logic4e.py)   |                                                            |                   8                   |
|      9      |        INFERENCE IN FIRST-ORDER LOGIC         |              [logic4e.py](../master/logic4e.py)              |   [tests/test_logic4e.py](../master/tests/test_logic4e.py)   |                                                            |                   9                   |
|     10      |           KNOWLEDGE REPRESENTATION            |                  No Algorithms to Implement                  |                           No Need                            |                          No Need                           |                  12                   |
|     11      |              AUTOMATED PLANNING               |           [planning4e.py](../master/planning4e.py)           | [tests/test_planning4e.py](../master/tests/test_planning4e.py) |                                                            |                10-11.3                |
|     12      |            QUANTIFYING UNCERTAINTY            |        [probability4e.py](../master/probability4e.py)        | [tests/test_probability4e.py](../master/tests/test_probability4e.py) |                                                            |                  13                   |
|     13      |            PROBABILISTIC REASONING            |        [probability4e.py](../master/probability4e.py)        | [tests/test_probability4e.py](../master/tests/test_probability4e.py) |                                                            |                  14                   |
|     14      |       PROBABILISTIC REASONING OVER TIME       | [reasoning_over_time4e.py](../master/reasoning_over_time4e.py) | [tests/test_reasoning_over_time4e.py](../master/tests/test_reasoning_over_time4e.py) |                                                            |                  15                   |
|     15      |            MAKING SIMPLE DECISIONS            | [making_simple_decision4e.py](../master/making_simple_decision4e.py) |                           No Need                            |                                                            |                  16                   |
|     16      |           MAKING COMPLEX DECISIONS            |                [mdp4e.py](../master/mdp4e.py)                |     [tests/test_mdp4e.py](../master/tests/test_mdp4e.py)     | [notebooks/chapter16-17](../master/notebooks/chapter16-17) |               17.1-17.4               |
|     17      |  MAKING DECISIONS IN MULTIAGENT ENVIRONMENTS  |                [mdp4e.py](../master/mdp4e.py)                |     [tests/test_mdp4e.py](../master/tests/test_mdp4e.py)     | [notebooks/chapter16-17](../master/notebooks/chapter16-17) |            11.4, 17.5-17.6            |
|     18      |            LEARNING FROM EXAMPLES             |           [learning4e.py](../master/learning4e.py)           | [tests/test_learning4e.py](../master/tests/test_learning4e.py) |    [notebooks/chapter18](../master/notebooks/chapter18)    |         18.1-18.6, 18.8-18.11         |
|     19      |             DEEP NEURAL NETWORKS              |      [DeepNeuralNet4e.py](../master/DeepNeuralNet4e.py)      |    [tests/test_deepNN.py](../master/tests/test_deepNN.py)    |    [notebooks/chapter19](../master/notebooks/chapter19)    |                 18.7                  |
|     20      |         LEARNING PROBABILISTIC MODELS         |      Partially Done, need confirmation abut pseudocode       |                                                              |                                                            |                  20                   |
|     21      |            REINFORCEMENT LEARNING             |                 [rl4e.py](../master/rl4e.py)                 |      [tests/test_rl4e.py](../master/tests/test_rl4e.py)      |    [notebooks/chapter21](../master/notebooks/chapter21)    |                  21                   |
|     22      |          NATURAL LANGUAGE PROCESSING          |                [nlp4e.py](../master/nlp4e.py)                |     [tests/test_nlp4e.py](../master/tests/test_nlp4e.py)     |    [notebooks/chapter22](../master/notebooks/chapter22)    |                  22                   |
|     23      | DEEP LEARNING FOR NATURAL LANGUAGE PROCESSING |                         No text yet                          |                                                              |                                                            |                                       |
|     24      |                  PERCEPTION                   |         [perception4e.py](../master/perception4e.py)         | [tests/test_perception4e.py](../master/tests/test_perception4e.py) |    [notebooks/chapter24](../master/notebooks/chapter24)    |                  24                   |
|             |                                               |                                                              |                                                              |                                                            |                                       |

# Index of data structures

Here is a table of the implemented data structures, the figure, name of the implementation in the repository, and the file where they are implemented.

| **Figure** | **Name (in repository)** | **File** |
|:-------|:--------------------------------|:--------------------------|
| 3.2    | romania_map                     | [`search.py`][search]     |
| 4.9    | vacumm_world                    | [`search.py`][search]     |
| 4.23   | one_dim_state_space             | [`search.py`][search]     |
| 6.1    | australia_map                   | [`search.py`][search]     |
| 7.13   | wumpus_world_inference          | [`logic.py`][logic]       |
| 7.16   | horn_clauses_KB                 | [`logic.py`][logic]       |
| 17.1   | sequential_decision_environment | [`mdp4e.py`][../master/mdp4e.py] |
| 18.2   | waiting_decision_tree           | [`learning4e.py`][../master/leanrning4e.py] |

<!---Reference Links-->

[agents]:../master/agents.py
[csp]:../master/csp.py
[games]:../master/games.py
[grid]:../master/grid.py
[knowledge]:../master/knowledge.py
[learning]:../master/learning.py
[logic]:../master/logic.py
[mdp]:../master/mdp.py
[nlp]:../master/nlp.py
[planning]:../master/planning.py
[probability]:../master/probability.py
[rl]:../master/rl.py
[search]:../master/search.py
[utils]:../master/utils.py
[text]:../master/text.py

