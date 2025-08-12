# Value of the Data in an Internet of Vehicles Network
Internet of Vehicles (IoV) manifests a highly dynamic communication network that facilitates interactions between vehicles via Vehicle-to-Vehicle (V2V) communication, vehicles and supporting roadside infrastructure via Vehicle-to-Infrastructure (V2I) communication, vehicles and vulnerable pedestrians via Vehicle-to-Pedestrian (V2P) communication, and vehicles and backbone network via Vehicle-to-Network (V2N) communication, thereby realizing Vehicle-to-Everything (V2X) communication. With the rapid advancement of information and communication technologies and artificial intelligence, IoV network is also experiencing a period of rapid growth. However, when it comes to the security of an IoV network, there still remains considerable challenges. In particular, conventional cryptography-based schemes are inadequate for addressing internal security attacks in a highly dynamic and distributed IoV network. On the contrary, trust-based approaches have demonstrated a potential for intelligently addressing such attacks. Trust, in essence, refers to the probability of a trustee to realize a certain action or a set of services, i.e., requested by a trustor, in an appropriate manner at a particular instance of time. Trust values, expressed within the range of [0, 1], serve as a quantitative measure for evaluating the trustworthiness of a trustee with 0 implying untrustworthiness and 1 suggesting trustworthiness.

As of date, there remains a significant lack of publicly accessible trust-based IoV datasets that can be utilized by the research community. This scarcity constitutes a critical bottleneck and has persistently impeded the evaluation of trust-based mechanisms in the context of an IoV network. Therefore, the significance of the envisaged trust-based IoV dataset is as follows:

• This particular trust-based IoV dataset is well-suited for assessing the trustworthiness of vehicles. By weighted aggregation of the trust parameters, i.e., experience of interaction, frequency of interaction, timeliness of interaction, and quality of received messages, a total trust score can be ascertained for each vehicle at each time instance. If the total trust score for a particular vehicle exceeds the stipulated trust threshold, it is classified as trustworthy or untrustworthy otherwise. Trust parameters can also be analyzed via intelligent learning-based algorithms and the classification pertinent to trustworthy and untrustworthy vehicles can be effectively distinguished via an optimal decision boundary. 

• This dataset encompasses the simulation of various trust-based attacks, i.e., on-off attacks, self-promoting attacks, and opportunistic attacks, thereby assisting researchers from both academia and industry to validate the robustness of their respective IoV-based trust mechanisms.

• This particular IoV dataset has a potential to be employed for trustworthy participant selection in the context of federated learning frameworks. It is pertinent to highlight that only reliable participants can ensure the integrity and reliability of this collaborative learning approach, and reduce the risks associated with the data poisoning attacks.

# Background

The motivation for designing this trust-based IoV dataset arises from the growing demand for secure and reliable communication in an IoV network. As vehicles increasingly depend on V2X communication, trust management becomes highly indispensable for preventing malicious behaviors in a bid to ensure traffic safety since failing to do so could result in road fatalities. Owing to the inherent dynamic and transient characteristics of an IoV network, conventional security mechanisms often fail to address the unique requirements of the said network. This trust-based IoV dataset has been, therefore, envisaged for assessing the trustworthiness of dynamic and transient interactions between vehicles. Accordingly, a realistic driving scenario under various dynamic traffic conditions has been employed for the said purpose and by particularly incorporating both trustworthy and malicious behaviors. This dataset encompasses four salient trust parameters, i.e., experience of interaction, frequency of interaction, timeliness of interaction, and quality of received messages, to support both conventional (weighted) and a learning-based approach, thereby offering researchers a standardized benchmark for evaluating their respective trust models for improving the resilience of an IoV network. 

# Data Description

Over the past decade or so, the notion of trust has become a focal point for researchers across academia and industry. Accordingly, the manuscript-at-hand presents an IoV simulator envisaged via Java. To ensure a realistic outlook, we have not only incorporated trustworthy vehicles but have also catered for malicious vehicles which dynamically switch between trustworthy and untrustworthy behaviors to execute trust-based attacks in order to evade detection in the context of an IoV network.

