## Summary
- ### Computer Security Concepts
	- Definition, Examples, Challenges
- ### OSI Security Architecture
- ### Security Attacks
	- Passive Attacks, Active Attacks
- ### Model for Network Security
- ### Network Security Standards
- ### Security Services
	- Authentication, Access Control
	- Data Confidentiality, Integrity, Availability
	- Nonrepudiation
- ### Security Mechanisms
- ### Attack Surfaces and Attack Trees

<hr>

## Network Layers and Related Attacks
When a system is being attacked, the attacks correspond with the network layers involved with the system. When we talk about network layers, we are referring to the classifications laid out by the **OSI Model** and the **TCP/IP Model**. The OSI model is a conceptual guideline for interpreting computer networking. When we analyze something in a computer which involves networking, we can refer to the OSI model or the TCP/IP Model to help us better understand it in more depth by figuring out which layer is in correspondence.

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

A **security attack** can be defined as any action which compromises the security of the information which is valued by an organization. **Security solutions** are the solutions that organizations can implement in order to curtail security attacks. Security solutions involve **security services** and **security solutions**. 
- **Security Service:** The processing or communication service which enhances the security of the data processing systems and the information transfers of an organization. These services are intended to counter against security attacks.
- **Security Mechanism:** The process that is designed to detect, prevent, or recover from a security attack. 

#### Security Attacks
As we defined it earlier, security attacks are basically any action which compromises the security of data which is valued by an organization. If there is an action which effects the confidentiality, integrity, availability, authenticity, and/or accountability of data which is valued by an organization, then we can confidently classify it as a security attack.

Generally there are two sub-classifications of security attacks: **passive** and **active**. A **passive attack** is any action concerned with acquiring information from a system without directly affecting the system. Passive attacks can be a form of reconnaissance on a target, acquiring knowledge of a system's potential vulnerabilities prior to actively attacking the system. An **active attack** is such that attempts to actually alter the system resources. As opposed to a passive attack which would attempt to acquire knowledge about the vulnerabilities of a system, an active attack would involve the actual exploitation of those vulnerabilities.

