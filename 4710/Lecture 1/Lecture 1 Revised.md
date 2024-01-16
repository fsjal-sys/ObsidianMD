# A Basic Introduction to Network Security

## What is Network Security?
Network Security refers to the domain of securing computer networks from threats. It is a subset of **Computer Security**, involving any activity designed to protect the usability and integrity of an organisation's network and data. 
### Importance of Network Security
Organisations need computers to perform their operations. Computers are devices which are used to efficiently process data. In a corporate office, workers can create documents and keep track of important information using computers. Computers also allow them to communicate with their co-workers or their bosses. In a school, computers are used to keep track of the students' classes and grades by storing that information in databases. Computers are also useful in educating students. At a cafe business, a computer is used to track orders and employee wages. The cafe might even provide its customers with Wi-Fi access, so that the customers can make better use of their own personal computers when they are within the cafe establishment. Ultimately, computers allow us to read and alter data which is very useful in getting our work done.

There are times when it will be in our interest to exert a desired level of control over the data that our computers process. If we go back to the corporate office example, we can assume that the office is probably using a computer to store important information about its employees. This information is valuable to both the organisation as a whole and the employees who work for the organisation. The organisation needs this information to manage its employees and the employees value this information because there can be a lot of risk if this information ends up in the wrong hands i.e. a criminal could use this information to impersonate and commit fraud. Computers process data which are valued by people and organisations. The value of this data incentivises people and organisations to invest in securing this data i.e. organisations have an incentive for **Computer Security**.

Organisations possess multiple computers, which transfer data with each other regularly. These computers which all transfer data with each other will collectively form an organisation's network. If an organisation acquires a new computer, that computer will become a part of its exclusive network and it will gain the ability to exchange data with the other computers on the network. It gains a foothold into the organisation's network, allowing it to have the ability of accessing the organisation's valued data. If a network is capable of exposing valued data to new computers as long as those computers join the network, then the organisation will have an incentive to secure the network. **The organisation wants to secure its computer data which also entails wanting to secure the network that those computers are a part of.** Organisations have an incentive for **Network Security**. Network Security is a subset of Computer Security, concerned with accomplishing the goals of Computer Security through the securing of the network.

Computer Security is concerned fundamentally with the security of data on a computer system. Network Security is more specific, concerning itself with a set of technologies that protect the usability and integrity of a company's infrastructure by preventing the entry or proliferation within a network by an unauthorised entity.
## Network Layers and Related Attacks
When a system is being attacked, the attacks correspond with the network layers involved with the system. When we talk about network layers, we are referring to the classifications laid out by the **OSI Model** and the **TCP/IP Model**. The OSI model is a conceptual guideline for interpreting computer networking. When we analyse something in a computer which involves networking, we can refer to the OSI model or the TCP/IP Model to help us better understand it in more depth by figuring out which layer is in correspondence.

The layers of the OSI Model and the TCP/IP Model are shown in the diagram below:
![[1.png]]
As you can see in the diagram, each layer corresponds with a number of protocols. These protocols are sets of rules which allow services to run on each layer. For example, the HTTP protocol establishes rules for displaying webpages. It is a protocol that exists on the Application Layer of the OSI and TCP/IP Model. If we are analyzing a web browser which is fetching webpages (which uses the HTTP protocol), then we can refer to the OSI Model and/or the TCP/IP model to establish that this is service which exists on the Application Layer.

Similarly if there is an attack on a webpage, then we can refer to the OSI Model and the TCP/IP model to establish the attack as an Application Layer attack. 

Let's take the point of view of an attacker. Suppose that an attacker wants to attack a website. Websites consist of webpages, and the HTTP protocol is the set of rules which allow those webpages to be fetched by browsers. The HTTP protocol corresponds with the Application Layer. So if we want to devise an effective attack then we will want to understand the Application Layer more deeply, as our attack will have to be designed for the Application Layer.

Let's take the point of a defender. Suppose that we want to defend a website hosted on a system from attacks. Obviously classifying these attacks would be an important step. The website is what we are trying to defend and websites exist on the Application Layer, so we will devise a line of defence specifically for the Application Layer.

