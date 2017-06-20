---
title: DreamHost Domain Configuration
provider: DreamHost
dnsprovider: true
description: Learn how to point your DreamHost domain to a Pantheon site.
tags: [providers]
permalink: docs/:basename/
editpath: dns-providers/dreamhost.md/
---
## Before You Begin
Be sure that you have a:


- Registered domain name using DreamHost to host DNS
- [Paid Pantheon plan](/docs/guides/going-live/plans/)
- [Domain connected](/docs/guides/going-live/domains/) to the target Pantheon environment (typically Live)

## Configure DNS Records on DreamHost
### A Record
1. Navigate to **Panel** > **Domains** > **Manage Domains** and click **DNS**.
2. Leave the **Name** field blank, select A from the Type dropdown menu, and enter the A record value provided by Pantheon in the **Value** field.
3. Click **Add record now!**.

### AAAA Records
1. Navigate to **Panel** > **Domains** > **Manage Domains** and click **Add IP**.
2. Click the **Add IPv6 Now** button and enter the AAAA record value provided by Pantheon.
3. Repeat steps 1-2 for the second AAAA record value provided by Pantheon. There are two AAAA records for improved uptime and reliability.

### CNAME Record
The CNAME record is only required if you wish to include `www` within your site's primary domain name.

1. Navigate to **Panel** > **Domains** > **Manage Domains** and click **DNS**.
2. Leave the **Name** field blank, select CNAME from the Type dropdown menu, and enter the enter the CNAME record value provided by Pantheon (e.g. `live-example.pantheonsite.io`) in the **Value** field.
3. Click **Add record now!**.

### TXT Record
The TXT record is only required if you need to prove ownership of your domain in order to pre-provision certificates to avoid HTTPS service interruption.

1. Navigate to **Panel** > **Domains** > **Manage Domains** and click **DNS**.
2. Leave the **Name** field blank, select TXT from the Type dropdown menu, and enter the record value provided by Pantheon in the **Value** field.
3. Click **Add record now!**.

## DreamHost Docs

* <a href="https://help.dreamhost.com/hc/en-us/sections/203272268-DNS-Records" target="blank">DNS Records <span class="glyphicons glyphicons-new-window-alt"></span></a>
* <a href="https://help.dreamhost.com/hc/en-us/articles/215414867-How-do-I-add-custom-DNS-records-" target="blank">How do I add custom DNS records? <span class="glyphicons glyphicons-new-window-alt"></span></a>

## Next Steps

* [Going Live: Domains & HTTPS](/docs/guides/going-live/domains-https/)
* [Going Live: Redirect to a Primary Domain](/docs/guides/going-live/redirects/)
