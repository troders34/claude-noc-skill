# Format
In generating the questions, provide the following mandatory components:

- number of questions (for example: 1,2,3,40,51)
- type of questions
- sentence of question
- subject
- question's design
- vendor (if applicable)
- answer options: if multiple-choice (A, B, C, D), if true-or-false (True or False)
- key answer: applicable to any type of questions
- brief explanation of key answer, for labs questions provide solving methodology and things to consider to support the answer.

## For example (multiple-choice single-answer):
- Type = multiple-choice single-answer
- Subject = network monitoring
- Design = technical, scenario-based

1. In a Network Operations Center (NOC), you are configuring a monitoring server to track the health of several enterprise routers. What is the primary function of an "SNMP Trap" in this monitoring architecture? Options:

A. To continuously poll the routers at regular intervals to collect baseline CPU and memory utilization metrics

B. To securely encrypt the management traffic sent between the monitoring server and the edge routers

C. To send an unsolicited, asynchronous alert from a router to the monitoring server the moment a critical event occurs, such as an interface going down

D. To synchronize the internal clocks of all managed network devices to ensure accurate system log timestamps

The key answer and explanation must be placed at the end of the last number of question, but the format should be like this:

Key answer = C

Explanation = Simple Network Management Protocol (SNMP) operates using two primary communication methods: Polling and Traps. An SNMP Trap is a push-based mechanism. Instead of the central monitoring server constantly asking the router for updates (which is known as SNMP Polling or a GET request, as described in Option A), a Trap allows the router to instantly notify the server on its own when a specific threshold is breached (like ether1 losing its link status). Option B describes SNMPv3 authentication/encryption, and Option D describes NTP (Network Time Protocol).

## For example (multiple-choice multiple-answer):
- Type = multiple-choice multiple-answer
- Subject = network monitoring
- Design = theoretical

1. Which of the following network metrics are typically gathered using flow-based monitoring (such as NetFlow or sFlow) rather than standard SNMP polling?

A. The current CPU and memory utilization of the core router

B. The specific application port numbers consuming the most bandwidth

C. The internal chassis temperature and fan speeds of a switch

D. The top source IP addresses generating traffic on the network

Key answers = B,D

Explanation = Flow-based monitoring protocols analyze the metadata of packets passing through a device to determine traffic patterns (who is talking to whom, and on what ports). SNMP polling is primarily used for pulling hardware-level device health metrics like CPU usage, memory, and temperature.

## For example (essay):
- Type = multiple-choice multiple-answer
- Subject = network monitoring
- Design = technical, troubleshooting

1. Your central monitoring server has suddenly stopped receiving SNMP metrics from a core MikroTik router. However, the router is still actively passing network traffic and responding to ICMP ping requests from the monitoring server. Describe the step-by-step troubleshooting process to identify and resolve this SNMP communication failure.

Key answer =
- Verify the SNMP service is actively running and enabled on the router,
- Confirm the SNMP community string (or SNMPv3 credentials) configured on the monitoring server exactly matches the configuration on the router,
- Check the router's Access Control Lists (ACLs) or firewall filter rules to ensure UDP port 161 is explicitly allowed from the monitoring server's IP address,
- Verify the router's return routing path to ensure the SNMP response packets are not being misrouted out of a different interface.

Explanation = The successful ICMP replies prove that Layer 3 (IP routing) and physical connectivity are functioning normally. Therefore, the troubleshooting must immediately isolate Layer 4 (firewall blocking UDP 161) and Layer 7 (SNMP application configuration, service status, and authentication credentials).

## For example (true OR false):
- Type = true-or-false
- Subject = network monitoring
- Design = theoretical

1. Port mirroring (SPAN) is classified as an active monitoring technique because it actively injects synthetic test packets into the network to measure latency and packet loss. (True/False)

Key answer = False

Explanation = Port mirroring is a passive monitoring technique. It safely duplicates existing, real-time production traffic to a monitoring port (such as an Intrusion Detection System or packet analyzer) without modifying the traffic or injecting new packets. Active monitoring relies on generating synthetic traffic, using tools like ping, traceroute, or specialized SLA probes.

## For example (labs):
- Type = labs
- Subject = network monitoring
- Design = technical, scenario-based

1. You have deployed a new MikroTik Cloud Hosted Router (CHR) node in a PNETLab topology. You need to configure this router to forward its system event logs to a remote monitoring Syslog server located at 192.168.10.100. Provide the exact configuration steps required to achieve this.

Key answer =
1. Define the remote server target:
`
/system logging action add name=RemoteSyslog target=remote remote=192.168.10.100
`

2. Route specific log topics to that target:
`
/system logging add action=RemoteSyslog topics=info,error,warning
`

Explanation = By default, RouterOS logs are only stored in local memory and are lost upon a reboot. This configuration creates a dedicated pathway to push critical, warning, and informational system events over the network to a centralized, persistent log server using UDP port 514.

Methodology = {name of methodology, for example = root cause analysis}
1. Step 1 (Target Definition): You must first establish "where" and "how" the logs are being sent. Creating a new logging action sets the destination IP and prepares the router to format the messages for a remote server rather than local disk or memory.
2. Step 2 (Topic Binding): You must define "what" is being sent. Creating a logging rule binds specific severity levels (topics) to the action you just created.

Things to consider to support answering:
1. Reachability: Before applying the configuration, use the ping tool to ensure the router has a valid route to 192.168.10.100.
2. Firewall Rules: Ensure there are no strict output chain firewall rules dropping outbound UDP traffic on port 514.
3. Noise Filtering: Consider omitting the debug topic in the second command unless actively troubleshooting, as sending debug logs to a remote server can easily overwhelm the network and the Syslog storage.