This is the importance of the OSI Model and the TCP/IP Model when it comes to Network Security. These models allow us to classify the different components which make a system's networking capabilities. Attacks on networks are going to involve these different components, so both attackers and defenders can refer to these models to help them accomplish their respective security goals.

## Basic Computer Security Concepts

#### Computer Security and Network Security
Network Security and Computer Security are not necessarily the same things. Networking Security can be thought of as a subset of Computer Security. We can think of this relationship similarly to the relationship between the English language and writing. Writing is an important aspect of the English language, but it is a subset of the English language. The English language is a broader concept which does not just consist of writing. For example, speaking is also an important aspect of the English language yet it is separate from writing. Similarly, Network Security is an important aspect of Computer Security, but Computer Security is a more broad concept which encompasses Network Security. Just like with English writing, one should have the necessary prerequisite knowledge of the broader English language in order to effectively understand how to write in the English language. When it comes to Network Security, having a basic understanding of Computer Security will make it more effective for one to understand Network Security.

According to the NIST Computer Security Handbook, Computer Security is defined as:
"The protection afforded to an automated information system to attain the applicable objectives of preserving the integrity, availability, and confidentiality of information system resources (hardware, software, firmware, information/data, and telecommunications)."

Prior to the widespread use of data processing equipment, the security of valuable information on a computer system was primarily concerned with physical security. If you had a computer with important data on it but no networking involved, then the only possible ways to access that data would be physically. Maybe you would physically operate the computer or transfer the data onto a physical storage medium. Computer Security is fundamentally concerned with the **security of data** on a computer system. That is how the concept of Computer Security originated, with the protection of data as a priority even prior to the proliferation of computer networks. Internet Security on the other hand is more specific with the protection of data. It does not merely concern the protection of data in general, rather the protection of the transmission of data over the Internet. Internet Security consists of the **measures to deter, prevent, detect, and correct security violations that involve the transmission of information.**

Computer security is concerned fundamentally with the security of data on a computer system. Network Security is more specific, concerning itself with a set of technologies that protect the usability and integrity of a company's infrastructure by preventing entry or proliferation within a network of a wide variety of potential threats. Network Security is **any activity designed to protect the usability and integrity of an organization's network and data, including hardware and software technologies.**

## Model for Network Security
#### Computer Security Objectives
The CIA triad is a very common model used to identify the objectives in securing a computer system. The CIA triad consists of three major domains for which the acronym CIA is formed: Confidentiality, Integrity, and Availability. A more comprehensive model adds two more major domains: Accountability and Authenticity. We will outline each domain briefly:
Confidentiality:
- Data confidentiality assures that private or confidential information is not disclosed to **unauthorized** individuals.
Integrity:
- Data integrity assures that data can only be altered in an authorized manner. Data cannot be tampered with or changed by **unauthorized** individuals or by **unauthorized** processes.
Availability:
- Data availability assures that data is available to be accessed by authorized individuals or processes. There cannot be any denial of service or limitation of the data's availability.
Accountability:
- Accountability assures that the actions of an entity in a system are traced in such a way where the actions of an entity can be uniquely identified with that particular entity.
Authenticity:
- Authenticity verifies that users are who they say are and that each input entering a system comes from a trusted source.

#### Breach of Security - Levels of Impact
When the security of a system is breached, we will want to understand the impact of the breach in order to mitigate the effects of the attack. Generally, there are three levels of impact:
1. High Impact
	- The loss of the organization as a result of the security breach is expected to have severe consequences on the organization's operations, their assets, and/or individuals associated.
	- An example might be a breach which resulted in the unauthorized transfer of an organization's employee database to an unknown system. This database contains employees' addresses, social security numbers, and other personally identifiable information. This has severe consequences for the organization's employees and the organization's operations, making this security breach have a high impact.
