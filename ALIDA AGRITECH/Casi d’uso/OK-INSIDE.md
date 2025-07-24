> ## OK-INSAID

<figure>
<img src="OK-INSIDE/image_072_image24.jpg" style="max-width:40%; height: auto;"/>
</figure>

> *Figure 2.7.1: OK-INSAID Project Logo*

| **Type** | **Start Date** | **End Date** | **ENG Grant Amount**  | **PM**|
| --- | --- | --- | --- | --- |
| CLOUD-EDGE |    1 Nove 2018 |  31 Marc 2022  |        n.a.   |        n.a. |

> *Table 2.7.9:* OK-INSAID Project Info

### Partners

<figure>
<img src="OK-INSIDE/image_066_image25.jpg" style="max-width: 75%; height: auto;"/>
</figure>

> *Figure 2.7.2: OK-INSAID Partners Logos*

| **Partner Name**                           | **Acronym** | **Country**   |
| --- | --- | --- | 
| Engineering Ingegneria Informatica S.p.A.    | ENG         | Italy       |
| EKA S.r.l. |     EKA  |         Italy |
| Università degli Studi di Palermo |    UNIPA |         Italy |
| Università del Salento  |   UNISAL |        Italy |
| Consiglio Nazionale delle Ricerche  |    CNR   |        Italy |
| Cefriel |    CEFRIEL |         Italy |
| Tera S.r.l. |      TERA  |        Italy |
| Consorzio Calef  |   CALEF |         Italy |
| GE Avio S.r.l.   |   GEA   |        Italy |
| SACMI |    SACMI |         Italy |

> *Table 2.7.10: OK-INSAID Partners*

### Case Overview

In this case, the SACMI company that create ceramic slabs sends data to
ALIDA in streaming. These data include information about the composition
used for the creation of slabs and the results obtained about the
quality of the stubs produced. ALIDA, through a **streaming BDA App
(1)**, processes, cleans, and stores such data in a distributed store,
fundamental for **Big Data** management.

In a later time, another **BDA App batch (2)** deals with training of a
model based on collected data. An application puts on the edge
(**Prediction**), near the data production site, **downloads from ALIDA
the model** of the produced ML.

This model guides company operators to the composition of the procedure,
based on input parameters.


<figure>
<img src="OK-INSIDE/image_001_image26.jpg" style="max-width:75%; height: auto;"/>
</figure>

> *Figure 2.7.3: OK-INSAID Contribution 01*

### Zooming into Project

One of the most widely adopted quality management strategies today is
Zero Defect Manufacturing (ZDM), a new paradigm aimed at surpassing
traditional Six Sigma approaches through knowledge management, supported
by new methodologies, technologies, and integrated tools for
maintenance, quality control, and production logistics.

The general functional requirements of zero-defect manufacturing can be
summarized as a system with the following capabilities:

1.  Data collection via smart sensors,

2.  Automatic signal processing, filtering, and feature extraction,

3.  Data mining and knowledge discovery for diagnosis and prognosis,

4.  Providing clear and concise information and advice on defects to the user,

5. Self-adaptation and optimization control.

ZDM Monitoring systems highlight that, in order to achieve zero defect
manufacturing, new cost-effective tools for monitoring and optimizing
quality with multiple and autocorrelated data should be developed.

Therefore, it is necessary to manage processes in real-time based on
inputs derived from simulation models to provide a clear and detailed
understanding of the entire process and detect all possible causes of
defects.

To achieve such digital representations, it is necessary to build a
detailed and high-precision model capable of providing various options
for identifying optimal product or process parameters.

The suggestion is to adopt Digital Twin technology during the production
phase to optimize production planning and process control.

In SACMI's production, the main components identified to better define
an investigation in this regard concern porosity and the percentage of
average penetration in the welding process.

The algorithms developed to predict the percentage values of penetration
and porosity in laser welding have been uploaded to the online platform
provided by the project, using the Docker system.

### Alida in the Project

