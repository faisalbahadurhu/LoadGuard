# LoadGuard-JMeter

LoadGuard-JMeter is a JMeter plugin developed for adaptive workload generation. Instead of keeping the request rate fixed throughout a test, it monitors runtime performance and changes the request rate according to the defined Service Level Objectives (SLOs).

The plugin uses response-time and error-rate information to determine whether the system is operating in a **SAFE**, **HOLD**, or **VIOLATION** state. Based on this state, the request rate can be increased, maintained, or reduced during test execution.

The main components of LoadGuard-JMeter include:

- Elastic Timer
- Metrics Listener
- SLO Feedback Controller
- Decision Log Writer

## Repository Files

The repository contains the main implementation files required to use and study LoadGuard-JMeter.

- **Source ZIP file:** Contains the complete source code of the LoadGuard-JMeter implementation.
- **JAR file:** Contains the compiled LoadGuard-JMeter plugin that can be added to Apache JMeter.
- **CSV files:** Experimental result files can be provided separately for analysis and reproducibility.

## Using the Plugin

The supplied JAR file is the compiled LoadGuard-JMeter plugin. It can be added to the JMeter installation and then used within a JMeter test plan for SLO-aware workload generation.
The source ZIP is provided for users who want to inspect, modify, rebuild, or further extend the implementation.

## Requirements

- Java/JDK 17 or above
- JMeter_5.6.3


## Purpose

LoadGuard-JMeter was developed to study how runtime SLO feedback can be used to regulate workload generation during performance testing. The main purpose is not to generate the maximum possible load, but to adjust the workload according to the observed condition of the tested system.
