> ## Infinitech


<figure>
<img src="Infinitech/image_064_image17.png" style="max-width: 40%; height: auto;"/>
</figure>

> *Figure 2.6.1: Infinitech Project Logo*

| **Type** | **Start Date** | **End Date** | **ENG Grant Amount**  | **PM**|
| --- | --- | --- | --- | --- |
| ML-OPS |      1 Octo 2019 |  31 Marc 2023  |        n.a.|            n.a.|

> *Table 2.6.7: Infinitech Project Info*

### Partners

<figure>
<img src="Infinitech/image_065_image18.jpg" style="max-width: 75%; height: auto;"/>
</figure>

> *Figure 2.6.2: Infinitech Partners Logo 01*


| **Partner Name**                           | **Acronym** | **Country**   |
| --- | --- | --- | 
| Engineering Ingegneria Informatica S.p.A.    | ENG         | Italy       |
| Atos Spain Sa                          | ATOS        | Spain         |
| Ibm Israel - Science And Technology Ltd   | IBM         | Israel        |
| Fujitsu Technology Solution            | FUJITSU     | France        |
| Hewlett Packard Italiana Srl           | HP          | Italy         |
| Singularlogic Anonymi Etaireia Pliroforiakon Systimaton Kai Efarmogonpliroforikis         | SAEP        | Greece        |
| Innovation Sprint                      | IS          | Belgium       |
| Santander Uk Plc                       | SAN         | United Kindom |
| Sia Spa                                | SIA         | Italy         |
| Unicaja Banco Sa                       | UB          | Spain         |
| National Bank Of Greece Sa             | NBG         | Greece        |
| Aktif Yatirim Bankasi As               | AYB         | Türkiye       |
| Banka Slovenije                        | BS          | Slovenia      |
| Banking & Payments Federation Ireland Company Limited By Guarantee  | BPFI        | Ireland       |
| Dynamis Ae Genikon Asfaleion           | DAGA        | Greece        |
| Genillard & Co Gmbh                    | GEN         | Germany       |
| Jrc Capital Management Consultancy & Research Gmbh   | JRC         | Germany       |
| Prive Services Europe Gmbh             | PSE         | Austria       |
| Crowdpolicy Psifiakes Symmetoxikesypiresies                   | CPSI        | Greece        |
| Poste Italiane - Spa                     | PI          | Italy         |
| Wenalyze                                 | WEN         | Spain         |
| Paris Europlace                          | PE          | France        |
| Copenhagen Fintech                       | CF          | Denmark       |
| Reportbrain Limited                      | RL          | United Kingdom       |
| Leanxcale Sl                             | LEAN        | Spain         |
| Gioumpitek Meleti Schediasmos Ylopoiisi Kai Polisi Ergon Pliroforikis Etaireia Periorismenis Efthynis | GMSY        | Greece        |
| Innov-Acts Limited                       | IAL         | Cyprus        |
| Unparallel Innovation Lda                | UI          | Portugal      |
| Roessingh Research And Development Bv    | RRAD        | Netherlands   |
| Etam Anonymh Etaireia Symboyleytikon Kai Melethtikon Ypireseion | EAES        | Greece        |
| Fondazione Bruno Kessler                 | FBK         | Italy         |
| University Of Galway                     | UG          | Ireland       |
| Uninova-Instituto De Desenvolvimento De Novas Tecnologias-Associacao | UID         | Portugal      |
| Bogazici Universitesi                    | BU          | Türkiye       |
| Institut Jozef Stefan                    | IJS         | Slovenia      |
| Edex - Educational Excellence Corporation ltd            | EDEX        | Cyprus        |
| University Of Glasgow                    | UG          | United Kingdom       |
| Association O.R.T                        | ORT         | France        |
| Fundacion Para La Promocion De La Innovacion Investigacion Y Desarrollo Tecnologico En La Industria De Spain  Automocion De Galicia     | FPLAPDLI    |     Spain     |
| Fundacion Centro Tecnoloxico De Telecomunicacions De Galicia          | FCT         | Spain         |
| Dwf Germany Rechtsanwaltsgesellschaft  Mbh  | DWF         | Germany       |
| Abi Lab-Centro Di Ricerca E Innovazione Per La Banca    | ABILAB      | Italy         |
| Bank Of Cyprus Public Company Ltd        | BCP         | Cyprus        |
| Caixabank Sa                             | CAIXA       | Spain         |
| Agricultural Applications Ike            | AAI         | Greece        |
| University Of Piraeus Research Center    | UPRC        | Greece        |
| Assentian Europe Limited                 | AEL         | Ireland       |
| Clear Communication Associates Ltd       | CCAL        | United Kingdom       |
| Inneurope Initiative S.L.                | IISL        | Spain         |
| The Governor And Company Of The Bank Of Ireland | BOI         | Ireland       |
| Traffikanalysis Hub Limited              | THL         | United  Kingdom      |
| Nexi Payments Spa                        | NEXI        | Italy         |

