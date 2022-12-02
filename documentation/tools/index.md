---
layout: default
title: Tools
parent: Documentation
nav_order: 2
---

# Tools
{: .important-title .no_toc}

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

## Network Activity

## Discover

## Alerts

## Log Insights

The Log Insights tab keeps a log of alerts that went off due to clients being geo blocked. Currently this is done with geographic restrictions using CloudFront. The user can click on the log type box in the top left to see that Cloudflare and cognito are planned to be added in the future. 

The Allow IPs option can be used to let specific IPs access the service, even if they are normally geo blocked.

Under the Delivered section are the logs of each client that was geo blocked. This list can be refreshed by clicking on the icon next to the delivered title. Additionally, any of the entries may be expanded to see more information about the event.

The final tool on this page is the Integrations tool. It uses a Webhook URL (which in simple terms can be thought of as an address to communicate with an app), to integrate Enigma Glass with Slack. This will allow users to get Slack notifications automatically, without having to log into Enigma Glass. There are plans to also add email and SMS support in the future.

![Log Insight](./assets/LogInsight.PNG)