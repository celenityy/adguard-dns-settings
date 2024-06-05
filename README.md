# adguard-dns-settings

My recommendations for the ultimate AdGuard DNS Configuration :)

# Blocklists

Off to a fun start.

Despite popular opinion, due to the reasons WaLLy3K has listed [here](https://github.com/WaLLy3K/wally3k.github.io?tab=readme-ov-file#why-use-this-over-other-sources), I think it's a good idea to use multiple lists and sources, rather than just limiting yourself to one or two giant lists. I myself constantly notice domains being blocked that were caught by only one list and missed by others. I'm not saying you should go overboard, but I do think it's a good idea to use a variety of high quality lists.

I would generally recommend using the following lists:

**General**

* ⭐️ AdGuard DNS filter *(Enabled by default)*
* ⭐️ AdGuard DNS Popup Hosts filter
* ⭐️ AWAvenue Ads Rule
* ⭐️ Peter Lowe's Blocklist 
* ⭐️ Dan Pollock's List
* ⭐️ HaGeZi's Pro++ Blocklist
* ⭐️ OISD Blocklist Big
* ⭐️ Steven Black's list

If you're fine with a little breakage, I would recommend using HaGeZi's **Ultimate** Blocklist instead of **Multi Pro++**.

**Security**

* ⭐️ Phishing URL Blocklist
* ⭐️ Dandelion Sprout's Anti-Malware List 
* ⭐️ HaGeZi's Badware Hoster Blocklist
* ⭐️ HaGeZi's DynDNS Blocklist
* ⭐️ HaGeZi's The World's Most Abused TLDs (Causes rare breakage but heavily improves security)
* ⭐️ HaGeZi's Threat Intelligence Feeds
* ⭐️ NoCoin Filter List
* ⭐️ Phishing Army
* ⭐️ Scam Blocklist by DurableNapkin
* ⭐️ ShadowWhisperer's Malware List 
* ⭐️ Stalkerware Indicators List
* ⭐️ The Big List of Hacked Malware Web Sites
* ⭐️ uBlock filters - Badware risks
* ⭐️ Malicious URL Blocklist (URLHaus)

**Others**

* ⭐️ Dandelion Sprout's Anti Push Notifications
* ⭐️ Dandelion Sprout's Game Console Adblock List
* ⭐️ HaGeZi's Allowlist Referral (See `User rules` section below)
* ⭐️ Perflyst and Dandelion Sprout's Smart-TV Blocklist
* ⭐️ WindowsSpyBlocker - Hosts spy rules

It might seem like a lot, but these are high quality lists with strong coverage, and it doesn't really hurt to use multiple like this.

# Security

**Block malicious, phishing, and scam domains** -> ✅

**Block newly registered domains** -> ✅ (This will cause very rare breakage, but massively improves security)

# Parental Control 

**Block adult websites** -> ❌ unless you want to, only putting this here since it seems to get turned on by default when Parental Control is enabled

**Safe Search** -> ❌ unless you want to, only putting this here since it seems to get turned on by default when Parental Control is enabled

**YouTube restricted mode** -> ❌ unless you want to, only putting this here since it seems to get turned on by default when Parental Control is enabled

**Blocked services and websites** -> You should add in here any services you don't use or care about. For instance, I usually block `Facebook`, `Instagram`, `LinkedIn`, `TikTok`, & `WhatsApp`, as I don't use or care about any Facebook, LinkedIn, or TikTok services, and I don't want to connect to or be tracked by them.

# User rules

While being nice from a usability perspective, HaGeZi's Referral Allowlist and the AdGuard DNS filter list do allow some questionable ad/tracking domains we don't want unblocked.

You can select `Open editor` and copy and paste the following to keep them blocked:

`||adservice.google.*^$important`

`||adsterra.com^$important`

`||amplitude.com^$important`

`||analytics.edgekey.net^$important`

`||analytics.twitter.com^$important`

`||app.adjust.*^$important`

`||app.*.adjust.com^$important`

`||app.appsflyer.com^$important`

`||doubleclick.net^$important`

`||googleadservices.com^$important`

`||guce.advertising.com^$important`

`||metric.gstatic.com^$important`

`||mmstat.com^$important`

`||statcounter.com^$important`

Note that I maintain a variety of comprehensive blocklists [here](https://codeberg.org/Magnesium1062/blocklists/). Sadly you won't be able to add them to AdGuard DNS, but you may skim through them and manually block whatever you wish to.

Regardless, if you use Apple devices, I would recommend blocking the following that aren't included on most lists for a nice bang for your buck:

`||cdn-xp-ingest.edge.apple^` # Similar to xp.apple.com (See below), except Apple officially admits this is used for "Reporting"

`||cdn-xp-ingest-ab.v.aaplimg.com^` # Similar to xp.apple.com (See below), except Apple officially admits this is used for "Reporting"

`||cdn-xp-ingest.apple.com^` # Related to xp-cdn.apple.com (See below)

`||cdn-xp-ingest-ab.apple.com^` # Related to xp-cdn.apple.com (See below)

`||idiagnostics.apple.com^` # Sends diagnostic data to Apple

`||idiagnostics.apple.com.akadns.net^` # Sends diagnostic data to Apple

`||pancake.apple.com^` # Seems to be used for "home sharing" & telemetry

`||pancake.apple.com.edgekey.net^` # Seems to be used for "home sharing" & telemetry

`||pancake.cdn-apple.com.akadns.net^` # Seems to be used for "home sharing" & telemetry

`||pancake.g.aaplimg.com^` # Seems to be used for "home sharing" & telemetry

`||xp.apple.com^` # General telemetry for various Apple apps & services: https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558. It has also been used for updates, but updates seem to still work without issue with this blocked

`||xp.apple.com.edgekey.net^` # General telemetry for various Apple apps & services: https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558. It has also been used for updates, but updates seem to still work without issue with this blocked

`||xp.itunes-apple.com.akadns.net^` # General telemetry for various Apple apps & services: https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558. It has also been used for updates, but updates seem to still work without issue with this blocked

`||xp-cdn.apple.com^` # Similar to xp.apple.com, except Apple officially admits this is used for "Reporting".

Note that I also maintain a comprehensive whitelist [here](https://codeberg.org/Magnesium1062/blocklists/src/branch/main/whitelist.txt). Sadly you won't be able to add it to AdGuard DNS, but you may skim through it and manually allow whatever you wish to.

# Access settings 

**Block known scanners** -> ✅ (Should be default)

**Respond to blocked domains** -> Default (Other options can cause issues)

**Block Firefox canary domain** -> ✅

**Log IP addresses** -> ❌

# Account settings

**Log DNS requests** -> ✅ (Having logs on is important for troubleshooting breakage)

**Logs retention** -> Last hour

**Statistics retention** -> Last hour

AdGuard account settings -> Settings -> **Password and 2FA** -> Enable 2FA

# Additional recommendations

* Use a privacy-respecting browser like [Firefox](https://www.mozilla.org/firefox/)

* Make sure to configure AdGuard DNS on **both** your OS and in your browser. This will allow you to take advantage of [Encrypted Client Hello](https://blog.cloudflare.com/announcing-encrypted-client-hello).

* Use a content blocking extension like [uBlock Origin](https://github.com/gorhill/uBlock)

* Enable Safe Browsing in your browser if possible and if it's not done in a privacy-invasive way. (You should use i.e. [Google Safe Browsing on "Standard" Mode](https://safebrowsing.google.com/), [Firefox's Safe Browsing](https://support.mozilla.org/kb/how-does-phishing-and-malware-protection-work), [Brave's Safe Browsing](https://brave.com/privacy/browser/#safe-browsing), & [Safari's Fraudulent Website Warning](https://www.apple.com/legal/privacy/data/en/safari/), you should avoid most other options i.e. [Google Safe Browsing on "Enhanced" Mode](https://safebrowsing.google.com/), [Microsoft SmartScreen](https://learn.microsoft.com/windows/security/operating-system-security/virus-and-threat-protection/microsoft-defender-smartscreen/), & [Opera Sitecheck](https://blogs.opera.com/security/2021/01/making-browsing-safe-from-phishing/))

* Use a (reputable) anti-virus if possible. On Windows, you can use the built-in [Microsoft Defender Antivirus](https://en.wikipedia.org/wiki/Microsoft_Defender_Antivirus), on macOS, you can stick to the built-in [XProtect](https://support.apple.com/guide/security/protecting-against-malware-sec469d47bd8/web), on Android, you can use [Hypatia](https://f-droid.org/packages/us.spotco.malwarescanner/), and on Linux, you can use [ClamAV](https://www.clamav.net/). NOTE: You should install Hypatia through the [DivestOS Official Repo](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) instead of F-Droid's main repo, as it will allow you to receive quicker updates directly from the developer. It's also recommended to use [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic/) as your F-Droid client of choice.