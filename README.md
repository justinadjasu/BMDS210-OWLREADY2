# BMDS210-OWL2READY: Building OWL Ontologies with Python

An interactive Jupyter notebook that teaches OWL ontology construction using [owlready2](https://owlready2.readthedocs.io/). Students build a grocery/cookie product ontology step-by-step, mirroring the Protege-based class exercise in Python.

## Prerequisites

- **Python 3.7+**
- **Java** (required for the HermiT reasoner in Section 9)
- Prior experience with Protege and basic OWL concepts

## Setup

```bash
# Clone the repository
git clone <repo-url>
cd BMDS210-OWLREADY2

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook owl2_cookie_ontology.ipynb
```

## Learning Objectives

By the end of this notebook, you will be able to:

1. Create and manage OWL ontologies programmatically using owlready2
2. Declare classes, class hierarchies, and disjoint axioms
3. Parse structured data to build large taxonomies automatically
4. Add annotations (labels, definitions, links) in multiple languages
5. Define object and data properties with domains, ranges, and characteristics
6. Model class restrictions (existential quantification, unions)
7. Use property chains and transitivity for inference
8. Create defined classes and run automatic classification with a reasoner
9. Create individuals with property assertions
10. Query ontologies using search and SPARQL
11. Export ontologies for use in Protege and other tools

## Notebook Sections

| # | Section | OWL Concepts |
|---|---------|-------------|
| 1 | Setup & Creating an Ontology | `get_ontology()`, IRI, `with onto:` |
| 2 | Classes and Class Hierarchy | SubClassOf, class inheritance |
| 3 | Building the Ingredient Taxonomy | Dynamic class creation, parsing structured data |
| 4 | Disjoint Classes | AllDisjoint, open-world assumption |
| 5 | Annotations | rdfs:label, skos:altLabel, skos:definition, foaf:depiction |
| 6 | Object Properties | ObjectProperty, domain, range, sub-properties |
| 7 | Modeling Cookie Ingredients | `someValuesFrom` restrictions, unions |
| 8 | Property Characteristics | Transitivity, property chains |
| 9 | Defined Classes & Reasoning | `equivalent_to`, `sync_reasoner()` |
| 10 | Individuals | Named individuals, property assertions |
| 11 | Data Properties & Nutrition | DataProperty, literal values |
| 12 | Querying & Exporting | `onto.search()`, SPARQL, `onto.save()` |

## Repository Structure

```
BMDS210-OWLREADY2/
├── README.md
├── requirements.txt
├── data/
│   ├── ingredients.txt          # Ingredient taxonomy (parsed in Section 3)
│   └── Cookie-Products.pdf      # Cookie product reference sheets
├── ontologies/                  # Save your ontology files here
├── owl2_cookie_ontology.ipynb          # Student notebook
└── owl2_cookie_ontology_solutions.ipynb # Solutions (instructor use)
```

## Verifying Java for Reasoning

Section 9 uses the HermiT reasoner, which requires Java. To check:

```bash
java -version
```

If Java is not installed, the notebook will skip reasoning exercises and explain what the expected output would be.

## References

- [owlready2 documentation](https://owlready2.readthedocs.io/)
- [OWL 2 Web Ontology Language Primer](https://www.w3.org/TR/owl2-primer/)
- [Protege](https://protege.stanford.edu/)