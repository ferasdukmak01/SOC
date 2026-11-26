# SOC
A SOC built on a laptop with 8GB of RAM using Windows Server, Kali Linux, and Splunk.
# mySOC: A Small SOC Built on a Laptop with 8GB of RAM

## Problem
Everyone says you need a powerful computer to practice cybersecurity. Mine has 8GB of RAM. Could I still build a working SOC (security operations center) at home?

## What I Did
I built a SOC using three virtual computers on one laptop in VMware Workstation:
- **Windows Server 2022 with Active Directory:** the machine being protected
- **Kali Linux:** the "attacker" machine used to test from the other side
- **Splunk:** collects Windows Security records so I can search and investigate them

## Why These Tools
- **Windows Server and Active Directory:** most companies run on Windows and manage their users this way, so this is what analysts actually protect.
- **Kali Linux:** the standard attacker machine for security testing.
- **Splunk:** widely used in SOC teams. It collects activity records and lets me search them like a search engine.

## What This Project Covers
- Collecting Windows Security records into a SIEM (a tool that gathers and searches security activity)
- Searching and filtering records to find specific activity
- Planning memory across three virtual machines on 8GB of RAM

## What I Learned
- Limits force planning. With only 8GB to share, I had to decide how much memory each machine really needed.
- Records only help if you can search them. Following an event from the server into Splunk is what made Windows logs make sense.
- Analysts look at specific details, like which machine and which source an event came from.

## What I'd Improve
- Add Sysmon for much more detail on what the server is doing
- Set up alerts so Splunk flags suspicious activity automatically
- Build a dashboard to see activity at a glance
- Add more machines as I get around the memory limit
- Test attacks from Kali and write up how I spot them from the defender's side

## Tools
VMware Workstation · Windows Server 2022 · Active Directory · Kali Linux · Splunk · Markdown
