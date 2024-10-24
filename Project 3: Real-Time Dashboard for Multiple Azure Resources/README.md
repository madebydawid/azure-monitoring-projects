## Project 3: Creating a Real-Time Dashboard for Multiple Azure Resources

## Overview
In this project, I created an Azure Monitor Dashboard that provides real-time data for CPU usage, memory usage, and network activity across three virtual machines (VMs). It involved configuring alerts, testing with data, configuring RBAC and setting up an automated response using Azure Automation.

**This project includes**:
- Monitoring CPU and RAM usage on VM1 and VM2.
- Monitoring Network In/Out traffic on VM3 with an automation runbook triggered when thresholds are exceeded.
- Use of iperf3 to simulate network traffic and test automated responses.

## Objectives
- Set up a custom Azure Monitor dashboard.
- Monitor and display real-time data for CPU, memory, and network activity.
- Automate responses using Azure Automation Runbooks.
- Trigger email alerts based on set thresholds for CPU, RAM, and network usage.

## Steps to Reproduce

<details>
  
### 1. Create a New Dashboard

- Go to the Azure Portal and select **Dashboards** from the menu.
- Click on **New Dashboard** and choose **Blank Dashboard** to create a new one from scratch.
- Name your dashboard according to the resources you’ll be monitoring.

### 2. Add Resource Widgets

- In your new dashboard, select **Add tile** to add widgets for each monitoring point.
- Choose **Metrics Chart** from the widget options, and select the first resource you want to monitor.
- Choose **Percentage CPU** as the metric and adjust the time interval for real-time updates.
- Repeat for **Memory Usage** and **Network In/Out** if you want to monitor these as well.

### 3. Configure Alerts

- Set up alerts for the monitored resources (e.g., CPU, memory, and network traffic).
- Define thresholds to trigger email alerts and automated responses using Azure Monitor's alerting system.
- For VM1 and VM2, configure alerts to send email notifications when thresholds are crossed.

### 4. Configure Network Traffic

- Set up a network traffic threshold on VM3 to monitor network in/out activity.
- Ensure VM3 has an inbound security rule for TCP traffic on port 5201 to allow traffic from VM2.

### 5. Test the Runbook

- Set up a simple PowerShell runbook in Azure Automation.
- Ensure that the runbook is linked to the alert and responds to network traffic thresholds by performing tasks such as checking VM status.
- After simulating traffic, check the **Runbook Jobs** pane for successful completion.

### 6. Customize and Save the Dashboard

- Organize the dashboard layout for clarity by grouping related widgets.
- Use filtering options to focus on relevant data.
- Save and, if needed, publish the dashboard for other users.
</details>

## Project Learnings

- Learned how to set up a real-time monitoring dashboard in Azure Monitor.
- Gained experience configuring alerts for CPU, memory, and network metrics.
- Successfully implemented an automated response using Azure Automation.
- Understood the importance of configuring network rules and Azure RBAC for security and automation.

## Next Steps

- Implement more granular user access controls on the dashboard.
- Integrate Log Analytics for deeper insights into metrics.
- Expand automation responses based on additional monitoring conditions.

## Screenshots

- Screenshot of Dashboard Layout
- CPU and Memory Monitoring Widget
- Network Activity Monitoring Widget
- Runbook Execution Confirmation

## Resources

- [Azure Monitor Dashboard Documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/visualize/tutorial-dashboards)
- [Azure Metrics Documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/data-platform-metrics)
- [Azure Automation Runbook Documentation](https://learn.microsoft.com/en-us/azure/automation/automation-runbook-execution)
