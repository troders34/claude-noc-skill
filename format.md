# Format
In generating the questions, provide the following mandatory components:

- number of questions
- type of questions
- sentence of question
- subject
- question's design
- vendor (if applicable)
- answer options: if multiple-choice (A, B, C, D), if true-or-false (True or False), if labs only (tell what to do and consider)
- key answer: applicable to any type of questions
- brief explanation of key answer

For example:

- Type = multiple-choice single-answer
- Subject = network monitoring
- Design = technical, scenario-based

1. In a Network Operations Center (NOC), you are configuring a monitoring server to track the health of several enterprise routers. What is the primary function of an "SNMP Trap" in this monitoring architecture? Options:

A. To continuously poll the routers at regular intervals to collect baseline CPU and memory utilization metrics

B. To securely encrypt the management traffic sent between the monitoring server and the edge routers

C. To send an unsolicited, asynchronous alert from a router to the monitoring server the moment a critical event occurs, such as an interface going down

D. To synchronize the internal clocks of all managed network devices to ensure accurate system log timestamps

Key answer = C

Explanation = Simple Network Management Protocol (SNMP) operates using two primary communication methods: Polling and Traps. An SNMP Trap is a push-based mechanism. Instead of the central monitoring server constantly asking the router for updates (which is known as SNMP Polling or a GET request, as described in Option A), a Trap allows the router to instantly notify the server on its own when a specific threshold is breached (like ether1 losing its link status). Option B describes SNMPv3 authentication/encryption, and Option D describes NTP (Network Time Protocol).
