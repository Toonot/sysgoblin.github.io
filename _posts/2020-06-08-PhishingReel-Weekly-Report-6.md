---
title: "PhishingReel Weekly Report 6"
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

Last week some major changes were introduced within PhishingReel, tripling the amount of domains being analysed. As a result, numbers across the board are a lot higher.  
I have only included data for the new build of PR, as such there are no numbers for 2020-06-01 and I have included some data from this AM.

## 👓 Overview

|                  | Total | Trend |
| ---------------- | ----- | :---: |
| Total detections | 1155  |   🔼   |
| Unique emails    | 279   |   🔼   |
| Unique panels    | 18    |   🔼   |
| Unique IP's      | 218   |   🔼   |
| Kits downloaded  | 665   |   🔼   |
| Unique domains   | 646   |   🔼   |


**Note:** Unique domains do not include subdomains.
{: .notice--info}

## 🔎 Top Kit Detections
![top kits graph](/assets/images/pr-weeklyreport/2020-06-08-fig1.png)

{% capture notice-1 %}
The top 5 kits were deployed a total of **1064** times over the past week.
{% endcapture %}

<div class="notice--info">
  {{ notice-1 | markdownify }}
</div>

## 📈 Detections Over Time
![detections ot graph](/assets/images/pr-weeklyreport/2020-06-08-fig2.png)

{% capture notice-2 %}
Out of the top 5 kits for the past week the date with the highest detections was **2020-06-03** with **247** for that day.  
{% endcapture %}

<div class="notice--info">
  {{ notice-2 | markdownify }}
</div>

## 📧 Top 5 Emails

| Emails                                        | Count |
| --------------------------------------------- | ----: |
| `Resultbertiga12@yandex.com`                  |    11 |
| `otokombo@yandex.ru`                          |    11 |
| `bosmudagoblok@yandex.com, admin@store.com`   |    10 |
| `spam.ccusan@yandex.com`                      |    10 |
| `depansultan@yandex.com, teguh@ganteng.cokkk` |     9 |


{% capture notice-0 %}
Top 5 most commonly discovered kit owner emails detected over the past week. These emails will receive victim information from the associated phishing kits they own.
{% endcapture %}

<div class="notice--info">
  {{ notice-0 | markdownify }}
</div>

## 📞 Top 5 IP's

| IP Address        | Count | Trend |
| ----------------- | ----: | :---: |
| `192.185.130.91`  |    46 |   🆕   |
| `162.241.115.143` |    25 |   🆕   |
| `162.214.51.139`  |    15 |   🔽   |
| `37.140.192.128`  |    14 |   🆕   |
| `162.214.108.227` |    12 |   🆕   |


{% capture notice-ip %}
Top IP's for the week which have had the most detections. Recurring IP's should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🌐 Top 5 Domains

| Domain         | Count | Trend |
| -------------- | ----: | :---: |
| `gleeze.com`   |    42 |   🔼   |
| `kozow.com`    |    36 |   🔼   |
| `serveirc.com` |    32 |   🔽   |
| `giize.com`    |    26 |   🆕   |
| `ooguy.com`    |    15 |   🆕   |


{% capture notice-ip %}
Top domains for the week where commercial phishing kits have been detected. These domains should be blocked where possible.
{% endcapture %}

<div class="notice--info">
  {{ notice-ip | markdownify }}
</div>

## 🔢 Top 5 Kit hashes

| SHA1 Hash                                  | Count | Trend |
| ------------------------------------------ | ----: | :---: |
| `4f514599543e419353e48e37d6a7ce38a6f22110` |    19 |   🔼   |
| `1e2b5cbe646da8a3d228f4d5c5d9dfa0137192e1` |    12 |   🔽   |
| `09bb0127e1951f268c5dc7114bde98d70e0ba592` |    10 |   🆕   |
| `75fb28c53f8485ce11b6f0245c89c2d7dbfe6607` |     9 |   🆕   |
| `3a490a0932c5c9cc8ed8f81ef8b3fa2a3144dba0` |     9 |   🆕   |

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