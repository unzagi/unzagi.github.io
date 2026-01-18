---
title: "Building an AI-Powered Home Phone ☎️ Switchboard"
date: 2025-06-10
status: publish
---
## Introduction

This project started with a simple but fun idea:

**Could I take an old red telephone ☎️ (a classic analogue phone), and make it part of a modern AI-powered smart home?**

Here’s the dream:

- Pick up the red phone → speak to an AI assistant (the assistant speaks back via Text-to-Speech on the phone line)
- Control smart home devices (lights, music, sensors, etc.)
- Ask questions and interact with the AI by phone
- Allow family and friends to call in from the outside world
- Allow myself to make calls out from my home phones to any normal phone

## How It Works

### Starting Point: Home Assistant VOIP

I began by following the [Home Assistant VOIP integration guide](https://www.home-assistant.io/integrations/voip/) and using a Grandstream Analogue-to-VoIP adapter.  
This allowed the red phone to directly call Home Assistant — triggering automations and interacting with the assistant without needing a full PBX.

![Red Phone Setup](/img/red_phone.jpg)


### Expanding with a PBX

To take the project further, I added a full PBX (Private Branch Exchange):

- Enables inbound and outbound calls using a real UK phone number
- Allows me to use softphones on mobile devices
- Provides voicemail, backups, notifications, and advanced call routing
- Sets the stage for future integrations — like replacing my video doorbell with a SIP-based intercom fully integrated into both the PBX and Home Assistant

### Why the PBX?

A full PBX isn’t strictly required for this project — the Home Assistant VOIP integration works great with just a Grandstream device.

However, running my own PBX gives me greater flexibility:

- Inbound/outbound calls on a real number
- Softphones
- Multi-extension management
- The ability to replace a video doorbell with a SIP intercom
- Local-only operation with no reliance on cloud services  
(The only ongoing cost is a minimal fee for the UK number and SIP trunk.)

### How It Runs

The PBX runs virtualised on **Proxmox** — an open-source hypervisor platform.  
It works much like the VMware ESXi systems I used to run years ago.  
I can spin up virtual machines and containers, keeping the PBX isolated but flexible — perfect for tinkering and future upgrades.

## What I Did Today

### 1️⃣ Set Up a PBX Server

- Installed PBX software to act as my home phone switchboard.
- The PBX manages calls between devices in the house and connects to the outside phone network.

### 2️⃣ Connected the Red Phone

- Used a small device (VOIP adapter) to connect the analogue red phone to the PBX.
- The red phone now acts like a modern phone, linked to the phone system.

### 3️⃣ Tested with Mobile Softphone

- Installed a phone app on my mobile phone that connects to the PBX.
- I can now use my mobile to make and receive calls over Wi-Fi, as if it were an extension of the home phone system.

### 4️⃣ Connected to the Outside World

- Set up a virtual phone number (a real UK phone number).  
Now:
  - Friends/family can call the home number, and the red phone rings.
  - I can use any home phone to call out to normal phone numbers.

### 5️⃣ Email Notifications

- Configured the system to send email notifications for things like:
  - System backups
  - Voicemails
  - Alerts

### 6️⃣ Backup System

- Set up an automatic backup system for the PBX.
- The PBX now saves copies of its configuration and data regularly to an external backup server.
- This ensures that if anything goes wrong, I can easily restore the system.

## Result

- I can call my **AI assistant** (via Home Assistant’s VOIP integration) from any home phone (physical or softphone).  
  When I pick up a phone and dial the AI extension, it speaks back using **Text-to-Speech**, and I can control smart devices by voice through the phone line.  
  For example:  
  _"Turn on the office lights," "Turn on the garden lights," or "Open the office blinds"_ — all from the red phone or any connected phone.
  
- I can receive calls from the public phone network at home.

- I can make calls out to any normal phone.

- The system is backed up and sending notifications.

## Why It’s Exciting

With **Home Assistant** acting as the brain of the home, I can take in data from a wide range of sources (apps, sensors, websites, live feeds) and run automations on them — and now, the phone system becomes another powerful output.

It opens up fun possibilities — everything from useful alerts to playful experiences.

## Next Steps

- Set up monitoring tools to check the PBX health and performance.
- Setup Cisco PoE VoIP phone for a second extension downstairs.
- Experiment with advanced call routing (e.g. different voices/phones at different times of day).
- Explore linking **Grafana alerts** to the phone system.
- Expand Home Assistant automations to trigger phone-based alerts.  
  - For example — I’d like to set it up so that when an **F1 race is about to start**, the phone rings and plays a voice alert!  
  - This will tie into my wider Home Assistant project, where data from various sources can trigger smart home routines

## References

If you want to dive deeper or try this yourself, here are some of the key resources I used along the way:

- [How to call Assist from a FreePBX VoIP phone (Reddit Guide)](https://www.reddit.com/r/homeassistant/comments/1ipaw6b/guide_how_to_call_assist_from_a_freepbx_voip_phone/)
- [Home Assistant VOIP Integration Docs](https://www.home-assistant.io/integrations/voip/)
- [Home Assistant 2025.5 Release: New Text-to-Speech Voice Variants](https://www.home-assistant.io/blog/2025/05/07/release-20255/#lots-of-new-text-to-speech-voice-variants-for-home-assistant-cloud-subscribers)
- [FormulaOne Card for Home Assistant (GitHub)](https://github.com/marcokreeft87/formulaone-card)