1. Moderate Impact
	- The loss of the organization as a result of the security breach is expected to have serious consequences on the organization's operations, assets, and/or individuals associated.
	- An example might be a strong DDOS attack on an organization built around a social media website. The organization's operations heavily revolve around the servicing of this website to users, so if the website is forced to go offline for a long time due to a sophisticated DDOS attack then it can be assumed that the organization's operations and asset (the asset being the website) have been severely impacted. However, this situation is still resolvable as opposed to a high impact which can have more permanent consequences.
1. Low Impact
	- The loss of the organization as a result of the security breach is expected to have limited consequences on the organization's operations, assets, and/or individuals associated.
	- An example might be a DDOS attack on the website of a large retailer such as Walmart. Suppose that this DDOS attack only effects the Walmart servers which are responsible for the online Walmart career applications. Walmart's most valuable assets are it's real estate, merchandise, etc. It isn't tied to the availability of a website. On top of that, Walmart can hire employees by hosting in-person hiring events so they do not need to rely solely on online applications for the purpose of acquiring new employees. This DDOS attack is also likely to be resolved appropriately as Walmart likely has an established cyber security team. The impact of this security breach does not severely effect the organization at all, thus it has a low impact.
## OSI Security Architecture
The OSI Security Architecture defines a systematic approach to providing security at each layer of the OSI model. It involved defining **security services** and **security mechanisms** which can be present at each layer to provide effective security against attacks which occur in those respective layers.
#### Security Attacks
As we defined it earlier, security attacks are basically any action which compromises the security of data which is valued by an organization. If there is an action which effects the confidentiality, integrity, availability, authenticity, and/or accountability of data which is valued by an organization, then we can confidently classify it as a security attack.

Generally there are two sub-classifications of security attacks: **passive** and **active**.

A **passive attack** is any action concerned with acquiring information from a system without directly affecting the system. Passive attacks can be a form of reconnaissance on a target, acquiring knowledge of a system's potential vulnerabilities prior to actively attacking the system. 
Thus we can say that passive attacks are in the nature of eavesdropping on or monitoring transmissions. The goal of the attacker when carrying out a passive attack is to obtain information that is being transmitted.
Two types of passive attacks are the release of message contents and traffic analysis. When it comes to the release of message contents, an unauthorized party may conduct a passive attack when the exposure of the transmission contents are disclosed to that unauthorized party. Traffic analysis if another form of a passive attack which focuses more on observing patterns, volumes and the behaviours of data transmissions without necessarily understanding the specific message contents. So with the release of message contents, the attacker's main objective is to intercept and read the actual message contents being transmitted. With traffic analysis, the attacker's main objective is to derive meaningful information from the analysis of traffic patterns, such as identifying communication patterns, user behaviours, and/or system vulnerabilities.
Specific techniques used in passive attacks are listed below:
1. Eavesdropping
	- The unauthorized interception of communications in order to read the actual contents of the message being transmitted i.e. the unauthorized release of of message contents.
2. IP Spoofing
     - The falsifying of the source address in a network packet to make it appear as if it originated from a source which it did not originally come from. 
4. Packet Sniffing
	- The capturing and analyzing of network packers in order to access and understand the data being transmitted. This can be thought of as a specific form of eavesdropping.
5. Tapping
	- The physical interception of actual communications cables or network devices in order to gain unauthorized access to the data that is being transmitted through those communications cables.
6. Traffic Analysis
	- The analysis of patterns in data transmissions to deduce information about the communications flow, even without understanding the actual content. More concerned with deriving information from how the content is presented.

An **active attack** is such that attempts to actually alter the system resources. As opposed to a passive attack which would attempt to acquire knowledge about the vulnerabilities of a system, an active attack would involve the actual exploitation of those vulnerabilities.
Unlike a passive attack, active attacks will always involve some kind of modification of the data stream or the creation of a false stream. These attacks are difficult to prevent due to the wide variety of possible attack surfaces and the wide variety of potential physical, software, and network vulnerabilities. 
Some specific types of active attacks include:
1. Masquerade
    - A masquerade attack involves the attacker pretending to be someone who they actually are not, in order to somehow alter the system in unauthorized manner. 
