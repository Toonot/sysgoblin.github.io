---
title: "PhishingReel Weekly Report 5"
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

|                  | Total | Trend |
| ---------------- | ----- | :---: |
| Total detections | 737   |   🔽   |
| Unique emails    | 131   |   🔽   |
| Unique panels    | 10    |   🔽   |
| Unique IP's      | 194   |   🔽   |
| Kits downloaded  | 131   |   🔽   |
| Unique domains   | 445   |   🔽   |


**Note:** Unique domains do not include subdomains.
{: .notice--info}

## 🔎 Top Kit Detections
![top kits graph](/assets/images/pr-weeklyreport/2020-06-01-fig1.png)

{% capture notice-1 %}
The top 5 kits were deployed a total of **698** times over the past week.
{% endcapture %}

<div class="notice--info">
  {{ notice-1 | markdownify }}
</div>

## 📈 Detections Over Time
![detections ot graph](/assets/images/pr-weeklyreport/2020-06-01-fig2.png)

{% capture notice-2 %}
Out of the top 5 kits for the past week the date with the highest detections was **2020-05-29** with **149** for that day.  
{% endcapture %}

<div class="notice--info">
  {{ notice-2 | markdownify }}
</div>

## 📧 Top 5 Emails

| Emails                                          | Count |
| ----------------------------------------------- | ----: |
| `resultlebaran@hotmail.com, resultcc@16shop.us` |    19 |
| `hubla.hula@yandex.com, admin@16shop.us`        |     7 |
| `resultkontolasw1@gmail.com, admin@16shop.us`   |     7 |
| `slifer.sky@yandex.com`                         |     6 |
| `hugoopeoott@yandex.com, admindilan@16shop.us`  |     6 |


{% capture notice-0 %}
Top 5 most commonly discovered kit owner emails detected over the past week. These emails will receive victim information from the associated phishing kits they own.
{% endcapture %}

<div class="notice--info">
  {{ notice-0 | markdownify }}
</div>

## 📞 Top 5 IP's

| IP Address        | Count | Trend |
| ----------------- | ----: | :---: |
| `35.193.169.140`  |    31 |   🆕   |
| `162.214.51.139`  |    29 |   🆕   |
| `162.241.115.246` |    23 |   🔽   |
| `62.171.168.154`  |    19 |   🆕   |
| `104.218.52.156`  |    16 |   🔽   |


{% capture notice-ip %}
Top IP's for the week which have had the most detections. Recurring IP's should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🌐 Top 5 Domains

| Domain         | Count | Trend |
| -------------- | ----: | :---: |
| `serveirc.com` |    24 |   🔼   |
| `ddnsking.com` |    19 |   🆕   |
| `kozow.com`    |    18 |   🆕   |
| `gleeze.com`   |    13 |   ⏹   |
| `camdvr.org`   |    12 |   🆕   |


{% capture notice-ip %}
Top domains for the week where commercial phishing kits have been detected. These domains should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🔢 Top 5 Kit hashes

| SHA1 Hash                                  | Count | Trend |
| ------------------------------------------ | ----: | :---: |
| `1e2b5cbe646da8a3d228f4d5c5d9dfa0137192e1` |    16 |   🔼   |
| `4f514599543e419353e48e37d6a7ce38a6f22110` |     8 |   🔼   |
| `b299405b891b50e2549def0c4f5d15424f5ddd2b` |     6 |   🔼   |
| `bb478881a1c7ca7a07065f12cb9783c472eb83a0` |     6 |   🆕   |
| `99e5bdcfdc69ee6a2638a9f3496ec039f74f20fa` |     5 |   🆕   |


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