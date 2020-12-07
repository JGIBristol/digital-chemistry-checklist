# How to make the most of a Chemical Synthesis robot

## Introduction

There is a growing appetite for Digital Chemistry. The Royal Society of Chemistry recently outlined their [FIXME X YEAR] plan for a Digital Future in Chemistry[FIXME REF], focusing on automating more chemical synthesis using robotics, and mining these high-throughput data sets using Artificial Intelligence (AI) and Machine Learning (ML). Meanwhile, IBM have released RoboRXN[FIXME, CITE], which uses AI to choose reagents and protocols to produce chemicals with desirable properties.

In contrast to RoboRXN, most robots for chemical synthesis are controlled by chemists (not AI), and are used to automate the time-consuming practical aspects of chemical synthesis: grinding, heating, shaking, etc. They can theoretically carry out 1000 times more experiments than their human lab-mates[REF: Kuka], creating more chemicals in both volume and variety. It's the data associated with these high-throughput experiments that can then form the input to AI algorithms, for chemical synthesis, drug discovery, and [FIXME OTHER EXAMPLES]. 

The installation of laboratory robots is only half the battle. ML algorithms require specific kinds of data to be feasible, and such data sets do not appear by accident. They can be very costly to produce[FIXME,CITE], for unsupervised as well as supervised learning. In fact, many agree that the field of data science is constrained by the lack of the right kinds of datasets[FIXME,CITE]. Companies who make use of data science, tend to have to spend more than 80% of their time on average on data preparation tasks[FIXME,CITE]. 

This is why it's important that we act quickly to begin capturing information in a useful format, in order to leverage them to make the most of the new possibilities in Digital Chemistry. This is particularly important, since Chemical synthesis robots are not cheap. With that in mind, this article aims to walk through the considerations for a research group who hope to go from using a Chemical Synthesis robot, to being prepared for this new interface between Data Science and Chemistry.

## The starting point
Let us begin by imagining a scenario where we have installed our new robotic friend and we have connected them to a computer which controls their movement with our computational instructions. Let's also assume that this same machine also collects any output data provided by the robot.

### Inputs and outputs

At this stage, for a single user and with one run of the robot, we are likely to have a few different types of inputs and outputs:

1. **Input chemicals**: the chemicals themselves and information about their provenance
2. **Robot instructions**: the input instructions to the machine
3. **Lab environment**: e.g. temperature in the lab, chemist operating the machine, etc.
4. **Context**: the purpose of this set of experiments in the context of a larger pipeline of research.
5. **Machine run log**: what actually happened during the experiments
6. **Output chemicals**: those sythesised by the robot.

Let's first assume a worst-case scenario for each of these sources of data as our starting point.

#### 1. Input Chemicals
We can assume that labs will have a Chemical Inventory System (CIS) of some form. This this will contain records of their chemicals, including name of the chemical, supplier, date acquired, hazard information and expiry date as a minimum. In the worst case scenario, it may be kept on paper. And if it is available in a computational format, then this information might be restricted to a small number of people such as the lab manager.

If the chemicals can be input to the robot in different ways, for example in a different order, or in different slots or locations, then this information may not be recorded, or may be recorded in a lab book by the chemist operating the robot.

#### 2. Robot instructions
In some way, the chemical synthesis robot must be told what to do. These instructions might created by users through interacting with buttons and menus using a Graphical User Interface, or written directly into a file. We will assume that this results in a file of some kind that the robot uses to carry out the experiment. This file may have a proprietary format, which may mean that the instructions are only readable to the specific robot's software, rather than being readable for other computer programs or humans without a license to the robot. 

#### 3. Lab environment
Some lab environment data may be collected by the robot, if it has inbuilt sensors. By default, it's likely that this information is lost, or collected in a lab book, which may not be digital.

#### 4. Context
By default, it's likely that this information is collected in a lab book (which may not be digital). If users submit jobs to the robot (which is operated by a technician), then it may not be the lab book of the person who is running the experiment - the experiment owner might not know who is operating the machine and vice versa.

#### 5. Machine run log
At a minimum the robot will output some information about what time it ran, what it did, and whether it's attempts were successful (i.e. the robot did not need to stop for some reason). More sophisticated technology might include information about the machine environment, e.g. if you told it to heat up a chemical to X degrees, what temperature did it actually reach inside the machine?

Similarly to (2), this information may be in a proprietary format.

#### 6. Output chemicals
Chemical synthesis robots create physical chemicals. These could come out of the machine in different locations or at different times, which may not be recorded. They could be labelled as a batch or individually by the user, and there may not be a set naming convention. 