3. Replay
	- A replay involves the passive capture of a data unit and its subsequent retransmission to produce and unauthorized effect onto the system.
4. Modification of Messages
	- The modification of messages occurs when some portion of a legitimate message is altered or messages are delayed or reordered to produce and unauthorized effect.
5. Denial of Service
    - The denial of service inhibits the normal use of a service on a network by diminishing its ability to communicate with users, usually through exhausting the network's capabilities.

#### Security Services
So we have established that a **security attack** can be defined as any action which compromises the security of the information which is valued by an organisation. **Security solutions** are the solutions that organisations can implement in order to curtail security attacks. Security solutions involve **security services** and **security mechanisms**. 
- **Security Service:** The processing or communication service which enhances the security of the data processing systems and the information transfers of an organisation. These services are intended to counter against security attacks.
- **Security Mechanism:** The process that is designed to detect, prevent, or recover from a security attack. 
These security solutions are meant to be solutions to the problems posed by security threats and security attacks. As defined by the RFC 4949 document:
- **Threat**: A potential violation of security which existed where there is a circumstance, capability, action, or event that could breach security and cause harm. A thread is a possible danger that might exploit a vulnerability.
- **Attack**: An assault on system security that derives from an intelligent threat. An intelligent act that is a deliberate attempt to evade security services and violate the security policy of a system.

A security service is a specific service deployed by an organisation to enhance the security on their network. Just like how networks have many services present within them, such as the HTTP service for providing access to webpages or the FTP service for providing means to transfer files, networks can also have security services which provide better security to the network.

**The X.800 framework from the OSI Security Architecture** defines a security service as:
- A service provided by a protocol layer of communicating open systems which ensures an adequate security of the systems or of the data transfers within an open systems network.
- The OSI Model conceptualises a communications system as consisting of several layers. A security service is a dedicated feature within these layers which ensures that the systems and the data they transfer are adequately protected against unauthorised security attacks and their consequences.
**The RFC 4949 document published by the IETF (Internet Engineering Task Force)** defines a security service as:
- A processing or communication service which is provided by the system to give a specific kind of protection to system resources.
- The RFC 4949 documents implies that security services are services that actively run on a network in order to safeguard the system resources.

##### Security Services Categories
Since there is a wide variety of potential network security risks, then there must also be a variety of security services to actively protect against these security risks. We can categorise security services as follows:
1. Authentication
2. Access Control
3. Data Confidentiality
4. Data Integrity
5. Availability
6. Nonrepudiation

**Authentication**
Authentication security services are concerned with the assurance that a communication within a network is authentic i.e. the message source is not obscured and is the true source. In the case of a single message, an authentication security service must assure the recipient that the message is from the source which the message claims to be from. In the case of an ongoing interaction, an authentication security service assures that the two entities are authentic and that the connection is not being interfered with by an unauthorised party. A third party cannot be allowed to masquerade as one of the two legitimate parties.

**Access Control**
Access control security services are committed to limiting and control the access to host systems and applications through communications links. To achieve this, each entity trying to gain access to a host must first be authenticated and have their access rights be tailored specifically based on the user's specific type of authorisation.

**Data Confidentiality**
Data confidentiality security services are meant to ensure the protection of transmitted data from passive attacks. A passive attack is an attack concerned with the unauthorised revealing or reading of data. A data confidentiality security service wants to make sure that the data is kept confidential so that it is only restricted to authorised parties. Data confidentiality security services can even prevent an attack from being unable to observe the source, destination, and other information regarding the traffic on a network.

**Data Integrity**
Data integrity security services ensure the integrity of data on their network. They make sure that the data on the network is not altered or modified by an unauthorised third party. This can apply to a stream of messages, a single message, or elected fields within a message. A **connection-oriented** integrity service deals with a stream of messages and assures that messaged are received as sent with no duplication, insertion, modification, rendering or replays. A **connectionless** integrity service deals with individual messages without regard to any larger context, protecting against message modification only.

**Availability**
Availability security services ensure that the property of a system or a system resource is made available to be accessed upon demand by an authorised system entity. A common attack which these services protect against are DDOS attacks.

