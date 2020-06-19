# Denial-of-Service Attack Detection using MachineLearning in Network-on-Chip Architectures

State-of-the-art System-on-Chip (SoC) designs consist of many Intellectual Property (IP) cores that interact using a Network-on-Chip (NoC) architecture. SoC designers increasingly rely on global supply chains for obtaining third-party IPs. In addition to inherent vulnerabilities associated with utilizing thirdparty IPs, NoC based SoCs enable attackers to exploit the distributed nature of NoC and its connectivity with various IPs to launch a plethora of attacks. Specifically, Denial-ofService (DoS) attacks pose a serious threat in degrading the SoC performance by flooding the NoC with unnecessary packets.

A machine learning-based runtime monitoring mechanism to detect DoS attacks is presented here. The approach is capable of detecting DoS attacks with high accuracy, even in the presence of unpredictable NoC traffic patterns caused by various applications and application mappings. We extensively explore machine learning models and features to provide a comprehensive study on how to use machine learning for DoS attack detection in NoC-based SoCs

[Initial] - Initial set of word done on the dataset from extraction, feature engineering to machine learning pipelines. Models run here to detect  dos attacks have limited features. ##errorneous features are also included.

[Modeling] - Modeling different set of data to understand about the features to be used and extracted from the log file itearatively.

[Modeling][dos ver 1] - Visualization of the original features extracted from the log file and the correlation about the features.

[Modeling][dos ver 2] - Visualization of the additional features and original features extracted from the log file and the correlation about the features.

[Modeling][dos ver 4] - Modeling the system by slinding windows of 100, 1000 and 10000 for the entire dataset.

[Modeling][dos ver 4] - Modeling the system by slinding windows of 100, 1000 and 10000 for the entire dataset.

[Results] - Initial set of models run in the system againts dos attack with limited features. ##errorneous features are included here.

[Paper] - Initial set of models run in the system againts dos attack with limited features. ##errorneous features are included here.

[dos ver 5.2] - Current set of models run in the system againts dos attack with all possible features atm. Results included.

[synth ver 1.1] - Current set of models run in the system againts eavesdropping attack with all possible features atm. Results included.

[design project] - Source files of models and data extraction for demonstrations.

[dos results ver 1] -  Simulation results and visualization for execution of FFT for 2 IPs (normal).

[dos results ver 2] -  Simulation results and visualization for execution of FFT for 8 IPs (normal).

[dos results ver 3] -  Results generation for 100 window

[dos results ver 4] -  Generated results foe the paper (for 1000 window)

log files are not included here due to large file size.
