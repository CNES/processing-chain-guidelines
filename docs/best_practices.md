Best practices
=====

Version and Tag
---------------

The version management for the evolution of the processing chain must comply with [semver.org](https://semver.org/lang/fr/). 
The version tag must be applied to a development branch containing the algorithm, the Docker image, and all standard rules described in the attached document.

| Digit | Description | Definition / Example |
| :--- | :--- | :--- |
| **First Digit** | Major Version | There are non-backward compatible changes. A set of minor changes and fixes. |
| **Second Digit** | Minor Version | There are additions of backward-compatible features. |
| **Third Digit** | Patch Version | There are backward-compatible anomaly corrections.  |

---

Configuration Management
------------------------

#### Readme
A Readme written in Markdown at the root of the GIT project must allow for a quick overview of the chain.
* **Documentation Link**: Link to the documentation hosted on readthedocs.com.
* **Title and Badge**: Project name and indicators (build status, version, license).
* **Short Description (Pitch)**: One to two sentences maximum on the "what" and the "why".
* **Quick Installation**: A single command line (e.g., `npm install` or `pip install`).

#### GIT Workflow
The project should follow the Git Flow workflow: [https://git-flow.readthedocs.io/fr/latest/presentation.html](https://git-flow.readthedocs.io/fr/latest/presentation.html)

---

Packaging
---------

#### Image Format
Images must be in OCI container format (Docker type).

#### CWL Description of the Process
A CWL file containing a minimal description of your process must be provided, including:
* **Input Data**
* **Processing**
* **Output Data**

---

Documentation
-------------

Documentation must be managed within the GIT project and made publicly available (e.g., Readthedocs, Jupyterbook, Sphinx).
A template is provided to help you initialize your documentation here:

#### Documentation Content
* **Process Description Template (v3.0)**: Standard template for describing a processing chain.
* **Dataflow Document**: A document outlining the data flow.

---