The envisaged trust-based IoV dataset encompasses 96 vehicles that have carried out 1,048,576 interactions in total, i.e., both positive and negative, at different time instances. The envisaged dataset is in a tabular format and comprises 10 columns, i.e., Interaction Time, Trustor, Trustee, four trust parameters (Experience of Interaction, Frequency of Interaction, Timeliness of Interaction, and Quality of Received Messages), Total Trust, and two labels (MaliciousVehicle and IsAttacking). The details are presented as follows:

**Trustor** - The trust between vehicles is ascertained by integrating multiple trust parameters which are primarily quantified based on the relationship between them. Accordingly, the vehicle that intends to act as an evaluator so as to assess and determine the trustworthiness of a target vehicle is defined as a trustor. The same is depicted in the second column of our envisaged trust-based IoV dataset.

**Trustee** - The target vehicle, i.e., the one whose trustworthiness is being ascertained, is referred as a trustee. In our envisaged trust-based IoV dataset, trustees have been delineated in the third column. It is pertinent to mention that 94 trustees have engaged in a total of 1,048,576 interactions with trustors in the context of the said dataset.

**Experience of Interaction (IExp)** - Experience of Interaction (0=< IExp <=1) manifests the interaction-based history between a trustor and a trustee in an IoV network, and is, therefore, measured at a time instance t by taking into account the proportion of the total number of positive interactions between a trustor and a trustee vis-`a-vis the total number of interactions amongst them up to that particular time. IExp is presented in the column four of our envisaged trust-based IoV dataset.

**Frequency of Interaction (IFre)** - Frequency of Interaction (0=< IFre <=1) suggests how often a trustor interacts with a trustee at a time instance t, and is quantified by considering the proportion of the total interactions between a trustor and a trustee to the trustor’s total interactions with all other trustees up to that particular time. A higher frequency of interactions thus  contributes to more accurately determining the true characteristics of a trustee. IFre is depicted in the column five of our envisaged trust-based IoV dataset.

**Timeliness of Interaction (ITim)** - Timeliness of Interaction (0=< ITim <=1) signifies the time of interaction between a trustor and a trustee with respect to the current time. Due to the inherent highly dynamic characteristics of an IoV network, prioritizing recent interactions over previous ones is crucial. Accordingly, in the design of this IoV simulator, considerable attention was accorded to this particular parameter. ITim is illustrated in the column six of our envisaged trust-based IoV dataset.

**Quality of Received Message (RMQ)** - Quality of Received Message (0=< RMQ <=1) primarily depends on the network communication quality within an IoV network and, therefore, has a direct impact on the quality of messages that a trustee receives from a trustor at a time instance t. A higher network communication quality typically suggests that a trustor can ascertain the trustworthiness of a trustee in a more precise manner. RMQ is outlined in the column seven of our envisaged trust-based IoV dataset.

**Total Trust** - The total trust of a particular vehicle is quantified via the above proposed four trust parameters, i.e., experience of interaction, frequency of interaction, timeliness of interaction, and quality of received messages. In our envisaged trust-based IoV dataset, a weighted sum approach has been employed to aggregate the said trust parameters. When a vehicle's total trust exceeds the stipulated threshold, the said vehicle is considered trustworthy, otherwise, it is deemed untrustworthy. Furthermore, the total trust value can also be used to evaluate a vehicle’s behavior over time, i.e., by detecting temporal changes in a vehicle's behavior, different types of trust-based attacks instigated by the said vehicle, if malicious, can be identified. This, therefore, enables the detection and subsequent elimination of malicious vehicles from an IoV network. In the envisaged trust-based IoV dataset, the total trust is depicted in column eight.

**MaliciousVehicle** - MaliciousVehicle is a label employed to indicate the behavior of a vehicle within our envisaged trust-based IoV dataset, i.e., 'Yes' denotes an attacking vehicle, whereas, 'No' indicates a normal, non-malicious vehicle. MaliciousVehicle is presented in the column nine of our envisaged trust-based IoV dataset.

**IsAttacking** - IsAttacking is a label that illustrates whether a vehicle is currently in an attacking state. 'Yes' implies that a vehicle is actively performing a trust-based attack, whereas, 'No' suggests that a vehicle is playing intelligently by engaging in a normal interaction. IsAttacking is delineated in the column ten of our envisaged trust-based IoV dataset.

# Experimental Design, Materials and Methods

It is pertinent to highlight that, as of date, no publicly accessible trust-based IoV dataset has been particularly designed for detecting trust-based attacks. Therefore, the dataset envisaged in this manuscript makes a pioneering contribution to this specific domain. For the purpose of generating the said dataset, Java has been employed to develop an IoV simulator that employed a realistic urban traffic scenario encompassing multiple interconnected road segments, i.e., of Shenzhen, Guangdong Province, P. R. China. A total of 96 vehicles, i.e., trustworthy and intelligent malicious, have been instantiated and subsequently facilitated for interaction in the said traffic scenario, wherein vehicles move at random speeds along different trajectories. Each vehicle maintains a constant speed along a single trajectory and changes its respective speed on switching to a new trajectory. In doing so, they interact with other vehicles in their immediate neighborhood. Accordingly, each interaction is quantified via four salient trust parameters, i.e., experience of interaction, frequency of interaction, timeliness of interaction, and quality of received messages, at each time instance. Specifically, the intelligent malicious vehicles are programmed to carry out trust-based attacks, i.e., on-off attacks (an intelligent malicious vehicle alternates between honest and dishonest modes), self-promoting attacks (an intelligent malicious vehicle colludes to enhance its respective reputation for gaining significant privileges), and opportunistic attacks (an intelligent malicious vehicle gains considerable trust of vehicles interacting with it and subsequently finds an opportunity to harm them).

# A specimen of the envisaged trust-based IoV dataset encompassing the trust parameters and labels.
| Trustor | Trustee | Interaction Experience  |Interaction Frequency| Interaction Timeliness| Received Message Quality |MaliciousVehicle | IsAttacking| 
| :------: |  :----:  | :-------:| :------: | :----: | :------: |:------: | :----: | 
|0|8|1.000|0.500|1.000|1.000|No|No|
|0|24|0.400|0.143|1.000|0.600|No|No|
|0|92|0.800|0.071|1.000|0.800|No|No|
|.|.|.|.|.|.|.|.|.|
|10|15|0.900|0.111|1.000|1.000|No|No|
|10|57|0.300|0.001|0.244|0.600|No|No|
|10|81|0.600|0.100|1.000|0.600|No|No|
|.|.|.|.|.|.|.|.|.|
|19|20|0.300|0.013|0.653|0.600|No|No|
|19|25|0.300|0.006|0.326|0.600|No|No|
|19|92|0.800|0.125|1.000|0.800|No|No|
|.|.|.|.|.|.|.|.|.|
|24|32|0.300|0.019|0.763|0.600|No|No|
|24|81|0.500|0.143|1.000|0.600|No|No|
|24|93|0.500|0.111|1.000|0.600|No|No|
|.|.|.|.|.|.|.|.|.|
|36|39|0.500|0.012|1.000|0.600|No|No|
|36|61|0.300|0.001|0.249|0.600|No|No|
|36|89|0.400|0.002|0.498|0.600|No|No|
|.|.|.|.|.|.|.|.|.|
|42|58|0.700|0.111|1.000|0.800|No|No|
|42|75|0.600|0.022|1.000|0.600|No|No|
|42|90|0.400|0.007|0.965|0.600|No|No|
|.|.|.|.|.|.|.|.|.|
|61|63|1.000|0.048|1.000|1.000|No|No|
|61|82|0.400|0.005|0.684|0.600|No|No|
|61|93|0.700|0.097|1.000|0.800|No|No|
|.|.|.|.|.|.|.|.|.|
|73|75|0.900|0.098|1.000|1.000|No|No|
|73|76|0.800|0.267|1.000|0.800|No|No|
|73|87|1.000|0.048|1.000|1.000|No|No|
|.|.|.|.|.|.|.|.|.|
|80|81|0.400|0.012|0.895|0.600|Yes|Yes|
|80|88|0.900|0.226|1.000|1.000|Yes|No|
|80|93|0.800|0.173|1.000|0.800|Yes|Yes|
|.|.|.|.|.|.|.|.|.|
|85|87|0.300|1.000|0.392|0.600|Yes|Yes|
|85|92|0.700|0.268|0.941|0.800|Yes|Yes|
|85|95|0.700|0.031|0.521|0.800|Yes|Yes|
|.|.|.|.|.|.|.|.|.|
|90|91|0.700|0.243|1.000|0.800|Yes|Yes|
|90|93|0.300|0.074|1.000|0.600|Yes|No|
|94|95|0.600|1.000|1.000|0.600|Yes|Yes|
