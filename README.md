# Denial-of-Service Attack Detection using Machine Learning in Network-on-Chip Architectures

## Abstract

State-of-the-art System-on-Chip (SoC) designs consist of many Intellectual Property (IP) cores that interact using a Network-on-Chip (NoC) architecture. SoC designers increasingly rely on global supply chains for obtaining third-party IPs. In addition to inherent vulnerabilities associated with utilizing thirdparty IPs, NoC based SoCs enable attackers to exploit the distributed nature of NoC and its connectivity with various IPs to launch a plethora of attacks. Specifically, Denial-ofService (DoS) attacks pose a serious threat in degrading the SoC performance by flooding the NoC with unnecessary packets.

A machine learning-based runtime monitoring mechanism to detect DoS attacks is presented here. The approach is capable of detecting DoS attacks with high accuracy, even in the presence of unpredictable NoC traffic patterns caused by various applications and application mappings. Extensive exploration of machine learning models and features were done to provide a comprehensive study on how to use machine learning for DoS attack detection in NoC-based SoCs.

## The Era of IoT


<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/01-iot.png">
</p>

The number of connected smart computing devices exceeds the human population, expecting over 50 billion devices to be deployed and mutually connected by 2025. Development of solutions are ranging from smartwatches, smart cars, smart homes, all the way to smart cities. We live in a time which is reigned by mutually connected devices.

## System-on-Chip

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/02-soc.PNG" width=50%>
</p>

System-on-Chip (SoC) designs are at the heart of the computing devices, which range from simple IoT devices in smart homes to complex navigation systems in airplanes.

SoCs are in contrast to the common traditional motherboard-based PC architecture, whereas a motherboard houses and connects detachable or replaceable components, SoCs integrate all of these components into a single integrated circuit, as if all these functions were built into the motherboard.

The Broadcom BCM2835 SoC used in the first generation Raspberry Pi includes a 700 MHz ARM1176JZF-S processor, VideoCore IV graphics processing unit (GPU), and RAM.

### Syetem-on-Chip Definition

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/03-soc-def.png">
</p>

A system on a chip (SoC) combines the required electronic circuits of various computer components onto a single, integrated chip (IC).

Modern SoC designs contain several highly sensitive assets such as encryption keys, device configurations, and on-device protected data that are responsible for keeping our personal, financial, and intimate physiological information safe and secure.

### Popular System-on-Chips

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/04-socs.PNG">
</p>

Today, System-on-Chips (SoCs) can be found in almost every smartphone and tablet.

### Why a SoC is different from a CPU?

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/05-cpusoc.PNG">
</p>

CPU is a very fast calculator. It fetches data from memory, and then performs some kind of arithmetic (add, multiply) or logical (and, or, not) operation on that data. It requires a whole framework of other silicon chips to perform the tasks of a computer. A memory to hold the data, an audio chip to decode and amplify music, a graphics processor to draw pictures on the monitor.

System-on-a-chip integrates almost all of these components into a single silicon chip. A SoC usually contains a GPU (a graphics processor), a memory, a USB controller, and power management circuits other than its processors.

A CPU cannot function without dozens of other chips, it’s possible to build complete computers with just a single SoC.

### Why SoCs are preffered?

Needs less wiring than a CPU

Almost at the same size of a CPU.

Provides more functionality than a CPU.

In most instances, SoCs have a lesser power consumption.

Provides better design security at hardware and firmware levels.

### Intellectual Property Core Definition

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/06-ipcore.PNG">
</p>

An  Intellectual Property (IP) core in semiconductors is a reusable unit of logic or functionality or a cell or a layout design  that is normally developed  with the  idea of  licencing to multiple vendor for  using as building blocks in  different chip designs.

### Complexity and Challenges

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/06-complexity.PNG">
</p>

The drastic increase in SoC complexity has led to a significant increase in SoC design and validation complexity. This has challenged the verification of modern system-on-chip solutions and the increasing number of cores demands the use of a scalable on-chip interconnection architecture.

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/07-vendors.PNG">
</p>

Reusable hardware IP based SoC design from various vendors has emerged as a pervasive design practice in the industry to dramatically reduce design and verification cost while meeting aggressive time-to-market constraints. These third-party IPs may come with deliberate malicious implants to incorporate undesired functionality .

## Network-on-Chip

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/08-noc.PNG">
</p>

Network-on-Chip architecture is widely used to interconnect the Intellectual Property (IP) cores the System-on-Chip (SoC) designs. It uses a a packet based communication approach. 

NoC has allowed computer architects to fully utilize the computational power in an SoC by facilitating low-latency and high-throughput.

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/09-nocs.PNG">
</p>

It is considered as an aggressive long-term approach for on-chip communications because it can deal well with the design issues of communication performance, power consumption, signal integrity, and system scalability.

