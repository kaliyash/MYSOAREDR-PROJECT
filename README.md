# MYSOAREDR-PROJECT
This project is a fully integrated Security Orchestration, Automation, and Response (SOAR) ecosystem built to work alongside Endpoint Detection and Response (EDR) solutions. It provides a modular, scalable, and automated framework for detecting, analyzing, and responding to endpoint threats in real time.
verview

This project integrates Lima Charlie (an EDR platform) with Tines (a SOAR automation tool) to detect and respond to potential security threats. It automates incident detection, notification, and response, including an analyst decision-making process for isolating compromised devices.

# Workflow

1. Monitoring with Lima Charlie

Lima Charlie continuously monitors endpoints for suspicious activities.

If a suspicious event is detected, Lima Charlie generates an alert.

2. Alert Handling with Tines

Tines receives the alert from Lima Charlie and triggers an automation workflow.

Tines sends an alert email to security analysts with details of the event.

3. Analyst Decision via Web Interface

A web page is generated with event details and an isolation decision prompt (Yes/No).

The security analyst reviews the alert and selects an action:

Yes (True Positive) → Device is isolated.

No (False Positive) → No isolation occurs.

4. Incident Response Actions

If True Positive:

The affected device is isolated using Lima Charlie's response capabilities.

A confirmation email is sent to stakeholders, notifying them of the isolation action.

If False Positive:

No isolation occurs.

A false positive notification email is sent to the client.


# Technical Components

Lima Charlie: Endpoint detection and response (EDR) tool.

Tines: SOAR platform for automation and orchestration.

Web Interface: Simple decision-making page for security analysts.

Email Notifications: Alerts and confirmations for different stakeholders.

Setup Instructions

1. Configure Lima Charlie:

Set up agents on endpoints for monitoring.

Define detection rules for suspicious activities.

2. Integrate Lima Charlie with Tines:

Configure Lima Charlie to send alerts to Tines.

Create a Tines workflow to handle alerts and send emails.


3. Deploy Web Interface:

Build a basic web page with a Yes/No prompt.

Connect the web interface to Tines for decision logging.


4. Automate Incident Response:

Set up Tines actions for device isolation (via Lima Charlie API).

Configure email notifications for different scenarios.

Future Enhancements

Integration with SIEM solutions for broader security visibility.

Custom dashboards for real-time threat monitoring.

---
This project enhances security operations by automating alert responses and ensuring analysts have the final say in isolating compromised devices. Lima Charlie provides robust endpoint detection, while Tines orchestrates efficient response workflows.


## Example Email Flow
Initial Alert:

"Suspicious activity detected on endpoint X."

True Positive:

"The analyst has confirmed a True Positive. The endpoint has been successfully isolated."

False Positive:

"The alert was reviewed and marked as a False Positive. No further action has been taken."

#AUTHOR
👤 Yashwardhan Singh
👤 Ojas Gaur
######  Feel free to submit issues or pull requests for enhancements or bug fixes. ######
