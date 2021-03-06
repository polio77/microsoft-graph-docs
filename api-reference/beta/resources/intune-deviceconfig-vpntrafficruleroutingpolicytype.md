---
title: "vpnTrafficRuleRoutingPolicyType enum type"
description: "Specifies the routing policy for a VPN traffic rule."
author: "tfitzmac"
localization_priority: Normal
ms.prod: "Intune"
---

# vpnTrafficRuleRoutingPolicyType enum type

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Specifies the routing policy for a VPN traffic rule.

## Members
|Member|Value|Description|
|:---|:---|:---|
|none|0|No routing policy specified.|
|splitTunnel|1|Network traffic for the specified app will be routed through the VPN.|
|forceTunnel|2|All network traffic will be routed through the VPN.|




