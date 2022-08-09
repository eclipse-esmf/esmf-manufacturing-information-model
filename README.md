# sds-manufacturing-information-model
This repository is dedicated to OMP Semantic Data Structuring Working Group (OMP SDS).

It contains the implementation of the OMP I4.0 Core Information Model described in the linked [Whitepaper](https://open-manufacturing.org/wp-content/uploads/sites/101/2022/05/OMP-SDS-Whitepaper_I4.0_Core_Information_Model.pdf)

The OMP I4.0 Core Information Model provides a common and standardized definition of relevant manufacturing entities, their attributes, and relationships, including their semantic meaning. This enables manufacturing enterprises to efficiently integrate data and provide a clear semantic context, thus reducing the time required to generate insights from the data. Furthermore, the OMP I4.0 Core Information Model allows companies to reuse data-processing applications across heterogeneous data sources as the standardized data model acts as an abstraction layer over the heterogeneous data decoupling data sources from data processing applications.

The OMP I4.0 Core Information Model consists of the following sub-models:
- Physical Asset Ontology
- Equipment Ontology
- Product Ontology
- Parameter Ontology
- Product Segment Ontology
- Process Segment Ontology

The file omp-i40-core.ttl imports the sub-models and defines relationships between entities of different submodels.

The OMP I4.0 Core Information Model supports many different use cases in particular the following: 
- Manufacturing Traceability: The OMP I4.0 Core Information
Model provides  model entities needed to implement manufacturing traceability, starting from
the product model defining a recursive model of the assembled materials to the product
segment model defining entities for the description of the result of manufacturing processes and
individual parts assembly enabling a traceability at both the product definition and product instance level. 
- Manufacturing Process Quality: The I4.0 Core Information model provides the means to describe process chains, including process
result parameters and their tolerances. This provides the basis for process quality monitoring use
cases
- Asset Inventory: The I4.0 Core Information Model provides with the physical asset model a good way to implement
asset inventory use cases in which one needs to know which assets are located in which buildings and
production lines. 
- Production Planning: The I4.0 Core Information model can also be used for production planning. The process model provides
a way to describe the general manufacturing processes, whereas the product segment model provides
ways to describe concrete implementations of the process segments for concrete products.

Contributors:
- Soufiane Ameziane (Teradata Corp.)
- Irlan Grangel-Gonzalez (Robert Bosch GmbH)
- Piotr Janik (Intel Corp.)
- Marcel Keller (Robert Bosch GmbH)
- Felix Loesch (Robert Bosch GmbH) – Coordinator of OMP I4.0 Core Information Model
- Fabio Massari (VMware Inc.)
- Denis Molin (Teradata Corp.)
- Nico Wilhelm (ZF Friedrichshafen AG)
