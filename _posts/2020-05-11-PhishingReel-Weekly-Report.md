---
title: "PhishingReel Weekly Report 2020-05-11"
categories:
  - PhishingReel Reports
tags:
  - PhishingReel
  - Phishing Kits
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
|---|:---|:---:|
| Total detections | 758 | 🔼 |
| Unique emails | 147 | 🔽 |
| Unique panels | 13 | 🔽 |
| Unique IP's | 204 | 🔽 |
| Kits downloaded | 147 | 🔼 |
| Unique domains | 624 | 🔽 |


**Note:** Unique domains do not include subdomains.
{: .notice--info}

## 🔎 Top Kit Detections
![top kits graph](/assets/images/pr-weeklyreport/2020-05-11-fig1.png)

{% capture notice-1 %}
The top 5 kits were deployed a total of **713** times over the past week.
{% endcapture %}

<div class="notice--info">
  {{ notice-1 | markdownify }}
</div>

## 📈 Detections Over Time
![detections ot graph](/assets/images/pr-weeklyreport/2020-05-11-fig2.png)

{% capture notice-2 %}
Out of the top 5 kits for the past week the date with the highest detections was **2020-05-04** with **133** for that day.  
{% endcapture %}

<div class="notice--info">
  {{ notice-2 | markdownify }}
</div>

## 📧 Top 5 Emails

|Emails|Count|
|---|---:|
| `resultcendoll@yandex.com, inbox@ccmasuk.com` | 12 |
| `jalanterus91@yandex.com, ys@youngsister.com` | 12 |
| `irwanganteng1337@gmail.com, admin@16shop.us` | 8 |
| `domainkuya99@gmail.com, 16shop.co` | 7 |
| `ayokspamlagi@yandex.com, im.comback@astaga.com` | 6 |


{% capture notice-0 %}
Top 5 most commonly discovered kit owner emails detected over the past week. These emails will receive victim information from the associated phishing kits they own.
{% endcapture %}

<div class="notice--info">
  {{ notice-0 | markdownify }}
</div>

## 📞 Top 5 IP's

|IP Address|Count|Trend|
|---|---:|:---:|
| `162.241.200.38` | 16 | 🆕 |
| `162.241.149.186` | 15 | ⏹ |
| `162.241.114.71` | 14 | 🆕 |
| `162.241.115.246` | 13 | 🔽 |
| `162.214.51.140` | 11 | 🆕 |


{% capture notice-ip %}
Top IP's for the week which have had the most detections. Recurring IP's should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🌐 Top 5 Domains

|Domain|Count|Trend|
|---|---:|:---:|
|`serveirc.com`|26|⏹|
|`servehttp.com`|19|🆕|
|`ddnsking.com`|10|🆕|
|`gleeze.com`|10|⏹|
|`myddns.me`|8|🆕|


{% capture notice-ip %}
Top domains for the week where commercial phishing kits have been detected. These domains should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🔢 Top 5 Kit hashes

|SHA1 Hash|Count|Trend|
|---|---:|:---:|
| `b299405b891b50e2549def0c4f5d15424f5ddd2b` | 10 |🔼|
| `d78905db1dbc48617a96da4e6c9770d04d313a3d` | 8 |🔼|
| `e4f4cea3c5c2d6794f9179133b8364966dc82762` | 8 |🔽|
| `dce23d26075d930bc2003fce20b5ac03a58685e6` | 6 |🔽|
| `187190b296a882fbfa9c376c8071fe519e0106f6` | 4 |🆕|


{% capture notice-hash %}
Top hashes of known malicious kits downloaded by PhishingReel. These hashes can be used to pivot for extra data on sites such as VirusTotal, Any.Run and many others.
{% endcapture %}

<div class="notice--info">
  {{ notice-hash | markdownify }}
</div>

{% capture notice-3 %}
The above information is a summary of the total available data collected.  
For further information such analysis on ASN's, registrars and targeted geolcation/victim information please contact me via [Twitter](https://twitter.com/sysgoblin) or [Keybase](https://keybase.com/sysg0blin).

If you notice any issues or incorrect information in these reports, please contact me using the above information.
{% endcapture %}

<div class="notice">
  {{ notice-3 | markdownify }}
</div>