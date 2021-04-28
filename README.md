
<!-- <link rel="stylesheet" type="text/css" media="all" href="custom-style.css" /> -->

<link rel="stylesheet" media="screen" href="https://fontlibrary.org//face/aileron" type="text/css"/>

![Data Product Elements](./data_product.svg)

<!-- TOC -->
- [Definitions](#definitions)
    - [1. Roles](#1-roles)
    - [2. Data terms](#2-data-terms)
    - [3. Storage Architectures](#3-storage-architectures)
    - [4. Types of storage](#4-types-of-storage)
    - [5. Data Processing](#5-data-processing)
- [Data Curation Projects](#data-curation-projects)
<!-- /TOC -->

# The Modern Data Product Company

A data product company is a firm that provides a service to clients by easing the process of going from data to knowledge which informs actions. Data is the first element in a five step sequence to value known as the DIKAR model:

Data → Information → Knowledge → Action → Results

A data product company takes data and transforms the data into information. The information should be presented in such a way that it easily produces knowledge for the user.<sup id="a1">[1](#f1)</sup> The goal of a data product company is to efficiently move from data to the conditions for knowledge acquition in the user base. For a data product with a subscription fee, users are synonomous with clients.<sup id="a1">[2](#f1),[3](#f1)</sup>

A data product is a combination of three elements:

1. Data Processing
2. User Interface
3. Data Curation

Data curation<sup id="a1">[4](#f1)</sup> carries its own unique status in this case, because data has an abstract value above and beyond the technical details of the systems that store it and the measurement schemes used to create records.

## Definitions

The most critical terms of data product companies are:

Business Logic
:  the technical elements of a system that provide unique value to users and/or customers.

Business Purpose
: specific processes by which the business logic is utilized for value creation.

Business Case
: a seperable domain of one or more business purposes which define value for clients.

Value
: utility, with a homomorphism to USD, derived from providing goods or services that ameliorate the human condition. A data product must provide value to clients, which is captured by the business as revenue and, ideally, profit.

### 1. Roles

Data Owner
: accountable for data quality and fitness.

Data Steward
: responsible for data quality and fitness. Alternate titles: Custodian, Curator, Data Mangement Head, Bill.

Data Engineer
: responsible for the technical implementation of data curation

Data Scientist
: responsible for implementation of business logic from data

Database Administrator
: responsible for the deployment and maintenance of storage mechanisms.

Software Engineer
: responsible for building applications.

DevOps Engineer
: responsibile for deploying applications and infrastructure in a infrastructure-as-code model. Responsible for both customer facing tools, and supporting development tools for engineers and data scientists.

```cpp
//TODO: add roles for infrastructure, software engineering, project management, other things.
```

### 2. Data terms

Datum
: a quantified record. 

Data
: the plural of datum. Both data and it's singular form are defined by context and are renormalized by scale. For example, the fact that characters have a byte code which defines how the character is stored in a digital file is immaterial for consideration of a whole document analysis of sentiment.

Data set
: A collection of records (or subset of a larger collection) utilized for finding information.

Record
: an observation of the world as a quantified measurement. This is inclusive of digital textual records.

Source(s) of records
: both the technical and institutional source from which records are captured.

Data retrieval
: accessing data by means of a query from storage.

Content
: all data is content and all content is data.

Data set status
: the current useability and availability of a given data set, according to a trinary logic of medal status. Thus:
  - Bronze: Data is available, but experimental, exploratory, and unverified and undocumented.
  - Silver: Data is available, documentation is somewhat available, and the process of preparing it for final storage in a production-worthy context has begun.
  - Gold: Data is available, fully documented, and available for production use.

Publication
: when a dataset is available for query by a production system.

### 3. Storage Architectures

Storage
: refers to both the abstract and tangible elements of storing records. The type of storage is defined by the business case and logic.

Database (general)
: where a collection of records is kept for querying.

Database (technical)
: a software solution for storing records for fast querying. Includes specific tools like PostgreSQL, Neo4j, MongoDB, etc..

Archive
: a complete and final collection of records from a source.

Data warehouse
: a federated or consolidated system and location of multiple collections of records. A form of "Cold Storage."

Data Lake
: a loosly consolidated, federated, or completely heterogenous collection of records accessible via multiple retreival mechanisms. A form of "Cold" or "Lukewarm" storage.

### 4. Types of storage

Hot Storage
: queries return data in human-scale time durations. Typically under five seconds.

Cold Storage (alternate adjective Lukewarm)
: queries return data in slower time frames. Can be a data lake or data warehouse, depending on the speed of queries and the degree of integration between records and sources, schematically.

Deep Freeze storage
: where final copies for later audit are stored. Last stop before deletion in a data lifecycle.

### 5. Data Processing

Data Ingest
: all technical and business processes up to, but not including, analytics for a business purpose.

Data Capture
: the process where batches of records are brought into a collection of records from an external source.
    - Alternate: extraction in an Extract-Transform-Load (ETL) model.<sup id="a1">[5](#f1)</sup>

Data Transformation(s)
: any data cleaning, repackaging, indexing, validation, verification, or quality assurance that occurs before a critical business logic.
    - Alternate term: pre-processing.

Trigger
: both the conditions under and the mechanism for a registered data capture event.

## Data Curation Projects

- Identification
    - data owner confirms choice(s) of data set (or content sets, generally)
    - steward and owner agree upon publication requirements
- Validation
    - Steward confirms fitness for purpose with sample(s)
- Archiving
    - Historical data ingestion, processing, integration, and storage
- Capture
    - create a reoccuring or triggered process for new records
- Processing
    - prepare data for analysis (pre-processing)
    - run business logic against prepared data, post-capture
- Publication
    - store data for retreival
    - confirm necessary documentation available
    - data owner confirms the status of data and publication mechanisms

------

<b id="f1">1</b> An AI-product company, by comparison, takes data and produces actions. An AI system creates a closed-loop system where results are measured and fed back into the system as data. [↩](#a1)

<b id="f1">2</b> N.b. For a firm like Facebook, the user base and client base are not the same. Facebook clients are advitisers, and the users are human chattel. [↩](#a1)

<b id="f1">3</b> This document will attempt to use the term "client" when referring to applications that run on user-owned hardware. [↩](#a1)


<b id="f1">4</b> Absent this third element, a company is a data _storage_ company and not a data _product_ company. [↩](#a1)

<b id="f1">5</b> This nomenclature is to be avoided if the data product is using text documents, as you have two senses of the word "extract" in that case. In an ETL, you are capturing the data by "extracting" it from the data store where you initally find it. With NLP work, you also need to "extract" the text from a document for processing. In the latter case, this occurs during pre-processing. [↩](#a1)