# sds-manufacturing-information-model-private
This private repository is dedicated to OMP Semantic Data Structuring Working Group (OMP SDS)
and contains the implementation of the OMP I4.0 Core Information Model described in the linked [whitepaper](https://open-manufacturing.org/wp-content/uploads/sites/101/2022/05/OMP-SDS-Whitepaper_I4.0_Core_Information_Model.pdf)

The OMP I4.0 Core Information Model provides a common and standardized definition of relevant manufacturing entities, their attributes, and relationships, including their semantic meaning. This enables manufacturing enterprises to efficiently integrate data and provide a clear semantic context, thus reducing the time required to generate insights from the data. Furthermore, the OMP I4.0 Core Information Model allows companies to reuse data-processing applications across heterogeneous data sources as the standardized data model acts as an abstraction layer over the heterogeneous data decoupling data sources from data processing applications.

The OMP I4.0 Core Information Model consists of the following sub-models:
- Physical Asset Ontology
- Equipment Ontology
- Product Ontology
- Parameter Ontology
- Product Segment Ontology
- Process Segment Ontology

The file omp-i40-core.ttl imports the sub-models and defines relationships between entities of different submodels. 