> *Table 2.6.8: Infinitech Partners 01*

### Case Overview

Poste Italiane sends data related to banking transactions to ALIDA,
which, through the BDA App, trains a model for outlier classification.

This model is then deployed and used on a graphical user interface (UI)
to provide a probability (to a domain expert) that new transactions were
fraudulent.

The same interface is also utilized to gather feedback from the domain
expert, which is useful for enriching the labelling of data, thus making
the model increasingly performing with each training iteration. See
*Figure 2.6.3: Infinitech Contributions 01*


<figure>
<img src="Infinitech/image_067_image19.jpg" style="max-width: 75%; height: auto;"/>
</figure>

> *Figure 2.6.3: Infinitech Contributions 01*

### Zooming into Project

Emerging technologies such as big data, artificial intelligence (AI) and
the internet of things (IoT) all have the potential to revolutionise how
we live, work and play. But tapping into that potential first requires
knowing how to use them -- something that for the financial and
insurance industry can be easier said than done.

"Many financial and insurance institutions still face difficulties using
big data technology due to complicated regulations and a lack of
appropriate test bed resources," says Maurizio Ferraris, innovation
manager at GFT Italia.

With the support of the EU-funded INFINITECH project, GFT, together with
a consortium of over 40 fintech partners, are working to lower the
barriers to datadriven innovation, boost regulatory compliance and
stimulate investment.

In a nutshell, ALIDA is a Micro-service based platform for composition,
deployment, optimisation, execution and monitoring of pipelines of Big
Data Analytics (BDA) services. ALIDA is a result of previous research
activities developed by ENG. Currently, it is a work in progress. ALIDA
offers a catalogue of BDA services (ingestion, preparation, analysis,
visualization): user designs his own (stream/batch) pipeline by choosing
the BDA services from it, indicates which Big Data set he wants to
process, launches and monitors the execution of the pipeline and
personalizes the results visualization by choosing from a set of
available graphs, all this without worrying about having software
developer skills or particular knowledge on big data technologies. This
service is registered in ALIDA catalogue as Spring Boot Application
containing the python code and its dependencies. After implementing the
algorithm using Pyspark, creating the Dockerfile and pushing the new
image inside a repository, this microservice is registered into the
ALIDA catalogue through the GUI. Source: https://home.alidalab.it/

ALIDA asset is a microservice based platform for data management and
composition, deployment, optimisation, execution and monitoring of big
data analytics data workflow (covering ingestion, preparation, analysis
and visualization), which has been developed by ENG in previous and
ongoing research activities. The main functionalities of ALIDA are:

- Streaming and Batch data workflow processing

- Catalogue of Big Data Analytics (BDA) services (covering ingestion,
  prepara-tion analysis, visualization) for various data analytics
  scenarios

- Graphical editor for building data workflow

- Data pipeline deployment by means of modern resource orchestrators
  such as Kubernetes

- Workflow execution monitoring

- Data visualization customization through a set of graphs and query
  editor

- Graphical User Interface to easily create and redistribute new custom
  BDAservices.

ALIDA presents a microservice architecture, where microservices are
deployed in containers, whose management is largely simplified by
Kubernetes, a container orchestrator which automates the deployment,
management, scaling, and networking of containers.

Basically, *Figure 2.6.4: Infinitech Contribution 02* shows three flows:
service registration (blue flow), workflow design and execution (red
flow) and visualization (orange flow).

The key flow is the workflow design and execution: by means of the GUI
user designs a workflow and executes it. In this case, the core
components of ALIDA submit the request of execution and deployment of
the workflow to the candidate orchestrator. Currently just Spring Cloud
Data Flow 8 is adopted as pipeline orchestrator in ALIDA.

