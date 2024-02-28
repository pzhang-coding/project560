# Multiple event identification and characterization by retrospective analysis of structured data streams

## AKA Post-processing some sensor data to see what happened

### Section 1 - Intro

Assumptions:

System suitable for analysis have the following characteristics:
1. The system generates one or more "events" that occur during operation
2. The "event" occurs sporadically, and has some tail
3. The "event" is associated with a "small and limited" number of sensing signals. That is, a limited number of sensor are able to capture the event

Goals:
1. Characterize the event signatures in the signals AKA, develop a feature set for the signals 

Editors note: This is an area I feel comfortable embarking on a literature review, am deeply interested in the below as well

2. Identify events within the signals and estimate the strength or weight (or whatever metric makes sense) of the event

Mechanism for achieving stated Goals: 
Multiple Event Identification and Characterization (MEIC) Algorithm, which is an optimization algorithm. 

Case Study:
Methods applied to some industrial process that has to do with rolled steel.

Paper format:
Section 1: Everything above
Section 2: Literature review (potential goldmine?)
Section 3: System Model, MEIC formulation, closed form solutions (MATH HEAVY)
Section 4: Simulation Study
Section 5: Case study
Sectoin 6: Conclusions

### Section 2 - Literature Review

The author states that wavelet analysis has been used in this domain as early as the 90s. However, the case for this paper is of sparse events, and wavelets are not great for that.

The author presents the notion of Phase-I monitoring for multiple signal data, but I have no familiarity with this concept.

This paper presents a solution that solves both the monitoring problem for multiple sensed signals as well as the signature characterization problem. I.e, we can identify events in the signals, and then we can identify the specific type of event. Traditionally, these are treated as separate problems. 

The MEIC algorithm identifies events, then it estimates the signature of the events. TBD how that happens (Sect 3).

The MEIC algorithm here uses the Dictionary Learning Technique developed in Lee (2007) (NOTE: READ THIS ONE). This method "identifies events and describes their effect by directly formulating an optimization criterion." See Yan: 2017,2018 and Mou: 2021.

### Section 3 - The MEIC Method
