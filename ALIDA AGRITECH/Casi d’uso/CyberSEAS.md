
> ## CyberSEAS

<figure>
<img src="CyberSEAS/image_044_image6.jpg" style="max-width: 50%; height: auto;"/>
</figure>

> *Figure 2.2.1: CyberSEAS Project Logo*


| **Type** | **Start Date** | **End Date** |  **ENG Grant Amount** |  **PM** |
| --- | --- | --- | --- | --- |
| FML | 1 Octo 2021 | 30 Sept 2024 | €722264,38 | x |

> *Table 2.1.4: CyberSEAS Project Info*


### Partners

<figure>
<img src="CyberSEAS/image_045_image7.jpg" style="max-width: 75%; height: auto;"/>
</figure>

> *Figure 2.2.2: CyberSEAS Partners Logo*


| **Partner Name** | **Acronym** | **Country** |
| --- | --- | --- | 
| Engineering Ingegneria Informatica S.p.A.   | ENG         | Italy       |
| Consorzio Interuniversitario Nazionale per l'Informatica  | CINI        | Italy       |
| Airbus Potect GMBH                            | AIRP        | Germany     |
| Fraunhofer Gesellschaft zur Fonderung der Angewandten Forschung EV     | FGFR        | Germany     |
| Guardtime                                     | GT          | Estonia     |
| Ikerlan S. COOP                               | IKS         | Spain       |
| Informatika Informacijske Storitve in Inzeniring DD        | IIS         | Slovenia    |
| Rheinisch-Westfaelische Technische Hochschule Aachen | RWTG        | Germany     |
| Software Imagination &Vision SRL              | SIV         | Romania     |
| Software Quality System SA                    | SQS         | Spain       |
| STAM SRL                                      | STAM        | Italy       |
| Synelixis Lyseis Pliroforikis                 | SLPA        | Greece      |
| Automatismou & Tilepikoinonion Anonimi Etairia       | ATAE        | Greece      |
| Wing ict Solutions Technologies Pliroforikis kai Epikoinonion Anonimi Etaireia  | WSTP        | Greece      |
| Ziv Aplicaciones y Tecnologia SL              | ZAT         | Spain       |
| Comune di Berchidda                           | CDBE        | Italy       |
| Comune di Benetutti                           | CDBT        | Italy       |
| Eles doo Operater Kombiniranega Prenosneg in Distribucijskega Elektroenergetskega Omrezja | EOKP        | Slovenia    |
| Petrol Slovenska Energetska Druzba dd  Ljubljana         | PSED        | Slovenia    |
| Akademska in Raziskovalns Mreza Slovenije     | ARMS        | Slovenia    |
| Hrvatski Operator Prijenosnog Sustava D.D.  | HOPS        | Croatia     |
| Enerim OY                                     | ENER        | Finland     |
| Elektrilevi OU                                | ELL         | Estonia     |
| Compania Nationala de Trasport al Energiei Electrice Transelectrica SA   | CNTE        | Romania     |
| Centrul Roman al Energiei                     | CRE         | Romania     |
| Timelex                                       | TML         | Belgium     |
| Operato DOO                                   | OPER        | Slovenia    |
|                                               |             |             |

> *Table 2.2.1: CyberSEAS Partners*

### Overview

The benefits of using *Federated Machine Learning (FML)* include the
ability to train models on distributed data without having to centralize
them, ensuring data privacy and reducing the risk of transmitting
sensitive information.

Within the CyberSEAS project we worked on a use case in the field of
*Social Engineering Detection*, in particular in training intelligent
models to detect fraudulent emails from the analysis of its text.

The FML therefore allowed us to create a *text classification* model for
emails in a collaborative and secure way, without compromising the
confidentiality of the personal data contained in the emails themselves.

### Zooming into Project

The move towards more agile, connected, intelligent and data-driven
energy systems, and their interconnection with our day-to-day lives,
means that there is a major increase in cyber exposure of energy systems
leading to major safety and privacy incidents.

The EU-funded CyberSEAS project improves the resilience of energy supply
chains by protecting them from disruptions generated by complex attack
scenarios.