**Non-repudiation**
Non-repudiation security services prevent either sender or receiver from denying a transmitted message. When a message is sent, the receiver can prove that the alleged sender did actually send that message. Likewise, the sender can prove that the recipient did actually receive the message.

#### Security Mechanisms
We have established that security services are meant to actively enhance the security of a system. However, these services must be implemented into the system in the first place. This is where the security mechanisms come into play, they are methods, tools, or processes which actually implement and enforce the security services. A particular security mechanism is capable of enforcing several security services. Think about how fast food is a service, and a fast food establishment consists of many different employees under different types of roles. These employees work to actually provide their respective fast food services. A cashier provides the service of transactions, allowing customers to make purchases. The fry cooks implement the creation of the menu items, allowing for the customers to be served. A security service is a broader security enhancement which must be implemented by a security mechanism. A particular security mechanism may implement or enforce several different security services. This is illustrated in the diagram below:
![[2.png]]

Security services and the security mechanisms which implement those services, are meant to ensure the security of a system from security threats and attacks. When designing a secure system, the security services and security mechanisms must be taken into account. The National Centres of Academic Excellence in Information Assurance/Cyber Defence, list the following as fundamental security design principles:
- Economy of Mechanism
- Fail-sage defaults
- Complete mediation
- Open design separation of privilege
- Least privilege
- Least common mechanism
- Psychological acceptability
- Isolation
- Encapsulation
- Modularity
- Layering
- Least astonishment
These design principles limit the **attack surfaces** that will be present in a system. An attack surface is a reachable and exploitable vulnerability in a system. 

Examples include: 
- An open port on an outward facing web server is a surface which is made reachable to external users. This web server is a part of the organisation's network which is reachable, making it a potential attack surface. 
- Services available on the inside of a firewall.
- Code that processes incoming data, email, XLM, office documents, and industry-specific custom data exchange formats.
- Interfaces SQL, and web forms.
- An employee with access to sensitive information vulnerable to a social engineering attack.

We can categorise attack surfaces:
- **Network Attack Surface**: Attack surfaces which are reachable over an enterprise network, wide-area network, or the Internet.
- **Software Attack Surface**: Attack surfaces which are reachable in the software of an organisation. These are vulnerabilities that exist in the applications, utilities, or operating system code.
- **Human Attack Surface**: Attack surfaces which are reachable through the personnel associated with the organisation. These vulnerabilities include social engineering, human error, and trusted insiders.

The risks involved with attack surfaces can depend on the layering implemented in a system. This is illustrated in he diagram below:![[3.png]]

When a system is attacked, there is a sequence of actions that usually unfold relative to the particular scenario. An **attack tree** is used to portray these sequences by breaking down and analysing the different paths that an attacker might take to compromise a system or achieve a specific goal. 
- Attack trees are represented by branching hierarchical data structures which showcase the **set of potential techniques for exploiting** security vulnerabilities.
- The **security incident** is represented in an attack tree as the root node. A security incident is the goal of the attack.
- The different ways that the attacker can reach that goal are iteratively and incrementally represented as branches and subnodes of the attack tree.
- The final nodes on the oaths outward from the root, the leaf nodes, represent the different ways that the attacker may initiate the attack.
- Branches can be labelled with values representing the difficulty, cost, or other attributes, so that alternative attacks can be compared.

#### Security Standards
The most popular sets of security standards include the NIST (National Institute of Standards and Technology) and ISOC (Internet Society) standards. 

**NIST**:
- NIST is a U.S. federal agency that deals with the measurement science, standards, and technology related to the U.S. government's uses and the promotion of U.S. private-sector innovation.
- NIST Federal Information Processing Standards (FIPS) and Special Publications (SP) have a worldwide impact.
**ISOC**:
- ISOC is a professional membership society with worldwide organisational and individual membership.
- Provides leadership in addressing issues that confront the future of the Internet and is home to the groups responsible for Internet infrastructure standards, including the IETF and the IAB.
- ISOC publishes Internet standards and related specifications as RFS (Requests for Comments).