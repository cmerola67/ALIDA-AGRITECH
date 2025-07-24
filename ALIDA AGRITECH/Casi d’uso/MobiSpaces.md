> # MobiSpaces

## Project Logo

![image.png](MobiSpaces/image.png)

## Project Info

| **Type** | **Start Date** | **End Date** | **ENG Grant Amount** | **PM** |
| --- | --- | --- | --- | --- |
| ML-Ops | 1 Sept 2022 | 31 Aug 2025 | 412500,00 € | x |

## Partner

![image.png](MobiSpaces/image%201.png)

![image.png](MobiSpaces/image%202.png)

| **Partner Name** | **Acronym** | **Country** |
| --- | --- | --- |
| Engineering Ingegneria Informatica S.p.A. | ENG | Italy |
| Atos Spain SA | ATOS | Spain |
| Robert Bosch GMBH | BOSCH | Germany |
| Siemens SRL | SIEM | Romania |
| Frequentis AG | FREQ | Austria |
| Azienda Mobilità e trasporti SpA | AMT | Italy |
| Marintrafik Opereisons Monoprospi Anonymi Etairia Pliroforikis | MOMA | Greece |
| Emisia SA-Anonymi Etairia Perivallontikon kai Energiakon Meleton kai Anaptixis Logismikou | EMISIA | Greece |
| Emisia SA-Anonimi Erairia | EMISIA | Greece |
| OKYS LTD | OKYS | Bulgaria |
| Ubitech Limited | UBIT | Cyprus |
| Leanxcale SL | LEANX | Spain |
| Unparallel Innovation LDA | UIL | Portugal |
| Trust-IT Services SRL | TRUST | Italy |
| COMMPLA SRL | COMMPLA | Italy |
| Geodatastyrelsen | GEODATA | Denmark |
| Digital Systems 4.0 | DS4 | Bulgaria |
| NET-U Consutlant LTD | NET-U | Cyprus |
| Universal of Piraeus Research Center | UPRC | Greece |
| Universite Libre de Bruxelles | ULB | Belgium |
| Australian Institute of Technology GMBH | AIT | Australia |
| Aalborg Univeristet | AAUN | Denmark |
| White Label Consultancy APS | WLC | Denmark |
| Fujitsu Service GMBH | FSG | Germany |
| Fujitsu Technology Solutions GMBH | FTSG | Germany |

## Overview

MobiSpaces is an end-to-end mobility-aware and mobility-optimized data governance platform based on mobility analytics for efficient, reliable, secure, fair and trustworthy data processing.

The purpose of the application is to address the problem of bus scheduling. Given a timetable (provided by the municipality of Genoa), it aims to assign a series of bus trips to a specific bus, optimizing battery usage, depot charging times, and overall fleet deployment.
Subsequently, it seeks to transform the maintenance process, currently performed traditionally, into a modern process with an approach based on automatic data learning.
Finally, it aims to measure the degradation of bus battery performance over time, predict their useful life, and anticipate details regarding their maintenance.

## Zooming into project

MobiSpaces aims to address the complex challenges of managing mobility data by providing a trustworthy and privacy-preserving platform that optimizes data processing for various applications such as intelligent transportation and vessel tracking. Through decentralized processing and validation across multiple use cases, MobiSpaces aims to establish a standard for reliable and sustainable data analytics, fostering growth in the EU digital economy.

## ALIDA in the project

From the management point of view, this work was divided in five different tasks, one for each use case: Task 6.2 (iRoute – Intelligent Public Transport Routing), Task 6.3 (SmartSense – Intelligent Infrastructure Traffic Sensing), Task 6.4 (MT
Tracker – Edge-powered Vessel Tracking), Task 6.5 VesselEdge (Edge Computing Onboard of Moving Vessel) and Task 6.6 (CrowdSeaMapping– Federated Learning for Enhancing Nautical Charts).
In particular, for iRoute, use case deals with data governance, management and analysis for public transport applications, especially in electric buses field AMT, public transport company in the city of Genova, Italy and leader of iRoute use case, has identified two real scenarios to exploit the research of MobiSpaces, applying it to challenging situations of public transport management, that can be optimized thanks to a right usage of the big amount of data collected everyday by AMT.
The scenarios allow to take advantage of the MobiSpaces outcomes and exploit the mobility-aware data governance framework to drive strategic decisions based on the outcomes of the analytics.
The use case is set in the electric-vehicle environment that is growing in AMT: the e-bus fleet includes more than 100 buses, with the related operational and managerial issues given by the complexity of the electric system, from bus recharging to battery decay.
The first scenario is about predictive maintenance of electric buses and aims to anticipate possible faults, thanks to the machine learning techniques studied in the project. The second scenario deals with battery level management and aims to give an instrument to re-build bus schedules, both real-time and long-term, given predictions on battery duration based on the data analysed and on the expected battery decay.

![image.png](MobiSpaces/image%203.png)

Together with the already quoted machine learning techniques, many MobiSpaces components are working for use case 1, as explained in detail in the paragraphs below. The starting datasets are mostly internal to AMT, and are:

- AVM (Automatic Vehicle Monitoring) data, that show real-time the positioning of each bus of the fleet and afterwards the trajectory travelled by the bus.
- GTFS data, that contain the planned transit service in an open de-facto standard used by Public Transport Operators.
- CanBus data, that collect information about the status of many bus systems including battery level, using FMS standard.

These internal data will be interlinked with external data, relevant for battery level, such as weather data or the elevation and the gradient of the path.

The internal data are usually located and stored on internal servers. A mission of the use case, detailed later in the deliverable, is to create a good, efficient and sustainable data path for the datasets described.