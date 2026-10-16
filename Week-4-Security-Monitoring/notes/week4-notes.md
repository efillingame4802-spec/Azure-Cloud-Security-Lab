Week 4 - Security Monitoring

  Resources Deployed
  
      Log Analytics Workspace
      Microsoft Sentinel
      Azure Activity Connector
      Windows Security Events via AMA
      Syslog via AMA
      Windows Data Collection Rule
      Linux Data Collection Rule
      
  Portal Architecture
      
      Microsoft Defender Portal:
          Sentinel Content Hub
          Data Connectors
          Analytics
          Incidents
          Automation

      Azure Portal:
          Log Analytics Workspace
          Virtual Machines
          Azure Monitor Agent Extensions
          Data Collection Rules
          Azure Activity Log
          Cost Management
  Data Sources
  
      AzureActivity
      SecurityEvent
      Syslog
      Heartbeat
  Azure Monitoring
  
      Azure Activity solution installed
      Subscription Activity Log forwarded to Log Analytics
      AzureActivity ingestion validated with KQL
      Policy remediation failure investigated
      Subscription diagnostic setting verified or created
  Windows Monitoring
  
      Windows Security Events solution installed
      AzureMonitorWindowsAgent deployed
      Minimal event collection selected
      Windows DCR associated with vm-win2022
      SecurityEvent ingestion validated

  Linux Monitoring
  
      Syslog solution installed
      AzureMonitorLinuxAgent deployed
      Selected Syslog facilities collected
      LOG_DEBUG excluded
      Linux DCR associated with vm-ubuntu
      Custom logger messages generated
      Syslog ingestion validated
  Cost Management
  
      $15 Azure subscription budget configured
      Actual-cost and forecast-cost alerts configured
      Windows collection limited to Minimal
      Linux facilities and severities restricted
      Pre-ingestion and post-ingestion usage compared
      VMs deallocated after telemetry validation
  Troubleshooting
  
      Sentinel management moved to the Microsoft Defender portal
      Azure Activity policy remediation initially failed
      Subscription diagnostic setting inspected
      Windows AMA deployment required the VM to remain running
      Linux AMA deployment required the VM to remain running
      iptables loopback rule initially appeared as an unrestricted anywhere rule
      Numeric and verbose iptables output clarified rule interfaces
      DCR associations verified independently from agent extensions
  Lessons Learned
  
      Microsoft Sentinel uses a Log Analytics workspace for analytics data.
      
      The Microsoft Defender portal provides the current unified Sentinel experience.
      
      Data connectors require their associated Content Hub solutions.
      
      Azure Monitor Agent uses Data Collection Rules to determine what data is collected.
      
      Agent installation and DCR association are separate requirements.
      
      Windows and Linux logs are stored in different tables.
      
      Connector status alone does not prove ingestion.
      
      KQL provides direct validation of event delivery and freshness.
      
      Azure budgets send alerts but do not automatically stop services.
      
      Restricting event collection reduces cost and unnecessary noise. 
Future Improvements

    Create custom analytics rules
    Build Sentinel workbooks
    Map detections to MITRE ATT&CK
    Perform controlled attack simulations
    Develop threat-hunting queries
    Create Sentinel incidents
    Automate incident response with Logic Apps
    Deploy monitoring infrastructure with Terraform
