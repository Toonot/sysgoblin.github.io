---
title: "PhishingReel Weekly Report 7"
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
| Total detections | 1303  |   🔼   |
| Unique emails    | 321   |   🔼   |
| Unique panels    | 13    |   🔽   |
| Unique IP's      | 244   |   🔼   |
| Kits downloaded  | 453   |   🔽   |
| Unique domains   | 775   |   🔼   |


**Note:** Unique domains do not include subdomains.
{: .notice--info}

## 🔎 Top Kit Detections
![top kits graph](/assets/images/pr-weeklyreport/2020-06-15-fig1.png)

{% capture notice-1 %}
The top 5 kits were deployed a total of **1411** times over the past week.
{% endcapture %}

<div class="notice--info">
  {{ notice-1 | markdownify }}
</div>

## 📈 Detections Over Time
![detections ot graph](/assets/images/pr-weeklyreport/2020-06-15-fig2.png)

{% capture notice-2 %}
Out of the top 5 kits for the past week the date with the highest detections was **2020-06-09** with **251** for that day.  
{% endcapture %}

<div class="notice--info">
  {{ notice-2 | markdownify }}
</div>

## 📧 Top 5 Emails

| Emails                                       | Count |
| -------------------------------------------- | ----: |
| `demibuahati@yandex.ru, teguh@ganteng.cokkk` |    13 |
| `yoi31834@gmail.com, ys@youngsister.com`     |    12 |
| `spamlah@yandex.com`                         |    10 |
| `rezult.pucku@gmail.com, admin@16shop.us`    |    10 |
| `rezulthere@yandex.com`                      |    10 |


{% capture notice-0 %}
Top 5 most commonly discovered kit owner emails detected over the past week. These emails will receive victim information from the associated phishing kits they own.
{% endcapture %}

<div class="notice--info">
  {{ notice-0 | markdownify }}
</div>

## 📞 Top 5 IP's

| IP Address        | Count | Trend |
| ----------------- | ----: | :---: |
| `192.185.130.91`  |    55 |   ⏹   |
| `129.226.156.16`  |    30 |   🆕   |
| `192.3.182.218`   |    23 |   🆕   |
| `27.102.128.25`   |    23 |   🆕   |
| `104.140.246.142` |    22 |   🆕   |


{% capture notice-ip %}
Top IP's for the week which have had the most detections. Recurring IP's should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🌐 Top 5 Domains

| Domain         | Count | Trend |
| -------------- | ----: | :---: |
| `gleeze.com`   |    72 |   ⏹   |
| `giize.com`    |    54 |   🔼   |
| `serveirc.com` |    45 |   ⏹   |
| `duckdns.org`  |    26 |   🆕   |
| `kozow.com`    |    25 |   🔽   |


{% capture notice-ip %}
Top domains for the week where commercial phishing kits have been detected. These domains should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🔢 Top 5 Kit hashes

| SHA1 Hash                                  | Count | Trend |
| ------------------------------------------ | ----: | :---: |
| `b299405b891b50e2549def0c4f5d15424f5ddd2b` |    16 |   🆕   |
| `4f514599543e419353e48e37d6a7ce38a6f22110` |    13 |   🔽   |
| `09bb0127e1951f268c5dc7114bde98d70e0ba592` |     7 |   ⏹   |
| `6a90d3458486530752ff0147adf0d5619b55ce5c` |     6 |   🆕   |
| `99e5bdcfdc69ee6a2638a9f3496ec039f74f20fa` |     6 |   🆕   |


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