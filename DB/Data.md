- Data can be stored in different formats, with various encodings e.g. ASCII, UCS, UTF-8. 
- Data is often created for 3 reasons: Backup, Input and Consumption. 

**Types of data:
- [[Structured data]]
- [[Unstructured data]]
- [[Semi-structured data]]

**Types of databases:
- [[Relational database]]
- [[Document oriented database]]
- [[Object oriented database]]

**Data Manipulation** - Shaping the data to answer question. 
- *Hierarchical indexing:*
	- Grouping data into parents and child groups. 
	- Partial indexing allows to select subsets of data. 
- *Merging datasets:*  Allows us to find useful patterns.
- *Pivoting*: Reshaping data to examine from different perspectives. 

**Data Cleaning** - Choose which parts of the data are relevant. 
- *Remove missing and duplicates:* Analyse missing data to find collection problems. 
- *Replace values:* Fill values with NaN or 0 (constants) to avoid errors and bugs. 
- *Rename axis:* Use map and rename. 
- *Remove outliers*: Make use of array operations. 

**Data analysis:**
- Split data into groups
- Apply calculations
- Combine results. 

**ERD**
- Entity relationship diagram
- One to one - I - O 
- One to many - User and Collaborators - Crows feet
- Many to one - Many breeds, but dog can only have one - Reverse crows feet
- Many to many - Try to avoid, try use a bridge table
- Self referencing. 
- Parent child. e,g product categories. 

Identify entities
Define relationships
Specify attributes
Establish primary keys
Draw ERD

*Entity*

*Relationship*
Connections between entities

*Attributes*
Characteristics of entity

*Key*
Unique identifier for each identity
Every table needs to have a key
Composite keys - 2 combined attributes that create uniqueness between them. 

**Benefits**
- Clarity
- Blueprint for implementation
- Identification of issues
- Planning and analysis
- Communication. 
## Normalisation
**Normal Forms**
Focus on the first 3 forms
- 1st normal form
	- Atomic values.
	- Move repeating attributes to new table
	- Identify repeating fields
	- Put those in new table with key from UNF
- 2nd normal form
	- Non key attributes dependent on primary key. 
	- Eliminating dependencies. 
	- Remove partial key demendencies
	- Any key that depends on part of key form value . 
- 3rd normal form
	- Tables with 0 or only one non key attribute
	- Move copy of attribute they are dependent on 
- Boyce-Cood normal form
- 4th normal form
- Fifth normal form
- 0 Normal form

**Importance of Normalisation**
- Data integrity
- Efficient storage and retrieval
- Simplified updates and maintenance
- Flexibility and scalability
- Improved query performance
- Easier understanding of data models

Atomic - Cannot be broken down further.