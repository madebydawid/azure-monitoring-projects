## Project 3: Creating a Real-Time Dashboard for Multiple Azure Resources

## Overview
In this project, I created an Azure Monitor Dashboard to display real-time data for CPU usage, memory usage, and network activity for multiple virtual machines. This project demonstrates how to create a custom dashboard in Azure to visualize multiple monitoring points in one place, making it easier to get an overview of resource status.

## Objectives
- Create a custom dashboard in Azure Monitor.
- Add widgets for real-time monitoring of CPU, memory, and network activity for multiple resources.
- Understand how to customize and filter data in a dashboard.

## Steps to Reproduce

1. **Create a New Dashboard**
   - Go to the Azure Portal and select **Dashboards** from the menu.
   - Click on **New Dashboard** and choose **Blank Dashboard** to create a new one from scratch.
   - Name your dashboard according to the resources you’ll be monitoring.

2. **Add Resource Widgets**
   - In your new dashboard, select **Add tile** to add widgets for each monitoring point.
   - Choose **Metrics Chart** from the widget options, and select the first resource you want to monitor.
   - Choose **Percentage CPU** as the metric and adjust the time interval for real-time updates.
   - Repeat for **Memory Usage** and **Network In/Out** if you want to monitor these as well.

3. **Customize and Organize Widgets**
   - Drag and drop the widgets to optimize the layout. Group them logically for a clear overview.
   - Use the filtering options to display only relevant data and avoid clutter.

4. **Add Additional Resources**
   - To monitor more than one VM, repeat step 2 for each additional resource, ensuring all monitoring points are represented.

5. **Save and Publish the Dashboard**
   - Once all widgets are added and organized, click **Save**. Your dashboard is now ready to use.
   - If you want, you can publish the dashboard to make it accessible to other users within your organization.

## Screenshots
![Screenshot of Dashboard Layout](#)
![CPU and Memory Monitoring Widget](#)
![Network Activity Monitoring Widget](#)

## Project Learnings
- Learned how to create a dashboard to monitor multiple Azure resources in real-time.
- Developed skills in organizing and presenting monitoring data for effective resource management.
- Understood how to use filtering and customization features to optimize visual information.

## Next Steps
- Implement user roles to restrict access to different parts of the dashboard.
- Explore the possibility of adding Log Analytics for more advanced data analysis.
- Create automated alerts based on metrics in the dashboard.

## Resources
- [Azure Monitor Dashboard Documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/visualize/overview)
- [Azure Metrics Documentation](https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/data-platform-metrics)
