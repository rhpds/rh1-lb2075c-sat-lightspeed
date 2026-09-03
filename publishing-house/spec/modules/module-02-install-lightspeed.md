# Module Outline: module-02-install-lightspeed

## Brief Overview

This module introduces Red Hat Lightspeed — a containerized, Podman-based vulnerability monitoring service that runs entirely on-premises on the Satellite server — and guides participants through the installation process. The core task is running a single satellite-installer command to enable the Lightspeed (IOP) component, then confirming the installation succeeded by checking for the new Lightspeed menu in the Satellite web UI. The module reinforces the architecture point that Lightspeed processes CVE data locally without any data leaving the Satellite server.

## Audience and Time

- **Target persona:** System administrators and Satellite administrators enabling Lightspeed for the first time
- **Prerequisites for this module:** Completion of module-01; Satellite web UI session must be active
- **Estimated duration:** 25 minutes

## Learning Objectives

- Install Red Hat Lightspeed on a Satellite server by running the satellite-installer --enable-iop command in the Satellite terminal
- Verify the Lightspeed installation by confirming the Lightspeed menu appears in the Satellite web UI

## Lab Structure

| Section | Title | Duration |
|---------|-------|----------|
| 1 | Introduction to Red Hat Lightspeed | 7 min |
| 2 | Run satellite-installer to enable Lightspeed | 13 min |
| 3 | Verify the Lightspeed menu in the Satellite web UI | 5 min |

## Detailed Steps

1. Read the conceptual introduction explaining that Red Hat Lightspeed is a containerized service (managed by Podman) that runs locally on the Satellite server and processes vulnerability data without sending it externally.
2. Open the Satellite server terminal tab (wetty) provided by the nookbag UI.
3. Run the following command as root on satellite.lab:
   ```
   satellite-installer --enable-iop
   ```
4. Wait for the installer to complete. This may take several minutes; monitor the terminal output for progress and any errors.
5. When the installer reports success, switch to the Satellite web UI browser tab.
6. Navigate the Satellite web UI menu and locate the new **Lightspeed** entry confirming that the component is installed and active.

## Key Takeaways

- Red Hat Lightspeed is enabled via the satellite-installer framework using the --enable-iop flag, which handles all container and service configuration automatically
- Lightspeed runs as a containerized service managed by Podman; no additional container setup is required
- The Lightspeed menu in the Satellite web UI is the primary indicator of a successful installation
- No vulnerability data is transmitted outside the Satellite server — Lightspeed operates entirely on-premises

## Infrastructure Notes

- satellite.lab must have internet connectivity sufficient for the satellite-installer to pull any required container images (or images must be pre-cached)
- The installer run time may vary; plan for the full 13-minute section window
- Participants need both the Satellite web UI tab and the Satellite terminal (wetty) tab open simultaneously during this module
