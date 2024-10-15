## Project 1: Monitoring CPU Usage on an Azure Virtual Machine

### Overview
In this project, I configured Azure Monitor to track the CPU usage on a virtual machine (VM) and set up an alert rule to send a notification if the CPU usage exceeds 80%. This project showcases how to create a VM, configure monitoring, and set up alerts.

> (Note: The whole alert process can be made during the initial VM setup [as seen here](https://github.com/madebydawid/azure-monitoring-projects/blob/main/Project%201:%20CPU-monitoring/images/VM_alert_shortcut.png?raw=true), but for the purpose of demonstration the whole setup is included below.)

### Objectives
- Create a virtual machine in Azure.
- Monitor the virtual machine's CPU usage with Azure Monitor.
- Set up an alert rule to trigger when CPU usage exceeds 80%.
- Receive email notifications when the alert is triggered.

### Steps to Reproduce

1. **Create a Virtual Machine**
   - Go to the Azure portal and create a new virtual machine.
   - Choose your OS (e.g., Windows or Linux) and configure the instance with basic settings.
   - Ensure that the VM is in the same resource group where you will be configuring monitoring.

2. **Configure CPU Monitoring**
   - Navigate to the Azure Monitor service.
   - Under Metrics, select your VM as the resource.
   - Choose **Percentage CPU** as the metric and visualize it on the graph.

3. **Set up the CPU Alert**
   - In Azure Monitor, go to **Alerts** and create a new alert rule.
   - Choose **Percentage CPU** as the signal, set the threshold to 80%, and configure the action group to send an email notification.

4. **Simulate CPU Load**
   - Use either PowerShell (for Windows) or `stress` (for Linux) to simulate high CPU usage on the VM and trigger the alert.
   - Check that the email notification is received as expected.

### Screenshots

[CPU Monitoring](https://github.com/madebydawid/azure-monitoring-projects/blob/main/Project%201:%20CPU-monitoring/images/Create_VM.png?raw=true)

[Alert Rule](https://github.com/madebydawid/azure-monitoring-projects/blob/main/Project%201:%20CPU-monitoring/images/Alert_rule.png?raw=true)
            

[Email Notification](https://github.com/madebydawid/azure-monitoring-projects/blob/main/Project%201:%20CPU-monitoring/images/notification.png?raw=true)

[Shortcut Alert Rule in VM creation](https://github.com/madebydawid/azure-monitoring-projects/blob/main/Project%201:%20CPU-monitoring/images/VM_alert_shortcut.png?raw=true)



### Project Learnings
- Gained experience with Azure Monitor to track resource performance.
- Implemented an alert system to notify administrators of potential performance bottlenecks.
- Learned how to simulate high CPU usage to test the alerting functionality.

### Next Steps
- Extend the monitoring to other metrics like disk IOPS, memory usage, and network traffic.
- Automate alert rule creation using Terraform in future projects.

### Resources
- [Azure Monitor Documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/overview)
- [Simulating CPU Load in a VM](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-vm)
