# [O-RAN.WG1.Use-Cases-Detailed-Specification-R003-v13.00](https://orandownloadsweb.azurewebsites.net/specification) 
# Use case 21: Energy Saving
-  Energy saving (ES) techniques can be implemented at different timescales and cell loads, such as switching off carriers or cells, RF channel switching, and Advanced Sleep Modes (ASM).
- ES solutions can be applied to various components of the O-Cloud, including O-CU and O-DU.  AI/ML helps figure out the best times to switch things off and on for maximizing energy savings.
![image](https://hackmd.io/_uploads/ByjNQ9d6p.png)


![image](https://hackmd.io/_uploads/rk2lv5_pp.png)
### Table from diagram
| stage | Non-RT RIC |Near-RT RIC |
| :---: | --- |---|
|1| SMO initiates specific measurement data collection request towards E2 Node and O-RU for AI/ML model training.| **same**| 
|2| E2 Node and O-RU send the configured measurement data to SMO periodically|**same**| 
|3| Non-RT RIC retrieves the collected measurement data for processing|**same**| 
|4| Non-RT RIC monitor performance and energy consumption of the E2 Node, also energy consumption of O-RU.|Non-RT RIC  trains the AI/ML models with the collected data. Trained AI/ML models are deployed, configured, and activated in the Near-RT RIC.  | 
|5| Based on the AI/ML inference the Non-RT RIC can request the SMO to configure E2 Node to prepare and execute cell or carrier switch off/on. |SMO can trigger EE/ES optimization and might provide policies guiding  the Near-RT RIC EE/ES function via O1 and/or A1 interface. |
|6|SMO guides E2 node via O1 to fulfill Non-RT RIC requests. O-RU receives updated configuration through Open FH M-Plane from E2 Node or SMO. SMO is notified by E2 Node/O-RU upon completion of cell or carrier switch off/on. |Near-RT RIC monitor performance and energy consumption of the E2 Node, also energy consumption of O-RU. E2 Node can request O-RU Node to prepare and execute cell or carrier switch off/on. E2 Node will notify Near-RT RIC once cell or carrier switch off/on is completed.|
|7|Non-RT RIC monitors AI/ML model performance. If energy-saving goals aren't met, it may trigger fallback, AI/ML model update, or retraining.|**--**|

**ends when**: E2 Node becomes non-Operational or when the operator disables the optimization functions for Energy Saving. 

# Review Paper

| item | information |
| --- | --- |
| Title| Understanding O-RAN: Architecture, Interfaces, Algorithms, Security, and Research Challenges|
|Paper Link |https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10024837 |
| Authors |Michele Polese, etc.|
| Date of Publication |  23 January 2023 |
|type | Journals|
| pages | 1376 - 1411|
| keywords | Open RAN, O-RAN, cellular, 5G, 6G |

This paper provides a comprehensive analysis of O-RAN technical specifications, architectural components, interfaces, ML and closed-loop control workflows, security challenges, experimental platforms, and recent results on design and optimization.
## Architecutre
![image](https://hackmd.io/_uploads/S13Ef4lCa.png)
**Figure 2.** The traditional black-box base station architecture is evolving towards a virtualized gNB with a functional split.
- The gNB is split into a Central Unit (CU), a Distributed Unit (DU), and a Radio Unit (RU). The CU is further split into two logical components, one for the CP, and one for the UP. 
-  The DU then takes care of the remaining functionalities of the physical layer, and of the Medium Access Control (MAC) and Radio Link Control (RLC) layers
-   A non-real-time RIC integrates with the network orchestrator and operates on a timescale longer than 1 second, while a near-real-time RIC controls loops with RAN nodes on a timescale between 10 milliseconds and 1 second.

## AI Model
- In the Paper each base station hosts three slices:
	1. **URLLC** for ultra-low latency services, 
	2. **eMBB** for high-throughput traffic (e.g., video streaming and file transfer)
	3. **mMTC** to handle traffic generated by small sensors and IoT devices.
- ![image](https://hackmd.io/_uploads/rkeaUK9x0.png)
 
1.  **Data Collection and Processing**
	- data is collected over the O1, A1 and E2 interfaces. 
	- For instance, since the xApp must adapt RAN slicing policies for different slices according to current data demand and required minimum performance levels, the collected data must include the number of Physical Resource Blocks (PRBs) needed to transmit data requested by  by each user of the three slices (eMBB, mMTC, and URLLC).
2.  **Training**
	- AI/ML models are required to go through an offline training to ensure reliability and prevent network issues from poorly trained models.
	- for instance, the operator has the capability to train various AI algorithms that manage the allocation of PRBs to different network slices. 
3.  **Validation and Publishing**
	- If validation is successful and the models are considered deployment-ready, they are published and stored in an AI/ML catalog on the SMO/non-RT RIC.
	- for instance, evaluating how well diverse AI solutions perform under diverse traffic patterns and demand, number and distribution of users, available bandwidth and operational frequencies.
4.  **Deployment**
	- Models in the AI/ML catalog can be **deployed  via the O1 interface** and executed through two options: image-based and file-based deployments. **The executing node known as the  inference host**.
	1. In the image-based deployment, the AI/ML model operates as a containerized image in the form of xApps or rApps deployed at the O-RAN nodes
	2. file-based deployment involves downloading the AI/ML model as a standalone file that executes outside the xApps or rApps
	- for instance,  the operator selects pre-trained AI-based RAN slicing models from the AI/ML catalog and deploys them as xApps in the near-real-time RIC
5.  **AI/ML Execution and Inference**
	-  Once deployed on the inference host, the models receive data for various online inference tasks such as classification, prediction, policy derivation at RICs transmitted over A1 and E2 interfaces, and management also control actions over O1 and E2 interfaces.
6.  **Continuous Operations**
	- ![image](https://hackmd.io/_uploads/BkexK35eR.png)
	- To ensure continuous improvement and avoid service interruptions, poorly performing online models can be refined and re-trained. This approach helps mitigate issues related to data or service unavailability and facilitates seamless updates to AI/ML models.
	- For instance, the operator can continuously monitor the performance of the RAN slicing xApp. If anomalies or inefficiencies are detected, they can opt to re-train the embedded AI/ML model using new data collected through the O1 and E2 interfaces.