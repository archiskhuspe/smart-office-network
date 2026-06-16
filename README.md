# Smart Office Network

![Cisco Packet Tracer](https://img.shields.io/badge/Cisco-Packet%20Tracer%208.1.1-1BA0D7?logo=cisco)
![License](https://img.shields.io/badge/license-MIT-green)

A Cisco Packet Tracer simulation of an IoT smart building network. The simulation models a three-layer IoT architecture — perception, network, and application — with smart devices for security, energy management, and remote control, all connected through a WLAN to a central IoT backend server.

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [How It Works](#how-it-works)
- [Prerequisites](#prerequisites)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Limitations](#limitations)
- [License](#license)

## Features

- **RFID door lock** — access control via Radio Frequency Identification
- **Solar-powered devices** — LED, lamp, and fan running on simulated solar battery
- **Remote device control** — fan, coffee maker, and music player controllable from the IoT browser homepage
- **Auto-dimming street lamp** — brightness adjusts based on time of day
- **Smoke-triggered garage** — garage door opens automatically on smoke detection
- **Fire sprinkler with siren** — automated fire response system
- **IoT browser homepage** — centralised dashboard to monitor and interact with all connected devices

## Tech Stack

- **Simulation tool:** Cisco Packet Tracer 8.1.1
- **Network:** WLAN (wireless), DHCP for IoT devices, static IP for IoT servers
- **IoT architecture:** Three-layer — Perception (sensors/RFID/actuators), Network (router/gateway), Application (cloud/IoT server)

## How It Works

The simulation is organised into three logical network areas: **sensors**, **servers**, and **devices**.

1. **Perception layer** — Smart devices (sensors, RFID tags, actuators) are wired to microcontrollers which connect wirelessly to a home gateway.
2. **Network layer** — The gateway forwards data to the cloud via a modem. The WLAN router uses a shared SSID and password; wireless devices obtain IPs via DHCP while IoT servers use static IPs to ensure stable addressing.
3. **Application layer** — An IoT backend server hosts a browser-accessible homepage where end-users can view device status and trigger actions remotely from smartphones or PCs over the wireless LAN or cell tower connection.

Both **real-time mode** (devices behave as live hardware) and **simulation mode** (packet-level traffic visualisation between nodes) are configured and testable within the `.pkt` file.

## Prerequisites

- [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) 8.1.1 or later (free with a Cisco Networking Academy account)

## Usage

1. Install Cisco Packet Tracer 8.1.1+.
2. Open `smart_office_network.pkt`.
3. Use **Simulation mode** to step through packet traffic between IoT devices and the server, or switch to **Real-time mode** to interact with devices live.
4. Open the IoT browser homepage from any simulated PC or smartphone to monitor and control connected smart devices.

## Project Structure

```
smart-office-network/
├── smart_office_network.pkt   # Cisco Packet Tracer simulation
├── research_paper.pdf         # Paper: "Build a network for Smart Building"
├── literature_survey.pdf      # Survey of related IoT research papers
├── .gitignore
├── LICENSE
└── README.md
```

## Limitations

- Fully virtual simulation — no physical hardware or real network traffic is involved.
- Requires Cisco Packet Tracer to open; the `.pkt` file is a proprietary binary format.
- IoT device behaviour is limited to what Cisco Packet Tracer's built-in IoT components support; real-world protocols (MQTT, CoAP) are not used.
- Network scale and device count are constrained by Packet Tracer's simulation environment.

## License

Released under the [MIT License](LICENSE).
