# Table of Contents
# 목차

- [x]	1. Introduction
- [x]	________1.1. Purpose
- [x]	________1.2. Scope
- [x]	________1.3. Definitions, Acronyms, and Abbreviations
- [x]	________1.4. References
- [ ]	________1.5. Overview
- [ ]	2. The Overall Description
- [ ]	________2.1. Product Perspective
- [ ]	________________2.1.1. System Interfaces
- [ ]	________________2.1.2. Interfaces
- [ ]	________________2.1.3. Hardware Interfaces
- [ ]	________________2.1.4. Software Interfaces
- [ ]	________________2.1.5. Communications Interfaces
- [ ]	________________2.1.6. Memory Constraints
- [ ]	________________2.1.7. Operations
- [ ]	________________2.1.8. Site Adaptation Requirements
- [ ]	________2.2. Product Functions
- [ ]	________2.3. User Characteristics
- [ ]	________2.4. Constraints
- [ ]	________2.5. Assumptions and Dependencies
- [ ]	________2.6. Apportioning of Requirements  
- [ ]	3. Specific Requirements
- [ ]	________3.1. External Interfaces
- [ ]	________________3.1.1. User Interfaces
- [ ]	________________3.1.2. Hardware Interfaces
- [ ]	________________3.1.3. Software Interfaces
- [ ]	________________3.1.4. Communications Interfaces
- [ ]	________3.2 Use Case Descriptions
- [ ]	________________3.2.1 Use Case 1
- [ ]	________________3.2.1 Use Case 2
- [ ]	________________3.2.1 Use Case n
- [ ]	________3.3. Performance Requirements
- [ ]	________3.4. Design Constraints
- [ ]	________3.5. Software System Attributes
- [ ]	________________3.5.1. Reliability
- [ ]	________________3.5.2. Availability
- [ ]	________________3.5.3. Security
- [ ]	________________3.5.4. Maintainability
- [ ]	________________3.5.5. Portability
- [ ]	________3.6. Other Requirements
- [ ]	4. Change Management Process
- [ ]	5. Document Approvals  
- [ ]	6. Supporting Information  
  
--

# 1. Introduction
# 1. 소개

	Introduction for this document.

## 	1.1 Purpose
##  1.1 목적

	The purpose of this document is to give a detailed description of the requirements for the "transChat".
	It will illustrate the purpose and features of the system, the interfaces of the system, what the system will do.
	It will also explain system constraints.
	This document is primarily intended to give developers a reference for developing the first version of program.

## 	1.2 Scope
##  1.2 범위
	The "transChat" is a web-based chatting application which gives the translation of the message.
	"transChat"은 메세지 번역 기능이 있는 웹 기반의 채팅 어플리케이션이다.
	This application will use translation API(google or NAVER).
	이 어플리케이션은 구글 또는 네이버의 번역 API를 사용할 계획이다.
	If it uses Naver translator API, then it only gives the translation between Korean and Japanese or Chinese.
	네이버 번역 API를 사용하게 될 경우, 한국어, 일본어, 중국어 간의 번역만을 제공 할 것이다.
	And can't give the translation between Japanese and Chinese.
	또한 일본어와 중국어 간의 번역을 제공하지 않는다.
	Once one of the users types a message and sends it to others, the message will be translated to others under the original message.
	사용자가 다른 사용자에게 메세지를 보내면, 원 메세지의 아래에 메세지가 번역되어진다.

## 	1.3 Definitions, Acronyms, and Abbreviations
##  1.3 정의, 두음문자, 약어

|Term|Definition|
|---------|:-------------------------------:|
|API|Application Program Interface|
| | |

## 	1.4 References
##  1.4 참고

	[1] IEEE Guide to Software Requirements Specifications (Std 830-1993)

## 	1.5 Overview
##  1.5 개요

	In this subsection:
		(1)	Describe what the rest of the SRS contains
		(2)	Explain how the SRS is organized

	Don’t rehash the table of contents here.  Point people to the parts of the document they are most concerned with.  Customers/potential users care about section 2, developers care about section 3.

# 2 The Overall Description

	Describe the general factors that affect the product and its requirements.  This section does not state specific requirements.  Instead, it provides a background for those requirements, which are defined in section 3, and makes them easier to understand. In a sense, this section tells the requirements in plain English for the consumption of the customer.  Section3 will contain a specification written for the developers.

