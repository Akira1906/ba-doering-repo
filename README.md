# PSAMP Packet Selection Architecture 

This repository contains Python prototypes for the components of a PSAMP (Packet Sampling) based Packet Selection Architecture. The purpose of this architecture is to provide an innovative application fot the PSAMP architecture for packet filtering to support various kinds of network functions.

## Components 

This repository contains two Python prototypes:

1. **psamp_device.py**: This prototype acts as an Observation Point that listens to a network interface, Metering Process and Exporting Process. It is responsible for exporting PSAMP protocol messages and connects to the PSAMP_Collector.py.

2. **psamp_collector.py**: This prototype incorporates a Collecting Process and a network function. It is responsible for collecting PSAMP protocol messages and is connected to the PSAMP_Device.py.

Both prototype components are configured to be executed on the same host. For further insights on the implementation prototype read the implementation chapter the accompanying thesis.

## Installation

The PSAMP prototype has been tested under Debian Bullseye, but should work under most Linux distributions. Follow these steps to install the prototype on a local machine:

1. Clone this repository to your local machine.
2. Install the required Python modules (scapy, matplotlib).
2. Configure the prototype via the config.json files in `prototype/code/configs`, the prototype can be configured according to the Configuration Model in RFC6728.
3. Execute both PSAMP_Collector.py and PSAMP_Device.py located in `prototype/code`.

## Testbed Environment

In order to provide reproducible tests, POS-Scripts ([Plain Orchestrating Service](https://gitlab.lrz.de/I8-testbeds/pos)) were used for the execution of all tests. There are two different variants of the script provided in this repository at `prototype/code/experiments/experiment_setup`:

1. Vermont + Python prototype
2. Python prototype components only

The script consists of two parts that are executed on two test nodes directly connected via Ethernet. Follow these steps to execute the script:

1. Configure the global parameters for the POS script.
2. Execute the script with two connected test nodes.
3. The test results are now available at the first test node where the Python prototype was executed.


## Contact

If you have any questions or issues with the PSAMP Packet Selection Architecture, please contact [Tristan Döring](mailto:tristan.doering@tum.de). Every feedback or contribution to this project is welcome.