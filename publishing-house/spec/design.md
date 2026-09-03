# Installing Red Hat Lightspeed on Red Hat Satellite

## Overview

This lab guides participants through installing and configuring Red Hat Lightspeed on an existing Red Hat Satellite server. Red Hat Lightspeed is a containerized, on-premises vulnerability monitoring service that processes CVE data locally without transmitting data externally. Participants will install Lightspeed using the satellite-installer command, download and stage the CVE metadata database, register RHEL 10 hosts with Red Hat Insights, and confirm that vulnerability data appears in the Satellite web UI.

## Target Audience

- **Role:** System administrators, Satellite administrators, and infrastructure engineers
- **Experience level:** Beginner
- **What they already know:** Basic familiarity with Linux command-line and web UIs; no prior Red Hat Satellite or Red Hat Lightspeed experience required
- **What they don't know:** How to install and enable Red Hat Lightspeed on a Satellite server; how Lightspeed processes CVE data locally using cvemap.xml; how to register RHEL hosts with Red Hat Insights and verify vulnerability detection

## Prerequisites

- None — Red Hat Satellite is pre-installed and content is pre-synchronized in the lab environment

## Learning Objectives

1. Install Red Hat Lightspeed on a Satellite server using the satellite-installer command
2. Configure the CVE metadata database by downloading and staging cvemap.xml in the Foreman data directory
3. Register RHEL 10 hosts with Red Hat Insights using the insights-client
4. Verify that Red Hat Lightspeed detects and displays host vulnerabilities in the Satellite web UI

## Content Type

Lab (hands-on)

## Products & Technologies

- Red Hat Satellite
- Red Hat Lightspeed (on-premises / Satellite-integrated)
- Red Hat Enterprise Linux 10 (RHEL 10)
- Podman
- Red Hat Insights / insights-client
- Foreman

## Module Map

| Module | Title | Duration |
|--------|-------|----------|
| 1 | Introduction | 10 min |
| 2 | Install Red Hat Lightspeed | 25 min |
| 3 | Configure CVE Data and Verify Lightspeed | 20 min |
| — | **Total hands-on** | **55 min** |
| — | **Total lab** | **~1 hour** |

## Difficulty Level

Beginner

## Environment

**Learner view:** The lab starts with a pre-installed Red Hat Satellite server (satellite.lab) and two RHEL 10 hosts (rhel1.lab, rhel2.lab). Satellite content is pre-synchronized. Participants access the Satellite web UI via a browser tab and the Satellite server terminal via a wetty terminal tab provided by the Zero-Touch nookbag UI. Red Hat Lightspeed is not yet installed at lab start.

**Automation needed:** Yes — the Satellite server and two RHEL 10 hosts must be provisioned, and Satellite must be pre-configured with synchronized content before the lab begins.

## Infrastructure Requirements

- **Cloud provider:** CNV (default)
- **Cluster type:** N/A — RHEL VMs only, no OpenShift
- **OCP version:** N/A
- **Topology:** Per-student — each student receives their own dedicated 3-VM set (satellite.lab, rhel1.lab, rhel2.lab)
- **Sizing per student:**
  - 1 × satellite.lab — 8 vCPU, 32 GB RAM, 540 GB disk (satellite-server image)
  - 1 × rhel1.lab — 1 vCPU, 4 GB RAM, 40 GB disk (RHEL 10)
  - 1 × rhel2.lab — 1 vCPU, 4 GB RAM, 40 GB disk (RHEL 10)
- **Egress:** TCP 443 only (required for security.access.redhat.com)
- **Automation approach:** Ansible
- **AI/MaaS:** None
- **External services:** security.access.redhat.com (CVE metadata download during lab)
- **AAP version:** N/A
- **Non-GA products:** None (all products are GA)

## Assessment Strategy (Optional)

This is a Zero-Touch lab using the nookbag UI with wetty terminals. Verification is learner-driven: participants observe the Lightspeed Vulnerability tab in the Satellite web UI and confirm that CVE data and host vulnerabilities are displayed after completing each stage. No automated solve/validate scripts are present in the current content.