## 	2.1  Product Perspective

	Put the product into perspective with other related products.   If the product is independent and totally self-contained, it should be so stated here.  If the SRS defines a product that is a component of a larger system, as frequently occurs, then this subsection relates the requirements of the larger system to functionality of the software and identifies interfaces between that system and the software.  If you are building a real system,compare its similarity and differences to other systems in the marketplace.  If you are doing a research-oriented project, what related research compares to the system you are planning to buil
	A block diagram showing the major components of the larger system, interconnections, and external interfaces can be helpful.  This is not a design or architecture picture.  It is more to provide context, especially if your system will interact with external actors.  The system you are building should be shown as a black box.  Let the design document present the internals.

 The following subsections describe how the software operates inside various constraints.

### 		2.1.1 System Interfaces

	List each system interface and identify the functionality of the software to accomplish the system requirement and the interface description to match the system.  These are external systems that you have to interact with.  For instance, if you are building a business application that interfaces with the existing employee payroll system, what is the API to that system that designer’s will need to use?

### 		2.1.2 Interfaces

	Specify:
		(1)	The logical characteristics of each interface between the software product and its users.
		(2)	All the aspects of optimizing the interface with the person who must use the system

	This is a description of how the system will interact with its users.  Is there a GUI, a command line or some other type of interface?  Are there special interface requirements?  If you are designing for the general student population for instance, what is the impact of ADA (American with Disabilities Act) on your interface?
	
### 		2.1.3 Hardware Interfaces

	Specify the logical characteristics of each interface between the software product and the hardware components of the system.  This includes configuration characteristics.  It also covers such matters as what devices are to be supported, how they are to be supported and protocols.  This is not a description of hardware requirements in the sense that “This program must run on a Mac with 64M of RAM”.  This section is for detailing the actual hardware devices your application will interact with and control.  For instance, if you are controlling X10 type home devices, what is the interface to those devices?  Designers should be able to look at this and know what hardware they need to worry about in the design.  Many business type applications will have no hardware interfaces.  If none, just state “The system has no hardware interface requirements”  If you just delete sections that are not applicable, then readers do not know if:  a. this does not apply or b.  you forgot to include the section in the first place. 

### 		2.1.4 Software Interfaces

	Specify the use of other required software products and interfaces with other application systems.  For each required software product, include:
		(1)	Name
		(2)	Mnemonic
		(3)	Specification number
		(4)	Version number
		(5)	Source

	For each interface, provide:
		(1)	Discussion of the purpose of the interfacing software as related to this software product
		(2)	Definition of the interface in terms of message content and format

	Here we document the APIs, versions of software that we do not have to write, but that our system has to use.  For instance if your  customer uses SQL Server 7 and you are required to use that, then you need to specify i.e.
	
	2.1.4.1 Microsoft SQL Server 7.  The system must use SQL Server as its database component.  Communication with the DB is through ODBC connections.  The system must provide SQL data table definintions to be provided to the company DBA for setup.

	A key point to remember is that you do NOT want to specify software here that you think would be good to use.  This is only for customer-specified systems that you have to interact with.  Choosing SQL Server 7 as a DB without a customer requirement is a Design choice, not a requirement. This is a subtle but important point to writing good requirements and not over-constraining the design.
	 
### 		2.1.5 Communications Interfaces

	Specify the various interfaces to communications such as local network protocols, etc.  These are protocols you will need to directly interact with.  If you happen to use web services transparently to your application then do not list it here.  If you are using a custom protocol to communicate between systems, then document that protocol here so designers know what to design.  If it is a standard protocol, you can reference an existing document or RFC.

### 		2.1.6 Memory Constraints

	Specify any applicable characteristics and limits on primary and secondary memory. Don’t just make up something here.  If all the customer’s machines have only 128K of RAM, then your target design has got to come in under 128K so there is an actual requirement.  You could also cite market research here for shrink-wrap type applications “Focus groups have determined that our target market has between 256-512M of RAM, therefore the design footprint should not exceed 256M.”  If there are no memory constraints, so state.

### 		2.1.7 Operations

	Specify the normal and special operations required by the user such as:
		(1)	The various modes of operations in the user organization
		(2)	Periods of interactive operations and periods of unattended operations
		(3)	Data processing support functions
		(4)	Backup and recovery operations 

	(Note:  This is sometimes specified as part of the User Interfaces section.)  If you separate this from the UI stuff earlier, then cover business process type stuff that would impact the design.  For instance, if the company brings all their systems down at midnight for data backup that might impact the design.  These are all the work tasks that impact the design of an application, but which might not be located in software. 

