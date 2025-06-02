# Cloud Monitoring - Qwik Start

1. Create a Compute Engine instance
  - In the Cloud console, on the Navigation menu (☰), click Compute Engine > VM Instances, then click Create instance.
  - Create VM

2. Add Apache2 HTTP Server to your instance
  - SSH into your instance
  - Install Apache2 HTTP Server
    ```bash
    sudo apt update
    sudo apt-get install apache2 php7.0
    ```
  - Start the Apache2 service
    ```bash
    sudo service apache2 restart
    ```
3. Create a Monitoring Metrics Scope
  - In the Cloud Console, click Navigation menu (Navigation menu icon) > View All Products > Observability > Monitoring.
  - Install the Monitoring and Logging agents
  - Run the Monitoring agent install script command in the SSH terminal of your VM instance to install the Cloud Monitoring agent:
    ```bash
    curl -sSO https://dl.google.com/cloudagents/add-google-cloud-ops-agent-repo.sh
    sudo bash add-google-cloud-ops-agent-repo.sh --also-install
    ```
  - Verify the agent is running
    ```bash
    sudo systemctl status google-cloud-ops-agent"*"
    ```
  
4. Create an uptime check
  - In the Cloud Console, in the left menu, click Uptime checks, and then click Create Uptime Check.
  - For Protocol, select HTTP.
  - For Resource Type, select Instance.
  - For Instance, select lamp-1-vm.
  - For Check Frequency, select 1 minute.
  - Click Continue.
  - In Response Validation, accept the defaults and then click Continue.
  - In Alert & Notification, accept the defaults, and then click Continue.
  - For Title, type Lamp Uptime Check.
  - Click Test to verify that your uptime check can connect to the resource.
  - When you see a green check mark everything can connect.
  - Click Create.

5. Create an alerting policy
  - In the left menu, click Alerting, and then click +Create Policy.
  - Click on Select a metric dropdown. Uncheck the Active.
  - Type Network traffic in filter by resource and metric name and click on VM instance > Interface. Select Network traffic (agent.googleapis.com/interface/traffic) and click Apply. Leave all other fields at the default value.
  - Click Next.
  - Set the Threshold position to Above threshold, Threshold value to 500 and Advanced Options > Retest window to 1 min. Click Next.
  - Click on the drop down arrow next to Notification Channels, then click on Manage Notification Channels.
  - A Notification channels page will open in a new tab.
  - Scroll down the page and click on ADD NEW for Email.
  - In the Create Email Channel dialog box, enter your personal email address in the Email Address field and a Display name.
  - Click on Save.
  - Go back to the previous Create alerting policy tab.
  - Click on Notification Channels again, then click on the Refresh icon to get the display name you mentioned in the previous step.
  - Click on Notification Channels again if necessary, select your Display name and click OK.
  - Add a message in documentation, which will be included in the emailed alert.
  - Mention the Alert name as Inbound Traffic Alert.
  - Click Next.
  - Review the alert and click Create Policy.

5. Create a dashboard
  - In the left menu select Dashboards, and then +Create Custom Dashboard.
  - Name the dashboard Cloud Monitoring LAMP Qwik Start Dashboard.
  - Add the first chart
  - Click on + ADD WIDGET
  - Select the Line option under Visualization in the Add widget.
  - Name the Widget title CPU Load.
  - Click on Select a metric dropdown. Uncheck the Active.
  - Type CPU load (1m) in filter by resource and metric name and click on VM instance > Cpu. Select CPU load (1m) and click Apply. Leave all other fields at the default value. Refresh the tab to view the graph.

