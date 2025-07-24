> ## SCREAM

<figure>
<img src="SCREAM/image_061_image14.jpg" style="max-width: 35%; height: auto;"/>
<figcaption><p>Figure 2.4.3</p></figcaption>
</figure>

> *Figure 2.5.1: SCREAM Project Logo*

| **Type** | **Start Date** | **End Date** | **ENG Grant Amount**  | **PM**|
| --- | --- | --- | --- | --- |
| CLOUD-EDGE | 1 July 2020 | 30 June 2023 | n.a. | n.a.|

> *Table 2.5.5: SCREAM Project Info*

### Partners

<figure>
<img src="SCREAM/image_062_image15.jpg" style="max-width: 75%; height: auto;"/>
</figure>

> *Figure 2.5.2: SCREAM Partners Logo*


| **Partner Name**                           | **Acronym** | **Country**   |
| --- | --- | --- | 
| Engineering Ingegneria Informatica S.p.A.    | ENG         | Italy       |
| Eka Srl                                    | EKA         | Italy       |
| IPREL Progetti Srl                           | IPREL       | Italy       |

> *Table 2.5.6: SCREAM Partners*

### Case Overview

The SCREAM project proposes to study, define, design and implement an
integrated, modular, flexible and adaptable platform for building
dedicated solutions for the remote and optimised monitoring, maintenance
and management of machines (Monitoring and Control - M&C) and production
equipment (e.g. to predict equipment failures and determine solutions
before they occur).

The platform will allow machine problems to be diagnosed (or predicted)
and resolved via secure remote access, without the need for an on-site
visit.

An open-source GUI for data visualization and exploration was made
available on the cloud to consult both the stored historical data and
the predictions obtained from the ML models trained on the consumption
of the cutting blade and number of cuts; other ML/DL models for
predictive maintenance and decision support were exported and used
within applications run on the Sofidel company's own machines, applied
to real-time data.

<figure>
<img src="SCREAM/image_063_image16.jpg" style="max-width: 75%; height: auto;"/>
</figure>

> *Figure 2.5.3: SCREAM Contribution 01*

### Zooming into Project

The solutions proposed in the project will be based on Big Data and
Artificial Intelligence and will consider the specific characteristics,
peculiarities, needs and requirements of the production environment and
the organisations using the production equipment and machines.
Furthermore, special attention will be given to the specific business
relationship that exists between the manufacturer/supplier and the
various users (goods producing industries).

Engineering is the Project Coordinator and is responsible for all
activities linked to the definition of the SCREAM Framework. Engineering
is also working on Big Data Infrastructure for remote and secure "M&C"
systems, aiming to define the infrastructure for Industrial Big Data
Analytics based on a hybrid edge-cloud model and a complete toolkit of
algorithms and analysis techniques to support machine analyses. Moreover
Engineering takes care of the design of application services for the
remote "M&C" systems of production machinery, with the aim of offering
advanced services to support decision making.

### Alida in the Project

In the example, the company Sofidel (producer of paper for hygienic and
domestic use) sends IoT data in streaming to ALIDA through an
asynchronous MQTT messaging protocol. This data includes information
from machinery (embosser, rewinder, cutter blade, unwinder) for paper
production.

In ALIDA, both **BDA App** streaming for the *data acquisition* and
*data preparation,* and *batch* for pre-process and generate ML/DL
models based on data stored within distributed data storage.

