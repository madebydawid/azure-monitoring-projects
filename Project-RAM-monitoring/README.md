# Project 2: Monitoring Memory Usage on an Azure Virtual Machine

## Overview
In this project, I configured Azure Monitor to track the memory usage on a virtual machine (VM) and set up an alert rule to send a notification if the available memory falls below a defined threshold. This project demonstrates how to monitor memory usage on a VM, set up alert rules, and simulate memory load for testing.

> **Note:** Memory monitoring can be included during the initial VM setup, but this guide covers the entire setup process for clarity.

## Objectives
1. Monitor the VM's available memory with Azure Monitor.
2. Set up an alert rule to trigger when available memory is below 600 MB.
3. Receive email notifications when the alert is triggered.

## Steps to Reproduce

### Configure Memory Monitoring
1. Navigate to the Azure Monitor service.
2. Under **Metrics**, select your VM as the resource.
3. Choose **Memory Available Bytes** as the metric and visualize it on the graph.

### Set up the Memory Alert
1. In Azure Monitor, go to **Alerts** and create a new alert rule.
2. Choose **Memory Available Bytes** as the signal, set the threshold to 600 MB (or your own preference), and configure the action group to send an email notification.

### Simulate Memory Load
1. Install `stress-ng` to simulate memory usage on your VM (Linux only):
   ```bash
   sudo apt update
   sudo apt install stress-ng -y
   sudo stress-ng --vm 1 --vm-bytes 90% --vm-hang 0 --timeout 60s
2. This will consume 90% of available memory for 60 seconds, triggering the alert if memory drops below the threshold.

### Verify Email Notification
1. Check your email to confirm the notification was received. Adjust thresholds or rerun the simulation as necessary.

### Screenshots

- [Memory Monitoring](https://github.com/madebydawid/azure-monitoring-projects/blob/main/Project-RAM-monitoring/images/vm-ram-metrics.jpg?raw=true)

- [Alert Rule Configuration](https://github.com/madebydawid/azure-monitoring-projects/blob/main/Project-RAM-monitoring/images/alert-rule%20-%20Copy.jpg?raw=true)

- [Email Notification](https://github.com/madebydawid/azure-monitoring-projects/blob/main/Project-RAM-monitoring/images/ram-alert-rule-email.jpg?raw=true)

### Project Learnings
- Gained experience with Azure Monitor to track VM memory usage.
- Learned to create and test alerts for resource monitoring.
- Enhanced skills in simulating memory load on VMs to validate alert functionality.
  
### Next Steps
- Extend monitoring to additional metrics like disk IOPS, CPU usage, and network traffic.
- Automate the alert rule setup using Terraform in future projects.

### Resources

- [Azure Monitor-Metrics](https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/data-platform-metrics)

- [Azure Monitor-Alerts](https://learn.microsoft.com/en-us/azure/azure-monitor/alerts/alerts-overview)

- [Simulating Memory Loadn on Linux](https://manpages.ubuntu.com/manpages/bionic/man1/stress-ng.1.html)