The entire predictive analysis pipeline, as designed, implemented, and
extensively documented in previous project reports, consists of five
fundamental steps (pipeline steps, abbreviated as PS):

1.  Pre-processing of datasets, consisting of temporal reordering,
    cleaning, normalization, splitting into train/validation/test, and
    final saving of the divided files. **\[PS1\]**

2.  Model training, exploring different training configurations (e.g.,
    referring to model hyperparameters such as learning rate or the
    number of training epochs, among others, or the type of training);
    finally, saving the weights of the trained model. **\[PS2\]**

3.  Validation of model performance, with the objective of selecting the
    best configuration based on calculated values for specific accuracy
    metrics, such as the well-known precision and recall; finally,
    saving the best parameters. **\[PS3\]**

4.  Testing model performance, to evaluate the quality of predictions
    when they are made on new and unseen data, but whose true value is
    known (i.e., the true welding quality). **\[PS4\]**

5.  Final prediction on completely new data that, according to what
    emerged during the project, are provided by the predictive models
    trained and tested by other partners. **\[PS5\]**

**Services and Application**

The Alida Cloud microservices platform operates on two fundamental
components, namely "**services**" and "**applications**."

Specifically, one or many services constitute an application. The end
user is responsible for launching an application, while the services
represent something abstract and internal to the application itself.

In this context, the 5 PS were transferred and implemented as Python
scripts within services. To achieve this, the PS were first grouped
into:

1.  **Dataset Preparation + Model Training + Validation \[PS1\] +
    \[PS2\] + \[PS3\]** we could call it as **S1;**

2.  **Model Testing \[PS4\] we could call it as S2;**

3.  **Prediction on New Data \[PS5\]** we could call it as **S3.**

The three services implemented on the Alida microservices platform were
transformed into Docker images to make them portable and host them on
the popular Docker image hosting platform known as DockerHub. Indeed, to
create a new service on the Alida Cloud platform, a JSON file containing
all the characteristics and metadata of the service, including the
reference to the Docker image uploaded on DockerHub, must be created.

Thus, a Python script was implemented and released for the partners
involved in predictive analysis through the Alida Cloud platform,
designed to generate the JSON configuration file.

Having uploaded the services as Docker images on DockerHub and generated
the JSON files containing the metadata for each service, it was possible
to create and upload the services on the Alida Cloud platform. They can
be found on the platform as:

**\[S1\] poliba-fit-3-0** - *Figure 2.7.4: OK-INSAID Contribution 02*
shows a screenshot of the parameters required by the service.

**\[S2\] poliba-test-3-0** - *Figure 2.7.5: OK-INSAID Contribution 03*
shows a screenshot of the parameters required by the service.

**\[S3\] poliba-predict-3-6** - *Figure 2.7.6: OK-INSAID Contribution
04* shows a screenshot of the parameters required by the service.

Finally, as indicated previously, the three services were grouped to
form two applications (named A1 and A2):

**\[A1\]** comprising S1+S2, for pre-processing, training, and testing -
*Figure 2.7.7: OK-INSAID Contribution 05* shows a screenshot of the
execution of application A1.

**\[A2\]** comprising S3, consisting of prediction on new data - *Figure
2.7.8: OK-INSAID Contribution 06* shows a screenshot of the execution of
application A2.


<figure>
<img src="OK-INSIDE/image_002_image27.jpg" style="max-width: 100%; height: auto;"/>
</figure>

> *Figure 2.7.4: OK-INSAID Contribution 02*

![image_003_image28.jpg](OK-INSIDE/image_003_image28.jpg)

> *Figure 2.7.5: OK-INSAID Contribution 03*

![image_004_image29.jpg](OK-INSIDE/image_004_image29.jpg)

> *Figure 2.7.6: OK-INSAID Contribution 04*

![image_005_image30.jpg](OK-INSIDE/image_005_image30.jpg)

> *Figure 2.7.7: OK-INSAID Contribution 05*

![image_006_image31.jpg](OK-INSIDE/image_006_image31.jpg)

> *Figure 2.7.8: OK-INSAID Contribution 06*

