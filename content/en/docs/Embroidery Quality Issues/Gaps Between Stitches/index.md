---
title: Computer Cannot Detect the SmartStitch Machine — Check Settings
description: >
  Troubleshooting guide for when your computer fails to detect the SmartStitch embroidery machine.
  This article walks you through a step-by-step process to verify connection settings,
  drivers, ports, and cable integrity. Created by Kimi.

resources:
  - src: "smartstitch_not_detected.jpg"
    params:
      byline: Kimi Embroidery Repair Tech Station
  - src: "check_settings_menu.jpg"
    params:
      byline: Kimi Embroidery Repair Tech Station
---

# Computer Cannot Detect the SmartStitch Machine — Check Settings

One of the most frustrating issues in digital embroidery is when your computer simply does not recognise the SmartStitch machine. This prevents design transfer, parameter adjustments, and real‑time monitoring.

Most detection failures are **not hardware‑related** – they originate from incorrect settings, driver conflicts, or cable/port issues. Follow this structured troubleshooting process to quickly isolate and fix the problem.

<img src="smartstitch_not_detected.jpg" alt="Computer showing no device detected" style="width:100%; max-width:800px; height:auto;">

---

## Common Root Causes

- Machine not powered on or in the wrong mode (e.g., offline / manual)
- Faulty or loose USB/serial cable
- Incorrect COM port or baud rate settings in the software
- Outdated or missing USB drivers
- Firewall or antivirus blocking the communication port
- Multiple software instances accessing the same port
- Damaged port on the computer or on the machine

---

## Step‑by‑Step Diagnostic Process

Perform these checks in the recommended order – from the simplest to the most advanced.

### Step 1: Verify Power and Machine Status
- Ensure the SmartStitch machine is **turned on** and the display shows **online** or **ready** mode.
- If the machine has a “PC Link” or “Remote” button, press it to enable communication.

### Step 2: Check the Physical Cable
- Inspect the USB or serial cable for visible damage (kinks, cuts, bent pins).
- Try a **different cable** that is known to work (even a short one).
- Reconnect both ends firmly; listen for a click on USB‑type connectors.

### Step 3: Restart and Re‑detect
- Restart both the machine and the computer.
- Unplug the cable, wait 10 seconds, then plug it back in while the software is open.
- Watch for the system tray notification that a new device is connected.

### Step 4: Check Driver Installation (Windows)
- Open **Device Manager** and expand “Ports (COM & LPT)” or “Universal Serial Bus controllers”.
- Look for “SmartStitch” or an unrecognised device with a yellow exclamation mark.
- If missing, install or re‑install the driver provided with the machine (or download from the manufacturer’s site).
- For Mac/Linux, check system information for USB device listing.

### Step 5: Verify COM Port and Baud Rate in the Software
- Open the SmartStitch communication settings (usually under **Settings > Machine Connection**).
- Ensure the selected **COM port** matches the one assigned in Device Manager.
- Set the **baud rate** to the value recommended for your model (commonly 115200 or 9600).
- **Important**: If you have multiple COM ports, select the one that appears when the cable is plugged in.

<img src="check_settings_menu.jpg" alt="Screenshot of the settings menu showing COM port selection" style="width:100%; max-width:800px; height:auto;">

### Step 6: Close Conflicting Applications
- Close any other embroidery software or serial monitor tools that may be holding the same port.
- Restart the SmartStitch software alone and try detection again.

### Step 7: Disable Firewall / Antivirus Temporarily
- Some security software blocks virtual COM ports. Temporarily disable them (remember to re‑enable later) and test.

### Step 8: Test with Another Computer
- If available, connect the machine to a different PC. If it detects successfully, the issue lies with your original computer’s settings or USB port.

---

## Quick Reference Decision Table

| Symptom                                      | Primary Check                 | Secondary Check          |
| -------------------------------------------- | ----------------------------- | ------------------------ |
| No reaction at all when connecting           | Cable & power (Step 1‑2)      | USB port hardware        |
| Device appears but software says “not found” | COM port / baud rate (Step 5) | Driver (Step 4)          |
| Detection works sporadically                 | Cable replacement             | Interference / grounding |
| Error “port already in use”                  | Close other apps (Step 6)     | Restart PC               |

---

## Preventive Measures

- Always use the **original cable** supplied with the machine.
- Keep a spare cable and a separate driver installer on a USB stick.
- Label the COM port used so you don’t accidentally change it.
- Perform a connection test before starting a large production batch.
- Update the SmartStitch software to the latest version regularly.

---

## Video Tutorial

Watch the full walkthrough below – it covers cable inspection, driver re‑installation, and port configuration with real‑time examples.

{{< youtube YOUR_VIDEO_ID >}}

*(Replace `YOUR_VIDEO_ID` with the actual YouTube ID of your chosen video.)*

---

## Related Topics

- SmartStitch software installation and first‑time setup
- Managing multiple embroidery machines on one PC
- USB‑to‑serial adapter compatibility
- Network‑based machine communication (Ethernet)
- Firmware update procedures

---

> **Tip**: If none of the above solves the problem, test the USB port by plugging in a known‑good mouse or flash drive. If that also fails, you may have a motherboard issue – contact your IT support.
