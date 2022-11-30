# Event-driven workflow examples

The repository contains event-driven workflows which can be used to demonstrate how to build Direktiv workflows. The following workflows are contained in this repository:
- **[aws-events/aws-cloudevents-freshservice.yaml](https://github.com/wwonigkeit/event-workflows#aws-eventsaws-cloudevents-freshserviceyaml):** workflow which receives and process AWS EC2 instances state changes (via EventBridge CloudEvents) to Freshservice CMDB
- **[aws-events/print-aws-events.yaml](https://github.com/wwonigkeit/event-workflows#aws-eventsaws-cloudevents-freshserviceyaml-1):** gets the latest value of a Bitcoin in USD and compares it to the previously stored value

## aws-events/aws-cloudevents-freshservice.yaml
### Description

This workflow uses events created by AWS EventBridge. For every state a virtual machine reports (EC2 type instance), the workflow will verify whether the machine exists in FreshService CMDB, then update the status of the machine or create the machine. Follow the guide on the documentation page to configure AWS EventBridge to forward CloudEvents to your Direktiv namespace: https://docs.direktiv.io/v0.6.6/events/cloud/amazon/

### Requirements

 - The FreshService URL: In the format https://direktiv.freshservice.com
 - The FreshService Username: Username used to log into FreshService portal
 - The FreshService Password: Password for the user
 - AWS Key: AWS key (created in IAM)
 - AWS Secret: AWS secret (created in IAM)
 - AWS Region: AWS region code

Run the setup_demo.yaml workflow. The workflow needs the following to create the above secrets and variables:
 - Direktiv URL: typicall https://demo.direktiv.io or http://localhost:8080
 - Direktiv Namespace: namespace created for the workflows
 - Direktiv Token: Direktiv API token configured for the docker container (opensource) or created in Permissions (enterprise)

## aws-events/aws-cloudevents-freshservice.yaml
### Description

Description

### Requirements

Requirements