### 		2.1.8 Site Adaptation Requirements

	In this section:
		(1)	Define the requirements for any data or initialization sequences that are specific to a given site, mission, or operational mode
		(2)	Specify the site or mission-related features that should be modified to adapt the software to a particular installation

	If any modifications to the customer’s work area would be required by your system, then document that here.  For instance, “A 100Kw backup generator and 10000 BTU air conditioning system must be installed at the user site prior to software installation”.
	This could also be software-specific like, “New data tables created for this system must be installed on the company’s existing DB server and populated prior to system activation.”  Any equipment the customer would need to buy or any software setup that needs to be done so that your system will install and operate correctly should be documented here.

## 	2.2  Product Functions

	Provide a summary of the major functions that the software will perform. Sometimes the function summary that is necessary for this part can be taken directly from the section of the higher-level specification (if one exists) that allocates particular functions to the software product.
	For clarity:
		(1)	The functions should be organized in a way that makes the list of functions understandable to the customer or to anyone else reading the document for the first time. 
		(2)	Textual or graphic methods can be used to show the different functions and their relationships.  Such a diagram is not intended to show a design of a product but simply shows the logical relationships among variables.

	AH, Finally the real meat of section 2.  This describes the functionality of the system in the language of the customer.  What specifically does the system that will be designed have to do?  Drawings are good, but remember this is a description of what the system needs to do, not how you are going to build it. (That comes in the design document). 

## 	2.3  User Characteristics 

	Describe those general characteristics of the intended users of the product including educational level, experience, and technical expertise.  Do not state specific requirements but rather provide the reasons why certain specific requirements are later specified in section 3.  

	What is it about your potential user base that will impact the design?  Their experience and comfort with technology will drive UI design.  Other characteristics might actually influence internal design of the system.

## 	2.4  Constraints  

	Provide a general description of any other items that will limit the developer's options.  These can include:

		(1)  Regulatory policies
		(2)  Hardware limitations (for example, signal timing requirements)
		(3)  Interface to other applications
		(4)  Parallel operation
		(5)  Audit functions
		(6)  Control functions
		(7)  Higher-order language requirements
		(8) 	Signal handshake protocols (for example, XON-XOFF, ACK-NACK)
		(9) 	Reliability requirements
		(10)  Criticality of the application
		(11) Safety and security considerations

	This section captures non-functional requirements in the customers language.  A more formal presentation of these will occur in section 3. 
	
## 	2.5 Assumptions and Dependencies

	List each of the factors that affect the requirements stated in the SRS.  These factors are not design constraints on the software but are, rather, any changes to them that can affect the requirements in the SRS.  For example, an assumption might be that a specific operating system would be available on the hardware designated for the software product.  If, in fact, the operating system were not available, the SRS would then have to change accordingly.

	This section is catch-all for everything else that might influence the design of the system and that did not fit in any of the categories above.
	
## 	2.6 Apportioning of Requirements

	Identify requirements that may be delayed until future versions of the system.  After you look at the project plan and hours available, you may realize that you just cannot get everything done.  This section divides the requirements into different sections for development and delivery.  Remember to check with the customer ? they should prioritize the requirements and decide what does and does not get done.  This can also be useful if you are using an iterative life cycle model to specify which requirements will map to which interation.

# 3. Specific Requirements  

	This section contains all the software requirements at a level of detail sufficient to enable designers to design a system to satisfy those requirements, and testers to test that the system satisfies those requirements.  Throughout this section, every stated requirement should be externally perceivable by users, operators, or other external systems.  These requirements should include at a minimum a description of every input (stimulus) into the system, every output (response) from the system and all functions performed by the system in response to an input or in support of an output. The following principles apply:

	(1)	Specific requirements should be stated with all the characteristics of a good SRS
		-	correct
		-	unambiguous
		-	complete
		-	consistent
		-	ranked for importance and/or stability
		-	verifiable
		-	modifiable
		-	traceable
	(2)	Specific requirements should be cross-referenced to earlier documents that relate
	(3)	All requirements should be uniquely identifiable (usually via numbering like 3.1.2.3)
	(4)	Careful attention should be given to organizing the requirements to maximize readability (Several alternative organizations are given at end of document)

	Before examining specific ways of organizing the requirements it is helpful to understand the various items that comprise requirements as described in the following subclasses.  This section reiterates section 2, but is for developers not the customer.  The customer buys in with section 2, the designers use section 3 to design and build the actual application.

	Remember this is not design.  Do not require specific software packages, etc unless the customer specifically requires them.  Avoid over-constraining your design.  Use proper terminology:
	The system shall…  A required, must have feature
	The system should… A desired feature, but may be deferred til later
	The system may…   An optional, nice-to-have feature that may never make it to implementation.

	Each requirement should be uniquely identified for traceability.  Usually, they are numbered 3.1, 3.1.1, 3.1.2.1 etc.  Each requirement should also be testable.  Avoid imprecise statements like, “The system shall be easy to use”  Well no kidding, what does that mean?  Avoid “motherhood and apple pie” type statements, “The system shall be developed using good software engineering practice”

	Avoid examples,  This is a specification, a designer should be able to read this spec and build the system without bothering the customer again.  Don’t say things like, “The system shall accept configuration information such as name and address.”  The designer doesn’t know if that is the only two data elements or if there are 200.  List every piece of information that is required so the designers can build the right UI and data tables.

