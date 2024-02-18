# Failed RDP Attempt Geolocation Analysis

## Overview
This project utilizes a PowerShell script to parse Windows Event Log for failed RDP (Remote Desktop Protocol) attempts and uses a third-party API to geolocate the source of these attacks. By integrating with Azure Sentinel (SIEM), the project sets up a live virtual machine as a honeypot to observe and visualize these attacks on a global scale.
## Features

- **Automated Log Parsing**: Extracts failed RDP attempt data from Windows Event Viewer using PowerShell.
- **IP Geolocation**: Leverages a third-party API to obtain geographic location data from the attacker's IP address.
- **Real-Time Monitoring**: Utilizes a honeypot to monitor live attacks and collect data on attackers' strategies.
- **Threat Visualization**: Plots incoming attacks on a world map using Azure Sentinel, providing a visual overview of the attack landscape over a 24-hour period.

## Tools and Technologies

- **PowerShell**: Scripting language used to automate the extraction of event logs.
- **Azure Sentinel**: Cloud-native SIEM system for log analysis, threat detection, and incident response.
- **Third-Party Geolocation API**: Service used to map IP addresses to geographical locations.
- **Virtual Machine**: Acts as a honeypot to attract and analyze cyberattacks.

## How It Works

1. **Log Extraction**: The PowerShell script filters the Windows Event Logs to identify and extract failed RDP login attempts.


- **Screenshot of PowerShell Capturing all of our nosey friends :)**:
![Screenshot of PowerShell Capturing all of our nosey friends :)](https://i.imgur.com/mRuLU3Y.png)

2. **IP Geolocation**: For each failed attempt, the attacker's IP address is sent to the geolocation API to retrieve location data.
3. **Honeypot Integration**: A virtual machine is set up to simulate a target for attackers, which captures attack data in real time.
4. **Data Aggregation and Visualization**: Azure Sentinel aggregates the data and displays the origins of the attacks on a world map, highlighting the frequency and distribution of the threats

## Visualization Results

The final output is a world map that illustrates the origin points of RDP attacks. Below are the visualizations captured at different intervals:

- **Map after 1 Hour**:
  ![Map after 1 Hour](https://i.imgur.com/74Y6JNN.png)

- **Map after 12 - 15 Hours: (YIKES)**:
  ![Map after 12 - 15 Hours](https://i.imgur.com/duJNJdc.png)

These images showcase the evolution of attack patterns and hotspots over time, providing valuable insights into the distribution of threats against RDP servers.



## Conclusion

This project aids in understanding the global pattern of cyberattacks against RDP servers, allowing for better defense strategies and informed cybersecurity measures.

---
