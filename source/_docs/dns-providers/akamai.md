---
title: Akamai Domain Configuration
provider: Akamai
dnsprovider: true
description: Learn how to point your Akamai domain to a Pantheon site.
tags: [providers]
permalink: docs/:basename/
editpath: dns-providers/akamai.md/
---
## Before You Begin
Be sure that you have a:


- Registered domain name using Cloudflare to host DNS
- [Paid Pantheon plan](/docs/guides/going-live/plans/)
- [Domain connected](/docs/guides/going-live/domains-https/) to the target Pantheon environment (typically Live)

## Configure DNS Records on Cloudflare
### A Record
1. Click **DNS** in the menu bar.
2. Select **A** from the dropdown menu.
4. Enter **@** in the **Name** field and enter the A record value provided by Pantheon in the **IPv4 Address** field.
5. Set the TTL to **30 minutes**.
6. Disable Cloudflare's CDN by clicking the cloud icon (should be gray, not orange).
6. Click **Add Record**.

### AAAA Records
1. Select **AAAA** from the dropdown menu.
2. Enter **@** in the **Name** field and enter the A record value provided by Pantheon in the **IPv6 Address** field.
3. Set the TTL to **30 minutes**.
4. Disable Cloudflare's CDN by clicking the cloud icon (should be gray, not orange).
5. Click **Add Record**.
6. Repeat steps 1-5 for the second AAAA record value provided by Pantheon. There are two AAAA records for improved uptime and reliability.

### CNAME Record
The CNAME record is only required if you wish to include `www` within your site's primary domain name.

1. Select **CNAME** from the dropdown menu.
2. Enter **www** in the **Name** field and enter the CNAME record value provided by Pantheon (e.g. `live-example.pantheonsite.io`) in the **Domain name** field.
3. Set the TTL to **30 minutes**.
4. Disable Cloudflare's CDN by clicking the cloud icon (should be gray, not orange).
5. Click **Add Record**.

### TXT Record
The TXT record is only required if you need to prove ownership of your domain in order to pre-provision certificates to avoid HTTPS service interruption.

1. Select **TXT** from the dropdown menu.
2. Leave the **Name** field blank and enter the record value provided by Pantheon in the **TXT Content** field.
3. Set the TTL to **30 minutes**.
4. Click **Add Record**.

## Cloudflare Docs

* <a href="https://support.cloudflare.com/hc/en-us/articles/200169046-How-do-I-add-a-CNAME-record-" target="blank">How do I add a CNAME record? <span class="glyphicons glyphicons-new-window-alt"></span></a>
* <a href="https://support.cloudflare.com/hc/en-us/articles/200169096-How-do-I-add-A-records-" target="blank">How do I add A records? <span class="glyphicons glyphicons-new-window-alt"></span></a>

## Next Steps

* [Going Live: Domains & HTTPS](/docs/guides/going-live/domains-https/)
* [Going Live: Redirect to a Primary Domain](/docs/guides/going-live/redirects/)