## 	3.1 External Interfaces

	This contains a detailed description of all inputs into and outputs from the software system.  It complements the interface descriptions in section 2 but does not repeat information there. Remember section 2 presents information oriented to the customer/user while section 3 is oriented to the developer.

	It contains both content and format as follows:

		-	Name of item
		-	Description of purpose
		-	Source of input or destination of output
		-	Valid range, accuracy and/or tolerance
		-	Units of measure
		-	Timing
		-	Relationships to other inputs/outputs
		-	Screen formats/organization
		-	Window formats/organization
		-	Data formats
		-	Command formats
		-	End messages

## 	3.2 Use Case Descriptions

	Functional requirements define the fundamental actions that must take place in the software in accepting and processing the inputs and in processing and generating the outputs.  These are generally listed as “shall” statements starting with "The system shall…  

	These include:
		-	Validity checks on the inputs
		-	Exact sequence of operations
		-	Responses to abnormal situation, including
		-	Overflow
		-	Communication facilities
		-	Error handling and recovery
		-	Effect of parameters
		-	Relationship of outputs to inputs, including
		-	Input/Output sequences
		-	Formulas for input to output conversion


	It may be appropriate to partition the functional requirements into sub-functions or sub-processes.  This does not imply that the software design will also be partitioned that way.

## 	3.3 Performance Requirements

	This subsection specifies both the static and the dynamic numerical requirements placed on the software or on human interaction with the software, as a whole.  Static numerical requirements may include:
		(a)  The number of terminals to be supported
		(b)  The number of simultaneous users to be supported
		(c)  Amount and type of information to be handled
	Static numerical requirements are sometimes identified under a separate section entitled capacity.

	Dynamic numerical requirements may include, for example, the numbers of transactions and tasks and the amount of data to be processed within certain time periods for both normal and peak workload conditions.

	All of these requirements should be stated in measurable terms.

	For example,
	95% of the transactions shall be processed in less than 1 second
	rather than, 
	An operator shall not have to wait for the transaction to complete.

	(Note:  Numerical limits applied to one specific function are normally specified as part of the processing subparagraph description of that function.)
	
## 	3.4 Design Constraints

	Specify design constraints that can be imposed by other standards, hardware limitations, etc.

## 	3.5 Software System Attributes

	There are a number of attributes of software that can serve as requirements.  It is important that required attributes by specified so that their achievement can be objectively verified.  The following items provide a partial list of examples.  These are also known as non-functional requirements or quality attributes. 

	These are characteristics the system must possess, but that pervade (or cross-cut) the design.  These requirements have to be testable just like the functional requirements.  Its easy to start philosophizing here, but keep it specific.

### 		3.5.1 Reliability

	Specify the factors required to establish the required reliability of the software system at time of delivery.  If you have MTBF requirements, express them here.  This doesn’t refer to just having a  program that does not crash.  This has a specific engineering meaning.

### 		3.5.2 Availability

	Specify the factors required to guarantee a defined availability level for the entire system such as checkpoint, recovery, and restart.  This is somewhat related to reliability.  Some systems run only infrequently on-demand (like MS Word).  Some systems have to run 24/7 (like an e-commerce web site).  The required availability will greatly impact the design.  What are the requirements for system recovery from a failure?  “The system shall allow users to restart the application after failure with the loss of at most 12 characters of input”.   