Spring Cloud Data Flow (SCDF) is a Microservice based Streaming and
Batch data processor that can make use of a variety of container
orchestrators. In the ALIDA platform, the SCDF engine instance uses an
implementation of the Spring Cloud Deployer for Kubernetes. Then,
Kubernetes uses the computation resources available into the platform
and the persistence layer to manage data storage and workloads.

The platform currently supports several frameworks such as Spark, H2O,
Flink, mainly used for BDA service development and registration. Other
frameworks may be deployed, and relevant machine learning libraries
available for Python can be used. It is worth to notice that BDA
services may or may not be implemented working on these frameworks. The
only requirement that the BDA services must match is that they have to
be implemented as a spring boot application shipped within a docker
image that can optionally contain a python application.

In ALIDA, most of the BDA services developed are based on Spark, so they
are able to process a large volume of data, in a distributed
environment. Spark is used for both batch and streaming applications
thanks to Spark Streaming.

Regarding the persistence layer, Hive and Redis play several roles. Hive
is used both to access the data resulting from the execution of the
workflows through the visualization component, and to ensure that SPARK
can write and read the datasets stored into HDFS.

![image_068_image20.png](Infinitech/image_068_image20.png)

> *Figure 2.6.4: Infinitech Contribution 02*

Redis is used by ALIDA to store some properties related to the platform
and to serve the visualization component with the aim to create graphs
and visualizations with real time updating capabilities. Last but not
least, Kafka is adopted on various fronts: the platform, the core
component of ALIDA, uses it to transmit and update the properties during
the workflow execution phases. SCDF itself exploits it in the management
of streams pipelines. ALIDA is cloud native software, this means that it
can be seamlessly deployed both in an on-premises environment and on the
cloud environments provisioned by the widely known providers such as
Microsoft Azure, Amazon AWS and Google Cloud Platform. In the context of
the INFINITECH project, ALIDA will be used in Pilot 10 to facilitate the
development of real-time BDA service in the context of Cyber-Security
for financial transactions.

### Alida in the Project

This pilot aims at significantly improving the detection rate of
malicious events (i.e., fraud attempts) and enabling the identification
of security-related anomalies while they are occurring by the analysis
in real-time of the financial transactions of a home and mobile banking
system.

This approach thus allows proactive and prompt interventions on
potential security threats. More specifically, Pilot 10 is developing a
tool based on ML techniques applied to real-time, financial transaction
data-streams focused on adaptive detection for malicious transactions
leveraging on established big-data analytics' practices.

The analysis of vast amounts of data will help to define relevant
cyber-risk rating metrics and allow us to implement adaptive security
measures and controls, based on real cyber-security postures.

*Current implementation status on Pilot 10 is shown in Figure 2.6.5:
Infinitech Contribution 03*.

![image_069_image21.jpg](Infinitech/image_069_image21.jpg)

> *Figure 2.6.5: Infinitech Contribution 03*

Poste Italiane create Synthetic and Realistic data set on "Bank Transfer
SEPA" transactions that are consistent with the real data present in the
data operations environment *Figure 2.6.6: Infinitech Contribution 04*.
These data sets are going to be used by Pilot 10 and, more in concrete,
for the first PoC. To develop the services and workflows and ALIDA
instance was deployed on ENG premise. As a Preliminary step: a job to
transfer synthetic data set on "Bank Transfer SEPA" transactions from an
SFTP server to ALIDA HDFS, was designed and it is up and running.

With the data ready to be processed, and using ALIDA, a first Batch
processing/workflow has been created. This workflow converts qualitative
fields into quantitative one, train a KMeans model and makes the
clustering process. The Figure 31:shows developed ALIDA workflow based
on three steps (string-indexer, trains the data with a KMeans models and
the clustering creation).

> After that, the data is grouped and visualized by clusters (*Figure
> 2.6.7: Infinitech Contribution 05*).

Here a domain expert has to label which clusters would be suspicious of
fraud. After that the Stream processing would start labelling and
detecting new incoming data in real time. But this part is not
implemented yet.

![image_070_image22.png](Infinitech/image_070_image22.png)

> *Figure 2.6.6: Infinitech Contribution 04*

![image_071_image23.png](Infinitech/image_071_image23.png)

> *Figure 2.6.7: Infinitech Contribution 05*

