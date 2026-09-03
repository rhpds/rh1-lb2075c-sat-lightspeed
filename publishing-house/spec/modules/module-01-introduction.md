# Module Outline: module-01-introduction

## Brief Overview

This opening module orients participants to the lab and its goals before any hands-on work begins. It describes the three-node environment — one Satellite server and two RHEL 10 hosts — and explains what the lab will accomplish: installing and verifying Red Hat Lightspeed on the Satellite server. The module closes by walking participants through their first interactive step: logging into the Satellite web UI using provided credentials. This module is intentionally short and low-friction, designed to build confidence before the more technical modules that follow.

## Audience and Time

- **Target persona:** System administrators and Satellite administrators new to Red Hat Lightspeed
- **Prerequisites for this module:** None — this is the entry point for the lab
- **Estimated duration:** 10 minutes

## Learning Objectives

- Explore the three-node lab environment (satellite.lab, rhel1.lab, rhel2.lab) and identify the role of each node
- Verify access to the Satellite web UI by logging in with the provided credentials

## Lab Structure

| Section | Title | Duration |
|---------|-------|----------|
| 1 | Introduction and lab goal | 3 min |
| 2 | Lab environment overview | 3 min |
| 3 | Log into the Satellite web UI | 4 min |

## Detailed Steps

1. Read the lab introduction text describing the goal: install and configure Red Hat Lightspeed on the Satellite server.
2. Review the lab environment diagram or description identifying the three nodes: satellite.lab (Satellite server), rhel1.lab (RHEL 10 host), rhel2.lab (RHEL 10 host).
3. Open the Satellite web UI browser tab provided by the nookbag UI.
4. Enter the provided username and password into the Satellite login form.
5. Click **Log In** and confirm the Satellite dashboard loads successfully.

## Key Takeaways

- Red Hat Lightspeed is a vulnerability monitoring service that runs locally on the Satellite server without sending data externally
- The lab environment provides a pre-installed Satellite server with pre-synchronized content, so participants can focus on Lightspeed configuration
- The Satellite web UI is the primary interface for monitoring and verification throughout the lab

## Infrastructure Notes

- satellite.lab must be reachable from the learner's browser tab in the nookbag UI
- No CLI interaction required in this module
- Satellite must be pre-installed and content pre-synchronized before the lab starts
