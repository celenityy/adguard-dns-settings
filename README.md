# adguard-dns-settings

My recommendations for the ultimate AdGuard DNS Configuration :)

*For AdGuard Home, see [here](https://codeberg.org/celenity/adguard-home-settings)*.

**NOTE:** This project can be found on both [Codeberg](https://codeberg.org/celenity/adguard-dns-settings), which will act as the main & preferred way to contribute, and [GitHub](https://github.com/celenityy/adguard-dns-settings).

# Blocklists

Off to a fun start.

Despite popular opinion, due to the reasons WaLLy3K has listed [here](https://github.com/WaLLy3K/wally3k.github.io?tab=readme-ov-file#why-use-this-over-other-sources), I think it's a good idea to use multiple lists and sources, rather than just limiting yourself to one or two giant lists. I myself constantly notice domains being blocked that were caught by only one or two lists and missed by others. **I'm not saying you should go overboard, but I do think it's a good idea to use a variety of high quality lists for the best coverage possible.**

I would generally recommend using the following lists:

**General**

* ⭐️ `AdGuard DNS filter` *(Enabled by default)*

* ⭐️ `AdGuard DNS Popup Hosts filter`

* ⭐️ `AWAvenue Ads Rule`

* ⭐️ `Peter Lowe's Blocklist`

* ⭐️ `Dan Pollock's List`

* ⭐️ `HaGeZi's Pro++ Blocklist`

* ⭐️ `OISD Blocklist Big`

* ⭐️ `Steven Black's list`

If you're fine with a little breakage, I would highly recommend using `HaGeZi's `**Ultimate**` Blocklist` instead of `HaGeZi's` **Pro++**` Blocklist`.

**Security**

* ⭐️ `Phishing URL Blocklist`

* ⭐️ `Dandelion Sprout's Anti-Malware List`

* ⭐️ `HaGeZi's Badware Hoster Blocklist`

* ⭐️ `HaGeZi's DynDNS Blocklist`

* ⭐️ `HaGeZi's The World's Most Abused TLDs` *(Causes rare breakage but heavily improves security, I've seen this work in real-time, blocking scam/spam domains before they were picked up by any lists)*

* ⭐️ `HaGeZi's Threat Intelligence Feeds`

* ⭐️ `NoCoin Filter List`

* ⭐️ `Phishing Army`

* ⭐️ `Scam Blocklist by DurableNapkin`

* ⭐️ `ShadowWhisperer's Malware List `

* ⭐️ `Stalkerware Indicators List`

* ⭐️ `The Big List of Hacked Malware Web Sites`

* ⭐️ `uBlock filters - Badware risks`

* ⭐️ `Malicious URL Blocklist (URLHaus)`

**Others**

* ⭐️ `Dandelion Sprout's Anti Push Notifications`

* ⭐️ `Dandelion Sprout's Game Console Adblock List`

* ⭐️ `HaGeZi's Allowlist Referral` *(See `User rules` section below)*

* ⭐️ `Perflyst and Dandelion Sprout's Smart-TV Blocklist`

* ⭐️ `WindowsSpyBlocker - Hosts spy rules`

It might seem like a lot, but these are all high quality lists with strong coverage and minimal false positives in my experience, and it generally doesn't hurt to use them like this.

# Security

**Block malicious, phishing, and scam domains** -> ✅

**Block newly registered domains** -> ✅ *(This will cause very rare breakage, but massively improves security)*

# Parental Control 

**Block adult websites** -> ❌ *(unless you want to, only putting this here since it seems to get turned on by default when `Parental Control` is enabled)*

**Safe Search** -> ❌ *(unless you want to, only putting this here since it seems to get turned on by default when `Parental Control` is enabled)*

**YouTube restricted mode** -> ❌ *(unless you want to, only putting this here since it seems to get turned on by default when `Parental Control` is enabled)*

**Blocked services and websites** -> You should use this feature to your advantage and block any services that you don't use or care about. This can dramatically improve your privacy by preventing connections to them from even being made. If you use a service, don't block it, just block what you're comfortable with and works best for you.

I usually block the following:

* `Facebook`

* `Instagram` *(Facebook)*

* `LinkedIn`

* `QQ`

* `Rakuten Viki`

* `Snapchat`

* `Spotify`

* `TikTok`

* `Viber` *(Rakuten)*

* `VK.com`

* `WeChat`

* `WhatsApp` *(Facebook)*

# User rules

First, we should go ahead and whitelist `adguard-dns.io`, so that we can ensure we can always access our dashboard in case of any rogue filters.

You can do this pretty easily by selecting `Add new rule` -> `Unblock domain` -> **adguard-dns.io**

Now, while being nice from a usability perspective, HaGeZi's Referral Allowlist and the AdGuard DNS filter list do allow some questionable ad/tracking domains we don't want unblocked.

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

Note that I maintain a variety of comprehensive blocklists [here](https://codeberg.org/celenity/BadBlock/). Sadly you won't be able to add them to AdGuard DNS, but you may skim through them and manually block whatever you wish to.

I also maintain a comprehensive whitelist [here](https://codeberg.org/celenity/BadBlock/raw/branch/main/whitelist.txt). Sadly you won't be able to add it to AdGuard DNS, but you may skim through it and manually allow whatever you wish to.

# Access settings 

**Block known scanners** -> ✅ *(Should be default)*

**Respond to blocked domains** -> `Default` *(Other options can cause issues)*

**Block Firefox canary domain** -> ✅

**Log IP addresses** -> ❌

# Account settings

**Log DNS requests** -> ✅ *(Having logs on is important for troubleshooting breakage)*

**Logs retention** -> `Last hour`

**Statistics retention** -> `Last hour`

AdGuard account settings -> Settings -> **Password and 2FA** -> Enable 2FA

# Additional recommendations

* Use a privacy-respecting browser like [Firefox](https://www.mozilla.org/firefox/) with a user.js like [Arkenfox](https://github.com/arkenfox/user.js).

* Make sure to configure AdGuard DNS on **both** your OS and in your browser. This will allow you to take advantage of [Encrypted Client Hello](https://blog.cloudflare.com/announcing-encrypted-client-hello).

* Use a content blocking extension like [uBlock Origin](https://github.com/gorhill/uBlock). *(See recommended settings [here](https://codeberg.org/celenity/ublock-origin-settings))*

* Enable Safe Browsing in your browser if possible and if it's not done in a privacy-invasive way. (You should use i.e. [Google Safe Browsing on "Standard" Mode](https://safebrowsing.google.com/), [Firefox's Safe Browsing](https://support.mozilla.org/kb/how-does-phishing-and-malware-protection-work), [Brave's Safe Browsing](https://brave.com/privacy/browser/#safe-browsing), & [Safari's Fraudulent Website Warning](https://www.apple.com/legal/privacy/data/en/safari/), you should avoid most other options i.e. [Google Safe Browsing on "Enhanced" Mode](https://safebrowsing.google.com/), [Microsoft SmartScreen](https://learn.microsoft.com/windows/security/operating-system-security/virus-and-threat-protection/microsoft-defender-smartscreen/), & [Opera Sitecheck](https://blogs.opera.com/security/2021/01/making-browsing-safe-from-phishing/)).

* Use a (reputable) anti-virus if possible. On Windows, you can use the built-in [Microsoft Defender Antivirus](https://wikipedia.org/wiki/Microsoft_Defender_Antivirus), on macOS, you can stick to the built-in [XProtect](https://support.apple.com/guide/security/protecting-against-malware-sec469d47bd8/web), on Android, you can use [Hypatia](https://f-droid.org/packages/us.spotco.malwarescanner/), and on Linux, you can use [ClamAV](https://www.clamav.net/). **NOTE:** You should install Hypatia through the [DivestOS Official Repo](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) instead of F-Droid's main repo, as it will allow you to receive quicker updates directly from the developer. It's also recommended to use [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic/) as your F-Droid client of choice.