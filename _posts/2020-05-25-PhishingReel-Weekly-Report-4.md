---
title: "PhishingReel Weekly Report 4"
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
| Total detections | 768   |   🔽   |
| Unique emails    | 148   |   🔽   |
| Unique panels    | 11    |   ⏹ |
| Unique IP's      | 211   |   🔽   |
| Kits downloaded  | 148   |   🔽   |
| Unique domains   | 465   |   🔽   |


**Note:** Unique domains do not include subdomains.
{: .notice--info}

## 🔎 Top Kit Detections
![top kits graph](/assets/images/pr-weeklyreport/2020-05-25-fig1.png)

{% capture notice-1 %}
The top 5 kits were deployed a total of **722** times over the past week.
{% endcapture %}

<div class="notice--info">
  {{ notice-1 | markdownify }}
</div>

## 📈 Detections Over Time
![detections ot graph](/assets/images/pr-weeklyreport/2020-05-25-fig2.png)

{% capture notice-2 %}
Out of the top 5 kits for the past week the date with the highest detections was **2020-05-20** with **138** for that day.  
{% endcapture %}

<div class="notice--info">
  {{ notice-2 | markdownify }}
</div>

## 📧 Top 5 Emails

| Emails                                              | Count |
| --------------------------------------------------- | ----: |
| `jalanterus91@yandex.com, ys@youngsister.com`       |    16 |
| `kawanresult@hotmail.com, resultcc@16shop.us`       |    10 |
| `ayokkkemmablii@yandex.com, admindilan@16shop.us`   |    10 |
| `otokombo@yandex.ru`                                |     8 |
| `ggenduy@gmail.com, resultmrsukarelap66@16toko.com` |     8 |


{% capture notice-0 %}
Top 5 most commonly discovered kit owner emails detected over the past week. These emails will receive victim information from the associated phishing kits they own.
{% endcapture %}

<div class="notice--info">
  {{ notice-0 | markdownify }}
</div>

## 📞 Top 5 IP's

| IP Address        | Count | Trend |
| ----------------- | ----: | :---: |
| `162.241.115.246` |    27 |   ⏹   |
| `104.218.52.156`  |    18 |   🆕   |
| `13.82.142.247`   |    14 |   🆕   |
| `34.70.147.98`    |    14 |   🆕   |
| `162.214.54.226`  |    13 |   🆕   |


{% capture notice-ip %}
Top IP's for the week which have had the most detections. Recurring IP's should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🌐 Top 5 Domains

| Domain              | Count | Trend |
| ------------------- | ----: | :---: |
| `ddns.net`          |    28 |   🆕   |
| `giize.com`         |    24 |   ⏹   |
| `serveirc.com`      |    16 |   🔽   |
| `gleeze.com`        |    13 |   🔽   |
| `servehalflife.com` |    12 |   🆕   |


{% capture notice-ip %}
Top domains for the week where commercial phishing kits have been detected. These domains should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🔢 Top 5 Kit hashes

| SHA1 Hash                                  | Count | Trend |
| ------------------------------------------ | ----: | :---: |
| `b5f7e7f62c6e91cbd723eeeb2b07696bcd63d658` |    14 |   🆕   |
| `1e2b5cbe646da8a3d228f4d5c5d9dfa0137192e1` |     9 |   🆕   |
| `4f514599543e419353e48e37d6a7ce38a6f22110` |     9 |   🆕   |
| `cbd82e1dd73d2dbba6bd3264d5b76cd51dea08ab` |     8 |   🆕   |
| `b299405b891b50e2549def0c4f5d15424f5ddd2b` |     7 |   🆕   |


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