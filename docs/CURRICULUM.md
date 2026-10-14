# TutorX Curriculum and Content Map

## Course design

The curriculum moves from vendor-neutral foundations to the practical work of a Tier 1 engineer. Each section should eventually contain short lessons, key definitions, diagrams, worked examples, flashcards, quizzes, a scenario, and interview prompts.

## Section map

| # | Section | Core learning outcomes |
|---:|---|---|
| 1 | Networking Fundamentals | Define networks and common terms; distinguish LAN/WAN; identify switches, routers, APs, CPE and ONTs; explain topology, media and performance metrics. |
| 2 | OSI Model and TCP/IP | Explain all seven OSI layers and the TCP/IP model; identify PDUs; describe encapsulation; classify common faults by layer. |
| 3 | IPv4 Addressing and Subnetting | Read IPv4 addresses; identify private and special ranges; calculate masks, prefixes, network/broadcast addresses and usable host counts. |
| 4 | Routing and Switching | Explain MAC learning, Ethernet frames, ARP, VLANs, trunks, default gateways, routing tables and longest-prefix match. |
| 5 | TCP/IP, Ports and Services | Compare TCP/UDP; understand ports; explain DNS, DHCP, ICMP, SSH, SNMP, NTP, HTTP/S and common service ports. |
| 6 | Telecommunications and B2B Networks | Explain CPE/CE, access and core networks, fibre access, OLT/ONT, optical alarms, Ethernet handoffs, SLAs and restoration checks. |
| 7 | Network Troubleshooting | Use a repeatable fault-isolation process; interpret ping/traceroute and local configuration; use interface counters and document evidence. |
| 8 | Incident, Problem and Change Management | Distinguish incidents, problems, requests and changes; apply impact/urgency; maintain tickets, SLA awareness, escalation and post-incident reviews. |
| 9 | Cisco and Juniper Essentials | Understand safe CLI habits, interface status, counters, routes, neighbours, IOS-style commands and Junos operational/configuration concepts. |
| 10 | NOC Operations and Customer Support | Triage alarms, correlate shared events, manage queues, communicate clearly, hand over shifts and validate maintenance. |
| 11 | Interview Practice and Final Assessment | Deliver structured technical answers, use STAR for behavioural examples, solve outage scenarios and assess readiness honestly. |

## Required lesson format

Every lesson should include:

1. A concise title and measurable objective.
2. A beginner-friendly explanation.
3. Definitions of essential vocabulary.
4. A practical B2B/NOC example.
5. A memory aid or misconception warning.
6. At least one knowledge-check prompt.
7. A teach-back prompt asking the learner to explain the concept in their own words.
8. Links or references for further study when the lesson covers a standard or vendor-specific behavior.

## Assessment coverage

- Flashcards: short definition, contrast, process, or troubleshooting prompt on the front; concise answer and caveat on the back.
- Quiz: multiple-choice or short-answer question, one defensible correct answer, explanatory feedback, and source/lesson mapping.
- Scenario: customer symptom, known evidence, best next action, explanation, and why common alternatives are weaker.
- Interview question: prompt, evaluation criteria, model answer framework, and a reminder not to invent experience.

## Content status in the first release

The first release includes authored lessons and flashcards across all 11 sections, section quizzes, six outage-detective scenarios, an interview bank, and a searchable glossary. The course is a strong interactive starter and should be expanded iteratively before being treated as a complete certification-level course.

## Technical content quality checklist

- Distinguish Ethernet frames, IP packets, TCP segments, and UDP datagrams.
- Avoid implying that ping failure proves a device is down.
- Avoid implying that an interface-up state proves end-to-end service availability.
- Include the RFC 1918 private IPv4 ranges correctly: 10/8, 172.16/12, and 192.168/16.
- Treat /31 and /32 IPv4 cases separately from the conventional usable-host formula.
- State that TCP/443 is common for HTTPS while HTTP/3 uses QUIC over UDP/443.
- Explain that command syntax varies by platform and OS version.
- Avoid invented provider-specific SLAs, fault codes, escalation contacts, or guaranteed restoration times.
- Remind learners to use production commands and tests only when authorized.

## Recommended primary references

- Cisco Networking Academy: https://www.netacad.com/
- IETF RFC 791, Internet Protocol: https://www.rfc-editor.org/rfc/rfc791
- IETF RFC 1918, Address Allocation for Private Internets: https://www.rfc-editor.org/rfc/rfc1918
- IETF RFC 4632, Classless Inter-domain Routing: https://www.rfc-editor.org/rfc/rfc4632
- IETF RFC 826, Address Resolution Protocol: https://www.rfc-editor.org/rfc/rfc826
- IETF RFC 9293, Transmission Control Protocol: https://www.rfc-editor.org/rfc/rfc9293
- IETF RFC 768, User Datagram Protocol: https://www.rfc-editor.org/rfc/rfc768
- IETF RFC 1034 and RFC 1035, DNS: https://www.rfc-editor.org/rfc/rfc1034 and https://www.rfc-editor.org/rfc/rfc1035
- IETF RFC 2131, DHCP: https://www.rfc-editor.org/rfc/rfc2131
- IETF RFC 3411, SNMP architecture: https://www.rfc-editor.org/rfc/rfc3411
- Juniper technical documentation: https://www.juniper.net/documentation/
- Cisco technical documentation: https://www.cisco.com/c/en/us/support/index.html
- ITIL overview and practices: https://www.peoplecert.org/

Check the current edition and applicability of any standard or vendor guide when building advanced lessons.