After leaving the machine, they are likely to undergo downstream analysis (e.g. NMR), which will be different depending on the lab and it's facilities. These machines may have existing data storage mechanisms that may not yet mesh with one another, or be stored in the same place.

#### The big picture
We've looked at several data types that will exist in any chemical synthesis scenario, and how they might be stored "by default". In a worst case scenario, these different data sources may:
- Not exist in a digital format
- Contain errors (e.g. typos) due to being written into spreadsheets or databases by hand without data validation.
- Be stored somewhere that will no longer be available in the future (for example when staff leave the group).
- Exist in a proprietary format that it is difficult to extract data from for use in other analyses
- Be disconnected from one another (and other possible sources of data linkage) and may not have contain identifiers which allow it to be connected easily.

In the next section, we'll look at what a best case scenario might look like, and then: how we can get there.

## The end goal
Ideally, the process of setting up and running the chemical synthesis robot should result in a well-linked, searchable, database with minimal manual effort. The database should include information from all six sources of data mentioned above. As well as all of the data created inside the lab, the database could also link to knowledge created outside of it, for example the literature, or national databases of interest. 

The process of creating this database should be as easy as possible, automating things that can be automated, in order to both reduce the burden on individuals as much as possible (and thereby increasing compliance), and to reduce opportunities for errors. For example, we might imagine:
- Persistent digital identifiers for chemicals, people, and equipment, helping us to link to other equipment in the lab
- Technicians set up new users in the system, ensuring that they have a unique identifiers (e.g. ORCid), and that the data they create is stored securely and safely, and is readable for them, and for the larger database.
- Users scan labels on input chemicals, to automatically add information about their provenance, including information like batch, which might unveil reproducibility issues
- Users are prompted to link experiments to digital lab books
- Input formats are automatically checked for errors and missing inputs in real time
- Data is automatically backed up

Once created, the data created might be kept "in-house", or it might be available to researchers freely, or selectively, through a data access committee. Depending on the audience, users may wish to query the database locally, to search it using a web front end, or through an API.

[FIXME NATIONAL DATABASE]

## Road map
In order to prepare for a Digital Chemistry future, we need to not only invest in technology, but also in the development of processes and training materials. Luckily, we do not need to reach our ideal "end goal" to leverage any benefit. We've broken up the process into three stages. For each stage, we have created a checklist. These are available [on GitHub](). We welcome suggestions for making these more effective, to reduce the burden on those setting up an effective Digital Chemistry lab.

### Stage 1: Capture
The purpose of this stage is to **prevent data being collected presently from being lost** in the future. We may not be able to easily sort or use it all at this stage, but the important thing is that it is not lost. 

In this stage, we think about collecting what we would need to connect data that we currently store to one another, and to outside data sets that may be of interest.

### Stage 2: Curation
Databases may contain proprietary files where the underlying data cannot be easily extracted at the present time.
Getting all of the information out.
Checking for any sources of error.
Getting everything talking to each other.

### Stage 3: Use
Data Access Comittee
Ethics?

### Stage 4: Infrastructure
A national database? Biocurators, chemicurators. Ontology? Versioning and archiving the database. 

## Conclusion
There are steps that you can take now to start capturing your data in a format that can be usable later.

--------

## Bibliography

IBM: https://www.chemistryworld.com/news/ibm-seeks-to-simplify-robotic-chemistry/4012359.article 
Kuka: https://www.nature.com/articles/s41586-020-2442-2?luicode=10000011&lfid=231522type%3D1%26t%3D10%26q%3D%23nature%23&featurecode=20000181&u=https%3A%2F%2Fwww.nature.com%2Farticles%2Fs41586-020-2442-2
Data cleaning takes forever: https://www.cognilytica.com/2019/03/06/report-data-engineering-preparation-and-labeling-for-ai-2019/
Bristol Chem Management: http://www.bristol.ac.uk/safety/media/po/Haz-Chem-management-v1.1-po.pdf 



<!--
- Data interoperability
	- Data format (and interoperability with popular computational tools).
	- Persistent identifiers
		- ORCID 
		- CAS
		- chemical ontologies [LINK FIXME]. 

Processes should increase efficiency, but they also need to be easy enough to do that people can actually be bothered to do them. 
Process documents
Training
Reduce difficulty for lab members and technicicans
Reduce error-prone by-hand typing 
Data Access Comittee
Ethics?

Considerations:
- What you will need the data for?
- Who will need to access the data?

Data should be 
(Findable, Accessible, Interoperable, and Reusable) for it's target audience.

Findable: 
   - People who want to use the data (i.e. people who you want 
Interoperable:
 	- Data should be easy to search, i.e. in a database, or in a .csv file
-->
