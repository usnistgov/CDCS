# Configurable Data Curation System (CDCS)


The Configurable Data Curation System (CDCS) or Curator developed at NIST provides a means for capturing, sharing, 
and transforming unstructured data into a structured format based on XML or JSON Schemas.

The CDCS can be viewed as a "loading dock" for scientific data. It serves as means to enable the collection and 
dissemination of structured scientific data. It can be applied to any area and is agnostic to the type of data. 
“Curated” data is amenable to transformation to other formats such as those used by existing computational tools. 
The data are organized using user-selected community-developed templates encoded in XML or JSON Schemas used to create data 
documents that are indexed in a database (PostgreSQL, SQLite, MongoDB).

The CDCS is implemented in Python, with the Django framework. It provides a 
Representational State Transfer (REST) API that allows other software to directly interact with it over a network. 
CDCS functions are available via the API, allowing for full automation.

More information regarding the CDCS can be found on the [CDCS Website](https://cdcs.nist.gov).

## Context

The CDCS originated from the Materials Genome Initiative (MGI). In the MGI, there may be collections of 
incompatible data often represented in diverse formats. This is a challenge to the distributed research goal envisaged 
by the MGI. The ability of the CDCS’ underlying XML/JSON format to be transformed into virtually any other format 
using standard tools, gives the CDCS the ability to serve as a data source for a wide variety of existing materials 
informatics efforts that can span across projects, groups, and organizations. Each project, group, or organization can 
run as many CDCS instances as needed. Individual CDCS repositories can be interconnected for federated searches and data sharing.


## Getting started

### CDCS Projects

Two types of systems are usually implemented using the CDCS:
- **Data repositories**, such as the Materials Data Curation System ([MDCS](https://github.com/usnistgov/MDCS)), that allows
for the curation and dissemination of materials dataset in an online repository using predefined templates.
- **Data registries**, such as the NIST Materials Resource Registry ([NMRR](https://github.com/usnistgov/nmrr)), that allows for the registration of 
materials resources, bridging the gap between existing resources and the end users. 
The Registry functions as a centrally located service, making the registered information available for research 
to the materials community.

### Deployment

The CDCS can be deployed using several methods:
- with Docker / Docker Compose (see [CDCS Docker](https://github.com/usnistgov/cdcs-docker)),
- with Kubernetes / Helm (see [CDCS K8s](https://github.com/usnistgov/cdcs-k8s)),
- natively (see for example the [MDCS installation instructions](https://github.com/usnistgov/MDCS/blob/develop/docs/mdcs-install-pypi.md)),
- for development (see for example the [MDCS development setup notes](https://github.com/usnistgov/MDCS/blob/develop/docs/mdcs-dev-setup.md)).


### Tools

The CDCS provides a REST API to programmatically access its features.
A documentation of the different REST endpoints is available
at the `/api/docs` url of a deployed system. The REST API can be accessed by
any HTTP library such as [curl](https://curl.se) or [python requests](https://requests.readthedocs.io/en/latest/).
A python library has also been implemented to facilitate the interactions with the CDCS REST API: [PyCDCS](https://github.com/usnistgov/pycdcs)


## Disclaimer

[NIST Disclaimer](https://www.nist.gov/disclaimer)
