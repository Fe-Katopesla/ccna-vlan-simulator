# 🖧 CCNA Layer 2 VLAN Simulator

![Project Preview](https://via.placeholder.com/1000x400/2c3e50/ffffff?text=VLAN+Simulator+-+Preview)

[![Live Demo](https://img.shields.io/badge/Live-Demo-2ecc71?style=for-the-badge&logo=github)](https://fe-katopesla.github.io/ccna-vlan-simulator/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)]()
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)]()
[![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)]()

This project is an advanced, interactive Network Simulator that demonstrates the concept of **Virtual LANs (VLANs)** and **Broadcast Domain Isolation** at Layer 2. It was built as a hands-on study tool for the **Cisco CCNA (200-125)** certification.

---

## Objective

In a standard switch, a broadcast frame (Destination MAC `FF:FF:FF:FF:FF:FF`) is flooded to all active ports, creating a single, large broadcast domain. This simulator visually proves how **VLANs** solve this problem by logically slicing a single physical switch into multiple isolated virtual switches. 

The core learning objective is to demonstrate that **Layer 2 broadcast traffic is strictly confined within its own VLAN**, improving network performance and security.

---

## Features

* **Dynamic VLAN Assignment:** Use the control panel to reassign any of the 8 PCs to different corporate departments (VLAN 10: Sales, VLAN 20: HR, VLAN 30: IT, VLAN 40: Finance) in real-time.
* **Visual Network Topology:** A dynamic UI where PCs and their network traffic automatically change colors based on their currently assigned VLAN.
* **Broadcast Flooding Animation:** Select a "Sender PC" and trigger a broadcast frame. Watch as the switch actively filters the traffic, animating packets **only** to ports matching the sender's VLAN.
* **Switch Console Logs:** A real-time, color-coded terminal that narrates the switch's internal logic step-by-step (e.g., *"Flooding ports within VLAN 10"*, *"Blocked on Port Fa0/3 - Belongs to VLAN 20"*).
* **Zero Dependencies:** Built entirely with Vanilla JavaScript, HTML5, and CSS3. No frameworks, no external libraries.

---

## How to Run the Project

Since this is a front-end only application, running it is incredibly simple.

### Option 1: Live Demo (Recommended)
**[Access the Online Simulator Here](https://fe-katopesla.github.io/ccna-vlan-simulator/)**

### Option 2: Run Locally
1. Clone this repository to your local machine:
```bash
git clone [https://github.com/fe-katopesla/ccna-vlan-simulator.git](https://github.com/fe-katopesla/ccna-vlan-simulator.git)
```

2. Navigate to the project directory:
```bash
cd ccna-vlan-simulator
 ```
3.Open the index.html file in your favorite web browser.

## Applied CCNA Concepts

By exploring this simulator, you are validating the following networking concepts:

    Broadcast Domains: Understanding how Layer 2 broadcasts propagate.

    VLAN Isolation: Recognizing that devices in different VLANs cannot communicate at Layer 2, even if they are on the same physical switch.

    Logical vs. Physical: Demonstrating that physical location (switch port) does not dictate the logical network segment when VLANs are used.

    Security & Optimization: How confining broadcasts prevents eavesdropping across departments and reduces unnecessary CPU interrupts on end devices.

 ## Technologies Used

    HTML5 / SVG: For the semantic structure and drawing the physical network cables.

    CSS3: For the dashboard layout (Flexbox/Grid), visual state changes, and smooth CSS transitions/animations for the network packets.

    JavaScript (Vanilla): For managing the state of the 8 PCs, triggering animations sequentially using Promises, and dynamically updating the DOM.

    FontAwesome: For the professional UI icons. Applied CCNA Concepts