CyberSEAS delivers an open and extendable ecosystem of 30 customisable
security solutions providing effective support for key activities, such
as risk assessment; interaction with end devices; secure development and
deployment; real-time security monitoring; skills improvement and
awareness; and certification, governance and cooperation. CyberSEAS
solutions will be validated through experimental campaigns consisting of
numerous attack scenarios.

### Alida in the Project

The adopted solution in CyberSEAS is the synergistic use of ALIDA tool,
in pair with SED (Social Engineering Detection).

ALIDA (Advanced Learning and Integration for Data Analysis) is a
platform designed for federated machine learning and big data analytics.
It facilitates secure, scalable, and privacy-preserving machine learning
across distributed datasets. The platform supports various machine
learning frameworks and provides tools for developing, registering, and
managing BDA services.

SED (Social Engineering Detection): The SED tool focuses on detecting
social engineering and phishing attempts through comprehensive analysis
of email headers, body content, and attachments.

Most existing FML-enabled platforms support only a few open-source
frameworks/libraries available to support the development/integration of
FML-based algorithms. On the other hand, the solution integrated within
the ALIDA asset wants to be able to support as many existing libraries
and frameworks as possible, and in such a way as to be able to perform
its own federation tasks quickly, thanks also to the support of a
cloud-side graphical interface, and by exploiting/re-utilizing the
algorithms made and already available within the ALIDA catalogue.

ALIDA leverages FLOWER (Federated Learning Over Wireless Networks) \[4\]
federated learning framework because of its flexibility,
customizability, interoperability, and easiness of use. Its design
integrates workflows independent of the ML/DL framework (PyTorch,
TensorFlow, etc.) with minimum performance overhead. It supports a wide
range of machine learning algorithms, including deep learning,
reinforcement learning and classical machine learning. It also includes
model aggregation and fault tolerance, which are critical components of
any federated learning system. Flower allows building scalable federated
learning systems that can be deployed on a range of devices, including
mobile phones, edge devices, and cloud servers.

The CyberSEAS federated and self-sovereign data analytics infrastructure
has been built starting from the ALIDA platform, one of the tools made
available in the CyberSEAS toolset. ALIDA (https://home.alidalab.it/) is
a Data Science (DS) and ML platform based on advanced frameworks and
open-source technologies for design, deployment, execution and
monitoring of both stream and batch Big Data Analytics (BDA) workflows.

ALIDA is cloud-native, so it is able to scale computing and storage
resources thanks to a pipeline orchestration engine that leverages the
capabilities of Kubernetes for cloud resource management. ALIDA provides
an extensible catalogue of BDA services (the building blocks of the BDA
Application) which covers all phases, from ingestion to preparation, to
ML analysis and for data publishing.

The reference framework used to enable FML between multiple client nodes
and an aggregator node is Flower, a unified approach to federated
learning, analytics, and evaluation. As shown in the next *Figure 2.2.3:
FML Architecture Flow in ALIDA platform*, ALIDA allows federated model
training, so that users can train models without the need to expose
data.

<figure>
<img src="CyberSEAS/image_046_image8.jpg" style="max-width: 75%; height: auto;"/>
</figure>

> *Figure 2.2.3: FML Architecture Flow in ALIDA platform*

Among the few open-source technologies that enable FML, Flower has been
chosen for the following features:

1.  Scalability: it was built to enable real-world systems with many
    clients

2.  ML Framework Agnostic: it's compatible with most existing and future
    machine learning frameworks such as PyTorch, Keras, SK-Learn

3.  Cloud, Mobile, Edge & Beyond: it enables research on all kinds of
    servers and devices, including mobile

4.  Research to Production: it enables ideas to start as research
    projects and then gradually move towards production deployment with
    low engineering effort and proven infrastructure

5.  Platform Independent: it's interoperable with different operating
    systems and hardware platforms to work well in heterogeneous edge
    device environments

6.  Usability: it's easy to get started with code examples for different
    frameworks.

Starting from the Flower framework, templates have been created for a
new pair of BDA services areas for ALIDA platform: FML Aggregator and
FML Participant areas, thus based on specific modules for the
micro-service to be ALIDA compliant, being able to integrate and use at
the same time all the features provided by Flower.