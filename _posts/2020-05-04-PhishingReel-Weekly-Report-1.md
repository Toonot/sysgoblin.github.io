---
title: "PhishingReel Weekly Report 1 2020-05-04"
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

Welcome to the first weekly report from @phishingreel.
After this post subsequent reports will be made weekly on a Monday AM approx 10:00 UTC, and will be fully automated.
{: .notice}

# 👋🤖
[PhishingReel](https://twitter.com/phishingreel) monitors and scans the internet to find these kits being deployed and monitors their activity until the domain is taken down. These reports serve as a weekly update on the current state and trends within the world of SaaS phishing kits.

This report only contains summarised analysis of detections for the week. For further information or access to feeds to enrich your own data, please contact me via [Twitter](https://twitter.com/sysgoblin) or [Keybase](https://keybase.com/sysg0blin).
{: .notice--danger}

## 👓 Overview

| Data Point | Total | Trend |
|---|---|---|
| Total detections | 751 | 🔼 |
| Unique emails | 266 | 🔼 |
| Unique panels | 14 | 🔼 |
| Unique IP's | 236 | 🔼 |
| Kits downloaded | 229 | 🔼 |
| Unique domains | 631 | 🔼 |

**Note:** Unique domains do not include subdomains.
{: .notice--info}

## 🔎 Top Kit Detections
![top kits graph](/assets/images/pr-weeklyreport/2020-05-04-fig1.png)

{% capture notice-1 %}
The top 5 kits were deployed a total of **698** times over the past week.
{% endcapture %}

<div class="notice--info">
  {{ notice-1 | markdownify }}
</div>

## 📈 Detections Over Time
![detections ot graph](/assets/images/pr-weeklyreport/2020-05-04-fig2.png)

{% capture notice-2 %}
Out of the top 5 kits for the past week the date with the highest detections was **2020-05-01** with **192** for that day.  
{% endcapture %}

<div class="notice--info">
  {{ notice-2 | markdownify }}
</div>


## 📧 Top 5 Emails

|Emails|Count|
|---|---:|
| `email@example.com` | 8 |
| `racikkkannn@yandex.com, admindilan@16shop.us` | 8 |
| `resultpilihan@yandex.com, inbox@ccmasuk.com` | 7 |
| `timothy.resultpepeh18@yandex.com, whm@timothytamvan.com` | 6 |
| `rumahbertingkat2@yandex.com, admin@16shop.us` | 5 |

{% capture notice-0 %}
Top 5 most commonly discovered kit owner emails detected over the past week. These emails will receive victim information from the associated phishing kits they own.
{% endcapture %}

<div class="notice--info">
  {{ notice-0 | markdownify }}
</div>

## 📞 Top 5 IP's

|IP Address|Count|Trend|
|---|---:|:---:|
| `162.241.69.85` | 29 | 🆕 |
| `162.241.149.186` | 28 | 🆕 |
| `162.241.115.246` | 17 | 🆕 |
| `162.214.49.191` | 16 | 🆕 |
| `162.241.29.128` | 16 | 🆕 |

{% capture notice-ip %}
Top IP's for the week which have had the most detections. Recurring IP's should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🌐 Top 5 Domains

|Domain|Count|Trend|
|---|---:|:---:|
|`serveirc.com`|24|🆕|
|`dynv6.net`|8|🆕|
|`servehalflife.com`|7|🆕|
|`gleeze.com`|6|🆕|
|`servebeer.com`|6|🆕|

{% capture notice-ip %}
Top domains for the week where commercial phishing kits have been detected. These domains should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🔢 Top 5 Kit hashes

|SHA1 Hash|Count|Trend|
|---|---:|:---:|
|dce23d26075d930bc2003fce20b5ac03a58685e6|21| 🆕 |
|e4f4cea3c5c2d6794f9179133b8364966dc82762|14| 🆕 |
|d78905db1dbc48617a96da4e6c9770d04d313a3d|9| 🆕 |
|b299405b891b50e2549def0c4f5d15424f5ddd2b|9| 🆕 |
|7b89522de61fc1b3e0bc2d1103ee7828fc88ca38|7| 🆕 |

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