## Motivation

The global trend of distributed design, manufacturing and testing of intellectual property  cores of system-on-chip (SoC)  has raised serious concerns about SoC security vulnerabilities.

Previous strategies to detect these security vulnerabilities are based on highly predictable NoC traffic patterns, which allowed the construction of linear statistical bounds to detect attacks such as DoS.

Assumptions of previous detection strategies do not hold during many realistic scenarios that include task migration, task preemption, changing application characteristics due to major input variations, etc

To the best of my knowledge, this is the first attempt at securing network-on-chip based system-on-chip using machine learning.

## Deliverables

Simulate and profile the normal behavior of traffic when applications are running.

Simulate and profile anomalous behavior of traffic when security violations are carried out against the system.

Build a model that encapsulates the normal behavior with the goal of capturing any abnormalities during runtime.

Implementing detection strategies for identified security violations (ex: DOS) and appropriate countermeasures.

Deploying the trained model in the NoC and evaluate the performance during runtime.

Need to add images from the begining about the structure - from data vil to models

## Timeline

Setup NoC simulation environment		- 13th March		-	✔️

Collect NoC traffic traces by simulator		- 20th March		-	✔️

Development of Initial ML model			- 30th April		-	✔️

Test ML model on different attack models	- 07th May		-	✔️	

Re-evaluate and re-build model if required	- 14th May		- 	✔️

Complete first draft of the paper		- 27th May		-	✔️

Paper submission to the conference		- 05th June		-	✔️

## Anormaly Detection Pipeline

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/10-detection.png">
</p>

## Machine Learning Pipeline

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/11-ml.PNG">
</p>

## Illustrative Example of a Denial-of-Service Attack

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/12-dos.png">
</p>

## Threat Model (Using FFT)

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/13-threat.png">
</p>

## GEM5 Simulation and Data Extraction

<p align="center"> 
<img src = "https://github.com/chamikasudusinghe/nocml/blob/master/%5B05%20-%20Resources%5D/14-sim.png">
</p>

Each hop of a flit is depicted in 6 lines; connection to network interface, waking up of the router, flit passing through the router.

### Simulation Edits

packet type - GETS, GETX, PUTX, PUTS, DATA, ACK
directory address of the packet - ex: 0x1dc0

Newly extracted data were added to the SwitchAllocator line and the SwitchAllocator line was used to extract features to be used in the machine learning model.

## Initially Generated Features

time: timestamp when the flit passes through the router
router: the router which the flit is passing at the timestamp
inport: the input port used by the flit to enter the router (1-South, 2-East, ...)
outport: the output port used by the flit to enter the router (1-South, 2-East, ...)
packet type: the type of the packet of the respective flit entering the router (1-GETS, 2-GETX, ...)
flit id: the identifier used to determine each flit that forms a packet
flit type: this defines whether the filt is the header of a request, response or data 
vnet: virtual networks provide the same resource sharing capabilities that are inherent in other resources being a platform-independent.
vc: virtual channel used by the flit to enter the router
src ni: the network interface of the source router used by the flit
src router: the source router of the flit
dst ni: the network interface of the destination router used by the flit
dst router: the destination router of the flit

## Fabricated Features (Routervise)


[Initial] - Initial set of word done on the dataset from extraction, feature engineering to machine learning pipelines. Models run here to detect  dos attacks have limited features. ##errorneous features are also included.

include future work as well

[Modeling] - Modeling different set of data to understand about the features to be used and extracted from the log file itearatively.

[Modeling][dos ver 1] - Visualization of the original features extracted from the log file and the correlation about the features.

[Modeling][dos ver 2] - Visualization of the additional features and original features extracted from the log file and the correlation about the features.

[Modeling][dos ver 4] - Modeling the system by slinding windows of 100, 1000 and 10000 for the entire dataset.

[Modeling][dos ver 5.1] - Modeling the per each router for the conventional NoC architecture.

[Modeling][dos ver 5.1] - Modeling the per each router for the KNL architecture with additional crafted features.

[Modeling][syth ver 1.1] - Modeling against synthetic traffic generation to see its performance againts the model.

[Results] - Iterative process of generating results to be included in the paper.

[Results][dos results ver 1][dos results ver 1.1] -  Simulation results and visualization for execution of FFT for 2 IPs (normal).

[Results][dos results ver 2] -  Simulation results and visualization for execution of FFT for 8 IPs (normal).

[Results][dos results ver 3] -  Results generation for 100 window for all 16  routers.

[Results][dos results ver 4] -   Results generation for 1000 window for all 16  routers. (included in the paper)

[Paper] - Statstical and descriptive content to be included in the paper.

log files are not included here due to large file size.