### 		3.5.3 Security

	Specify the factors that would protect the software from accidental or malicious access, use, modification, destruction, or disclosure.  Specific requirements in this area could include the need to:
		-	Utilize certain cryptographic techniques
		-	Keep specific log or history data sets
		-	Assign certain functions to different modules
		-	Restrict communications between some areas of the program
		-	Check data integrity for critical variables

### 		3.5.4 Maintainability

	Specify attributes of software that relate to the ease of maintenance of the software itself.  There may be some requirement for certain modularity, interfaces, complexity, etc.  Requirements should not be placed here just because they are thought to be good design practices.  If someone else will maintain the system

### 		3.5.5 Portability

	Specify attributes of software that relate to the ease of porting the software to other host machines and/or operating systems.  This may include:
		-	Percentage of components with host-dependent code
		-	Percentage of code that is host dependent
		-	Use of a proven portable language
		-	Use of a particular compiler or language subset
		-	Use of a particular operating system

	Once the relevant characteristics are selected, a subsection should be written for each, explaining the rationale for including this characteristic and how it will be tested and measured.  A chart like this might be used to identify the key characteristics (rating them High or Medium), then identifying which are preferred when trading off design or implementation decisions (with the ID of the preferred one indicated in the chart to the right).  The chart below is optional (it can be confusing) and is for demonstrating tradeoff analysis between different non-functional requirements.  H/M/L  is the relative priority of that non-functional requirement.

|ID|Characteristic|H/M/L|1|2|3|4|5|6|7|8|9|10|11|12|
|---|:--------:|:-----:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|--:|
|1|Correctness||||||||||||||
|2|Efficiency||||||||||||||
|3|Flexibility||||||||||||||
|4|Integrity/Security||||||||||||||
|5|Interoperability||||||||||||||
|6|Maintainability||||||||||||||
|7|Portability||||||||||||||
|8|Reliability||||||||||||||
|9|Reusability||||||||||||||
|10|Testability||||||||||||||
|11|Usability||||||||||||||
|12|Availability||||||||||||||

	Definitions of the quality characteristics not defined in the paragraphs above follow.

		-	Correctness - extent to which program satisfies specifications, fulfills user’s mission objectives
		-	Efficiency - amount of computing resources and code required to perform function
		-	Flexibility - effort needed to modify operational program
		-	Interoperability - effort needed to couple one system with another
		-	Reliability - extent to which program performs with required precision
		-	Reusability - extent to which it can be reused in another application
		-	Testability - effort needed to test to ensure performs as intended
		-	Usability - effort required to learn, operate, prepare input, and interpret output

## 	3.6 Other Requirements

	Whenever a new SRS is contemplated, more than one of the organizational techniques given in 3.7 may be appropriate.  In such cases, organize the specific requirements for multiple hierarchies tailored to the specific needs of the system under specification. 

	Three are many notations, methods, and automated support tools available to aid in the documentation of requirements.  For the most part, their usefulness is a function of organization.  For example, when organizing by mode, finite state machines or state charts may prove helpful; when organizing by object, object-oriented analysis may prove helpful; when organizing by feature, stimulus-response sequences may prove helpful; when organizing by functional hierarchy, data flow diagrams and data dictionaries may prove helpful. 

	In any of the outlines below, those sections called “Functional Requirement i” may be described in native language, in pseudocode, in a system definition language, or in four subsections titled: Introduction, Inputs, Processing, Outputs.

# 4. Change Management Process
 
	Identify the change management process to be used to identify, log, evaluate, and update the SRS to reflect changes in project scope and requirements.  How are you going to control changes to the requirements.  Can the customer just call up and ask for something new?  Does your team have to reach consensus? How do changes to requirements get submitted to the team?  Formally in writing, email or phone call? 

# 5. Document Approvals

	Identify the approvers of the SRS document. Approver name, signature, and date should be used.

# 6. Supporting Information

	The supporting information makes the SRS easier to use.  It includes:
		-	Table of Contents
		-	Index
		-	Appendices

	The Appendices are not always considered part of the actual requirements specification and are not always necessary.  They may include:

		(a) Sample I/O formats, descriptions of cost analysis studies, results of user surveys
		(b) Supporting or background information that can help the readers of the SRS
		(c) A description of the problems to be solved by the software
		(d) Special packaging instructions for the code and the media to meet security, export, initial loading, or other requirements

	When Appendices are included, the SRS should explicitly state whether or not the Appendices are to be considered part of the requirements.
