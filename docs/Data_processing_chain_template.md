# Processing Chain Description Template

#### Interface Elements for Chain Integration: `<chain_name>`

#### Process: `<process_name>`

* **Description**
    * TODO: Functional description of what the process does.
    * TODO: Link to the process documentation (README, user manual, etc.).
* **Application Domain (Granule)**
    * TODO: Description of the processing granule.
* **Scheduling and Triggers**
    * For continuous processing, specify the expected periodicity and the triggering events.

#### Inputs
**Data**
| Data Type Name | Cardinality | Selection Criteria |
| :--- | :--- | :--- |
| `<data_type_1>` | 1 | Trigger |
| `<data_type_2>` | 1 | Most recent |
| `<data_type_3>` | 1..n | Files intersecting over the period XXX |
| ... | 3 | The last 3 files on the same tile |

#### Outputs
**Data**
| Data Type Name | Cardinality |
| :--- | :--- |
| `<data_type_4>` | 1 |
| `<data_type_5>` | 0..n |
| ... | ... |

#### Return Codes
* **0**: OK, execution completed successfully.
* **1**: KO, execution failed.
* **2, 3, 4, ...**: Potential other error cases or warnings (usually described in the process user documentation).

#### Log Format
The preferred log format should ideally follow this structure:
`<date> <Message_Classification>:<Class_Name>::<Method_Name>:<userMessage>`

| Field | Description |
| :--- | :--- |
| `date` | Format: `YYYY-MM-DDThh:mm:ss.sss` |
| `Message_Classification` | `ERROR`, `WARNING`, `INFO`, `DEBUG` |
| `Class_Name` | Can contain the chain name, executable name, or Python module |
| `Method_Name` | Can contain the name of the method or step currently executing |
| `userMessage` | The body of the message |

#### Required Resources
| Resource Type | Quantity |
| :--- | :--- |
| Number of CPUs | ? |
| RAM Amount | ? |
| Input Disk Space (total size of all input data) | ? |
| Working Disk Space | ? |
| Output Disk Space (total size of all output files) | ? |
| Execution Time | ? |
| Data Waiting Time (if not all data is present at trigger time) | ? |

#### Data Types
**`<data_type_1>`**
* **Description**: TODO: description of the data type: content, origin, usage... Where to find the data?
* **Granule**: TODO: A granule is a temporal and/or geographical identification object. Some types are universal (e.g., `SEGMENT` for a period or `DAY` for a day). Others are specific, such as `S2_TILE` (geographical only, e.g., `S2T29LQK`) or `S2_TEMPORAL_TILE` (tile associated with a date, e.g., `S2TT12HWG_20211018-122314-612`).
* **Nomenclature**: 
    * **Regular Expression**: TODO: regex to identify a file corresponding to the data type, with explanations of its components.
    * **Example(s)**: TODO: one or more examples of filenames corresponding to the data type.