
# 2025-07-11 - Building an AI-Powered Home Phone Switchboard
# 2025-07-11 - Building an AI-Powered Home Phone Switchboard

---

## Project

This project started with a simple but fun idea:

Could I take an **old red telephone** (a classic analogue phone), and make it part of a modern **AI-powered smart home**?

Here’s the dream:

- Pick up the red phone → speak to an AI assistant
- Control smart home devices (lights, music, sensors, etc.)
- Ask questions and interact with the AI by phone
- Also allow family and friends to **call in** from the outside world
- Allow myself to make calls **out** from my home phones to any normal phone

---

## The System

To make this work, I needed to set up a proper **phone system** at home — also known as a **PBX** (Private Branch Exchange).  
This is what phone companies and businesses use to route calls internally and externally.

![Red Phone Setup](/img/red_phone.jpg)

---

## What I Did Today

---

## 1️⃣ Set Up a PBX Server

- Installed **PBX software** to act as my home phone switchboard.
- The PBX manages calls between devices in the house and connects to the outside phone network.

---

## 2️⃣ Connected the Red Phone

- Used a small device (called a **VOIP adapter**) to connect the **analogue red phone** to the PBX.
- The red phone now acts like a modern phone, linked to the phone system.

---

## 3️⃣ Tested with Mobile Softphone

- Installed a phone app on my **mobile phone** that connects to the PBX.
- I can now use my mobile to make and receive calls over Wi-Fi, as if it were an extension of the home phone system.

---

## 4️⃣ Added a Desk Phone

- Set up a **VOIP desk phone** (a standard office-style phone) in another room.
- It is also connected to the PBX and works just like the other phones.

---

## 5️⃣ Connected to the Outside World

- Set up a **virtual phone number** (a real UK phone number).
- Now:
  - Friends/family can **call the home number**, and the red phone rings.
  - I can use any home phone to **call out** to normal phone numbers.

---

## 6️⃣ Email Notifications

- Configured the system to send **email notifications** for things like:
  - System backups
  - Voicemails
  - Alerts

---

## 7️⃣ Backup System

- Set up an automatic **backup system** for the PBX.
- The PBX now saves copies of its configuration and data regularly to an **external backup server**.
- This ensures that if anything goes wrong, I can easily restore the system.

---

## Result

✅ I can call my **AI assistant** from any home phone to control smart devices.  
✅ I can receive calls from the public phone network at home.  
✅ I can make calls out to any normal phone.  
✅ The system is backed up and sending notifications.  

---

## Next Steps

- Improve the **AI phone assistant** — make it more conversational and able to trigger more smart home routines.
- Add more phones in different rooms.
- Set up monitoring tools to check the PBX health and performance.
- Experiment with advanced call routing (e.g. different voices/phones at different times of day).

---

## Why This Project?

This is more than just a "phone system."  
It’s part of my vision for a **fully integrated smart home**, where even classic devices (like an old red telephone) can interact with the latest AI technologies.

It blends the charm of vintage hardware with modern voice control and automation.

## References

- [How to call Assist from a FreePBX VoIP phone (Reddit Guide)](https://www.reddit.com/r/homeassistant/comments/1ipaw6b/guide_how_to_call_assist_from_a_freepbx_voip_phone/)

- [Home Assistant VOIP Integration Docs](https://www.home-assistant.io/integrations/voip/)

- [Home Assistant 2025.5 Release: New Text-to-Speech Voice Variants](https://www.home-assistant.io/blog/2025/05/07/release-20255/#lots-of-new-text-to-speech-voice-variants-for-home-assistant-cloud-subscribers)

---
