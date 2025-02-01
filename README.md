This repository contains a Python implementation to classify grammars according to the Chomsky hierarchy. The program reads production rules for a grammar and classifies it into one of the four Chomsky hierarchy types:

Type 3: Regular Grammar
Type 2: Context-Free Grammar
Type 1: Context-Sensitive Grammar
Type 0: Recursively Enumerable Grammar
The code uses basic regular expressions and string manipulation to evaluate the form of the given production rules.

Overview
The Chomsky hierarchy classifies grammars into four types based on the form of their production rules:

Type 3: Regular Grammar – All rules must be of the form A -> α, where A is a non-terminal, and α is a string of terminals.
Type 2: Context-Free Grammar – All rules must be of the form A -> γ, where A is a non-terminal, and γ is a string of terminals and/or non-terminals.
Type 1: Context-Sensitive Grammar – All rules must be of the form αAβ -> αγβ, where the length of the left-hand side is less than or equal to the length of the right-hand side.
Type 0: Recursively Enumerable Grammar – There are no restrictions on the form of the production rules.
Requirements
To run the code in Google Colab, you don’t need to install anything locally since Colab already supports Python and the required libraries.

The libraries used in the project:

re: For regular expression matching.
You can install the required libraries with the following code if you're working locally:

bash
Copy
Edit
!pip install re
Files
grammar_classification.ipynb: The main Jupyter notebook where the grammar classification code is implemented.
README.md: This file, providing an overview of the project.
How It Works
The code contains functions to classify grammars based on the rules you input:

Regular Grammar Check: The grammar is considered regular if every rule has the form A -> α, where A is a non-terminal and α is a string of terminals.
Context-Free Grammar Check: The grammar is considered context-free if every rule has the form A -> γ, where A is a non-terminal and γ is a string of terminals and/or non-terminals.
Context-Sensitive Grammar Check: The grammar is context-sensitive if every rule has the form αAβ -> αγβ, and the length of the left-hand side (αAβ) is less than or equal to the length of the right-hand side (αγβ).
Recursively Enumerable Grammar Check: All grammars are recursively enumerable (Type 0), so they automatically pass this check.
The program will classify the grammar and output the type it belongs to.

Example
Input grammar:

rust
Copy
Edit
S -> aA
A -> bB
B -> aS
S -> ε
Output:

css
Copy
Edit
The grammar belongs to: Regular Language (Type 3)
Running the Code in Google Colab
To run the code in Google Colab, follow these steps:

Open the grammar_classification.ipynb notebook in Google Colab.
Execute each cell in the notebook sequentially.
When prompted, enter the grammar production rules, one rule per line.
Type done when you're finished entering the grammar rules.
The notebook will output the classification of the grammar.
Example Usage
python
Copy
Edit
Enter your grammar production rules. Type 'done' when finished:
S -> aA
A -> bB
B -> aS
S -> ε
done
The grammar belongs to: Regular Language (Type 3)
License
This project is licensed under the MIT License. 

This README is structured for a Google Colab-based workflow where users can run the provided Jupyter notebook and interact with it by entering grammar rules.

AUTHOR

ELURU POOJITH KUMAR REDDY
