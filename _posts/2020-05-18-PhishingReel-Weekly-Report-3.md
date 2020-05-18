---
title: "PhishingReel Weekly Report 3"
categories:
  - PhishingReel Reports
tags:
  - PhishingReel
  - Phishing Kits
header: 
  teaser: "/assets/images/pr-weeklyreport/2020-05-18-fig2.png"
---

<style>
table {
    display:table;
    width:100%;
}
</style>
# 👋🤖
[PhishingReel](https://twitter.com/phishingreel) monitors and scans the internet to find these kits being deployed and monitors their activity until the domain is taken down. These reports serve as a weekly update on the current state and trends within the world of SaaS phishing kits.

This report only contains summarised analysis of detections for the week. For further information or access to feeds to enrich your own data, please contact me via [Twitter](https://twitter.com/sysgoblin) or [Keybase](https://keybase.com/sysg0blin).
{: .notice--danger}

## 👓 Overview

| |Total|Trend|
|---|---|:---:|
| Total detections | 917 |🔼 |
| Unique emails | 226 |🔼 |
| Unique panels | 11 |🔽 |
| Unique IP's | 214 |🔼 |
| Kits downloaded | 226 |🔼 |
| Unique domains | 629 |🔼 |


**Note:** Unique domains do not include subdomains.
{: .notice--info}

## 🔎 Top Kit Detections
![top kits graph](/assets/images/pr-weeklyreport/2020-05-18-fig1.png)

{% capture notice-1 %}
The top 5 kits were deployed a total of **862** times over the past week.
{% endcapture %}

<div class="notice--info">
  {{ notice-1 | markdownify }}
</div>

## 📈 Detections Over Time
![detections ot graph](/assets/images/pr-weeklyreport/2020-05-18-fig2.png)

{% capture notice-2 %}
Out of the top 5 kits for the past week the date with the highest detections was **2020-05-14** with **192** for that day.  
{% endcapture %}

<div class="notice--info">
  {{ notice-2 | markdownify }}
</div>

## 📧 Top 5 Emails

|Emails|Count|
|---|---:|
| `pokoknyasetor@yandex.com, comback@jagadpro.com` | 21 |
| `jadijadiiandwdwd@yandex.com, admindilan@16shop.us` | 11 |
| `jalanterus91@yandex.com, ys@youngsister.com` | 11 |
| `kawanresult@yandex.com, sayang@shintanaomi.com` | 9 |
| `sibolangsibocahpetuaberenang@yandex.com, andi@dbsg.us` | 8 |


{% capture notice-0 %}
Top 5 most commonly discovered kit owner emails detected over the past week. These emails will receive victim information from the associated phishing kits they own.
{% endcapture %}

<div class="notice--info">
  {{ notice-0 | markdownify }}
</div>

## 📞 Top 5 IP's

|IP Address|Count|Trend|
|---|---:|:---:|
| `162.241.115.246` | 19 |🔼 |
| `188.213.174.50` | 19 |🆕 |
| `162.241.67.39` | 17 |🆕 |
| `162.241.201.38` | 16 |🆕 |
| `162.241.115.158` | 15 |🆕 |


{% capture notice-ip %}
Top IP's for the week which have had the most detections. Recurring IP's should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🌐 Top 5 Domains

|Domain|Count|Trend|
|---|---:|:---:|
|`serveirc.com`|24|⏹ |
|`giize.com`|21|🆕 |
|`gleeze.com`|15|🔼 |
|`kozow.com`|15|🆕 |
|`servebeer.com`|14|🆕 |


{% capture notice-ip %}
Top domains for the week where commercial phishing kits have been detected. These domains should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🔢 Top 5 Kit hashes

|SHA1 Hash|Count|Trend|
|---|---:|:---:|
| `09bb0127e1951f268c5dc7114bde98d70e0ba592` | 9 |🆕 |
| `4f514599543e419353e48e37d6a7ce38a6f22110` | 8 |🆕 |
| `611a600213426262524c5b8b08d6507f9ec4a054` | 6 |🆕 |
| `8125f95fd9cb111b9770639eeee3dfe0f0b7cce9` | 6 |🆕 |
| `8b6522c1ff29e04bae3401b9b5b85f677736d3e3` | 6 |🆕 |


{% capture notice-hash %}
Top hashes of known malicious kits downloaded by PhishingReel. These hashes can be used to pivot for extra data on sites such as VirusTotal, Any.Run and many others.
{% endcapture %}

<div class="notice--info">
  {{ notice-hash | markdownify }}
</div>
