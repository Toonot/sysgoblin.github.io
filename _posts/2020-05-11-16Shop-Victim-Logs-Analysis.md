---
title: "16Shop Victim Analysis"
categories:
  - Kit Analysis
tags:
  - Research
  - Phishing Kits
classes: wide
header: 
  teaser: "/assets/images/16shop-victim-analysis-teaser.png"
---

<style>
table {
    display:table;
    width:80%;
    margin-left:auto; 
    margin-right:auto;
}
</style>

As you may have seen from my [weekly reports](https://sysgoblin.github.io/categories/#phishingreel-reports), the most popular commercial phishing kit being detected by [PhishingReel](https://twitter.com/phishingreel) at the moment is **16Shop**.  Making up nearly 40% of all detections, I thought it may be interesting to do some analysis on the victim log data I have collected from over the past week.

If you are not familiar with 16Shop or what it is, I recommend you have a read through this thread by [@JCyberSec_](https://twitter.com/jcybersec_) which gives a great overview of what it is and its history. 👇

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">:: 16Shop Intelligence Thread ::<a href="https://twitter.com/hashtag/16Shop?src=hash&amp;ref_src=twsrc%5Etfw">#16Shop</a> is a prolific and one of the first <a href="https://twitter.com/hashtag/Phishing?src=hash&amp;ref_src=twsrc%5Etfw">#Phishing</a>-as-a-Service (PaaS) offerings. <br><br>⚠️This is an intelligence thread on notable elements of the kit, the operation, how to test and detect the scam.<a href="https://twitter.com/hashtag/THREAD?src=hash&amp;ref_src=twsrc%5Etfw">#THREAD</a> <a href="https://t.co/mTFeByFx5a">pic.twitter.com/mTFeByFx5a</a></p>&mdash; Jake (@JCyberSec_) <a href="https://twitter.com/JCyberSec_/status/1255902497782317056?ref_src=twsrc%5Etfw">April 30, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

I've made this analysis from a sample of the total data set, consisting of victim information from just over 100 unique deployments from the past week. The data scraped consists of IP/geo/device information for those which have visited the phishing site, entered credentials or even supplied bank and credit card information.

I have parsed this data and will be focusing on analysing where the victim has entered credentials to the phishing page. Now bear in mind not all of these may be genuine, some may have decided to instead leave a "message" to the owner of the phishing page- however, there is no way to determine this, so numbers are presented as is. 👨‍💻

After cleansing the data and removing duplicates, I produced some basic statistics.

| | |
|---|:---|
| Unique domains | 105 |
| Countries | 135 | 
| IP addresses | 13 |
| ISP's | 147 |
| IP's | 13735 |
| **Total victims logged** | **13936** |

&nbsp;  
&nbsp;  

# Victim geolocation

From an initial eyeball of the victim data it was apparent that the US was the most targeted country out of these deployments, making up almost **60%** of all victims. I took the victim data and extrapolated the below graph of the top 10 countries by victim count.  

_Click details for a table of all countries._

![victims by country](/assets/images/16shop-victim-analysis-country_graph.png){: .center-image }

{% capture table_1 %}
|Name| Count|
|---|---|
|United States|8499|
|Australia|1502|
|Japan|656|
|United Kingdom|378|
|Canada|342|
|Spain|259|
|Germany|243|
|Mexico|187|
|Brazil|155|
|Italy|146|
|Belgium|127|
|Netherlands|110|
|Sweden|89|
|France|72|
|Portugal|69|
|Colombia|66|
|Ireland|61|
|Puerto Rico|57|
|Indonesia|48|
|Norway|40|
|Switzerland|37|
|Argentina|36|
|Philippines|33|
|Peru|30|
|India|29|
|Greece|28|
|Venezuela|27|
|Saudi Arabia|26|
|Thailand|25|
|Denmark|23|
|Singapore|22|
|Chile|21|
|Austria|21|
|Dominican Republic|21|
|Ecuador|20|
|New Zealand|19|
|Turkey|18|
|Finland|17|
|Cyprus|14|
|Malaysia|14|
|Costa Rica|13|
|Romania|13|
|United Arab Emirates|13|
|Malta|11|
|El Salvador|11|
|Uruguay|10|
|Egypt|9|
|Hong Kong|9|
|Israel|9|
|Bahamas|9|
|Nigeria|9|
|South Africa|8|
|South Korea|8|
|Luxembourg|8|
|Guatemala|8|
|Trinidad and Tobago|7|
|Qatar|7|
|Kuwait|6|
|Taiwan|6|
|Estonia|6|
|Bosnia and Herzegovina|6|
|Serbia|5|
|Albania|5|
|U.S. Virgin Islands|5|
|Morocco|5|
|Panama|5|
|Vietnam|5|
|Bolivia|5|
|Croatia|5|
|Curaçao|4|
|Hungary|4|
|China|4|
|Angola|4|
|North Macedonia|4|
|Paraguay|3|
|Belize|3|
|Slovenia|3|
|Slovakia|3|
|Saint Vincent and the Grenadines|3|
|Honduras|3|
|Russia|3|
|Sri Lanka|3|
|Guam|3|
|French Guiana|2|
|Algeria|2|
|Suriname|2|
|Bahrain|2|
|Ukraine|2|
|Jamaica|2|
|Senegal|2|
|Pakistan|2|
|Oman|2|
|Kenya|2|
|Lebanon|2|
|Cameroon|2|
|Cayman Islands|2|
|Georgia|2|
|Czechia|2|
|Iraq|2|
|Tanzania|1|
|Turks and Caicos Islands|1|
|Syria|1|
|Seychelles|1|
|Jersey|1|
|Poland|1|
|Andorra|1|
|Anguilla|1|
|Antigua and Barbuda|1|
|Aruba|1|
|Azerbaijan|1|
|Bangladesh|1|
|Barbados|1|
|Bonaire, Sint Eustatius, and Saba|1|
|Brunei|1|
|Ghana|1|
|Gibraltar|1|
|Guernsey|1|
|Guyana|1|
|Hashemite Kingdom of Jordan|1|
|Iceland|1|
|Iran|1|
|Isle of Man|1|
|Latvia|1|
|Liberia|1|
|Martinique|1|
|Mauritius|1|
|Montenegro|1|
|Nepal|1|
|New Caledonia|1|
|Nicaragua|1|
|Northern Mariana Islands|1|
|Palau|1|
|Saint Lucia|1|
|Zimbabwe|1|
{% endcapture %}

<details> 
  {{ table_1 | markdownify }}
</details>

&nbsp;  
&nbsp;  

# US victim analysis

Out of the US victims it was also clear a vast majority of them were accessing these phishing pages via mobile devices. 📲  
This is not entirely surprising, as use of mobile devices to browse the web continues to increase. It is also generally being harder for mobile users to discern legitimate and malicious websites within a mobile browser- especially when these kits are responsive/"mobile friendly".

![device pie chart](/assets/images/16shop-victim-analysis-device_pie_chart.png){: .center-image }

A top 10 of the ISP information shows these are primarily from consumer home and mobile internet providers.

| ISP | Count |
|---|:---|
|Comcast Cable Communications, LLC|1412|
|Charter Communications|1379|
|Verizon Wireless|817|
|AT&T Corp.|762|
|T-Mobile USA, Inc.|600|
|AT&T Mobility LLC|583|
|Verizon Business|435|
|Sprint Communications, Inc.|315|
|Cox Communications Inc.|290|
|CenturyLink Communications, LLC|252|

From looking at the less common ISP and IP information, it's also possible to identify some potential victims from particular locations or businesses. Some of these included individuals located at:
- **Decatur Manor Healthcare**, a care facility for the chronically or mentally ill.
- **University of Texas Medical Branch**
- **University of Arkansas for Medical Sciences**
- **Acucraft Fireplaces**, a luxury fireplace maker based in Minnesota
- **Bickerstaff Parham LLC**, a real estate firm
- **Cornell University**

The victim logs contained data on those which had supplied bank details, however, these are not able to be correlated with login activity. From the data collected it was evident that bank details had been provided 3389 times with (unsurprisingly) the majority of these details originating from the US.

_Click details for full results._

![bins by country](/assets/images/16shop-victim-analysis-bins_by_country.png){: .center-image }

{% capture table_2 %}
Country| Count
|---|:---|
|United States|2277|
|Japan|176|
|United Kingdom|121|
|Australia|112|
|Spain|80|
|Mexico|57|
|Italy|56|
|Canada|48|
|Brazil|37|
|Germany|32|
|Sweden|30|
|Colombia|19|
|Norway|19|
|Portugal|17|
|Puerto Rico|15|
|Belgium|15|
|Philippines|14|
|France|14|
|Ireland|13|
|Argentina|11|
|Indonesia|10|
|Denmark|9|
|Saudi Arabia|8|
|Netherlands|7|
|Switzerland|7|
|Greece|7|
|El Salvador|7|
|Venezuela|7|
|Chile|7|
|Finland|6|
|Singapore|6|
|Ecuador|5|
|Dominican Republic|5|
|Trinidad and Tobago|5|
|Israel|5|
|Cyprus|5|
|Serbia|5|
|Romania|5|
|Uruguay|4|
|Bahamas|4|
|New Zealand|4|
|Nigeria|4|
|Saint Vincent and the Grenadines|3|
|Peru|3|
|Malta|3|
|South Korea|3|
|United Arab Emirates|3|
|Egypt|3|
|Kuwait|3|
||3|
|Costa Rica|3|
|Croatia|3|
|Estonia|3|
|Curaçao|3|
|India|3|
|Guatemala|2|
|Senegal|2|
|Czechia|2|
|Sri Lanka|2|
|Hong Kong|2|
|Angola|2|
|Taiwan|2|
|Bolivia|2|
|Thailand|2|
|Guam|2|
|Paraguay|2|
|Turkey|2|
|U.S. Virgin Islands|2|
|North Macedonia|2|
|Malaysia|2|
|Luxembourg|2|
|Antigua and Barbuda|1|
|Algeria|1|
|Austria|1|
|Albania|1|
|South Africa|1|
|Georgia|1|
|Honduras|1|
|Seychelles|1|
|Guernsey|1|
|Kenya|1|
|Saint Lucia|1|
|Russia|1|
|Qatar|1|
|Bahrain|1|
|Bonaire, Sint Eustatius, and Saba|1|
|Hungary|1|
|Cameroon|1|
|Iceland|1|
|Cayman Islands|1|
|Nepal|1|
|Jamaica|1|
|Slovenia|1|
|Northern Mariana Islands|1|
{% endcapture %}

<details> 
  {{ table_2 | markdownify }}
</details>
&nbsp;  
It was also possible to produce a top 10 of banks whose customers had fell victim to these phishing sites.

![bins by bank](/assets/images/16shop-victim-analysis-bins_by_bank.png){: .center-image }
 
&nbsp;  
&nbsp;  

# Trends within the data

During analysis it became clear there were certain similarities between the victim logs.

My focus had been on analysing victim data where the user had entered sensitive information. However, all clicks/visits to the sites are also logged, regardless of if the user has entered information at any point.  
A common thread between a large portion of these deployments were the first few visits.

From looking at the first visitor from each deployment, almost **40%** came from Indonesian IP addresses before then logging US victims or victims based in other geolocations.  
This would indicate a portion of the threat actors "test" their deployment when it's live, before sending out phishing/smishing to their intended victims. It also evidences that the larger customer base for 16Shop is based in Indonesia.

Some of these "visitors" can be tracked across several domains, indicating the same threat actor was behind it's creation.

| Domain                                                                           | IP Address      | Browser          | OS         | ISP |
| ---                                                                              | ---             | ---              | ---        | --- |
| `amazon.accountalert01.com`                                                        | 110.136.88.251  | Chrome           | Windows 10 | PT Telkom Indonesia |
| `amazon.notificationalertappsdys908239d.tecxies.com`                               | 110.136.88.251  | Firefox          | Windows 10 | PT Telkom Indonesia |
| `asd-paypal124-help1.ga`                                                           | 110.137.112.18  | Firefox          | Windows 10 | PT Telkom Indonesia |
| `manage-account.paypalinsc.com`                                                    | 110.137.220.119 | Chrome           | Windows 10 | PT Telkom Indonesia |
| `websecure-mailupdate-account.verification.kloutscormnvr.com`                      | 110.138.150.92  | Chrome           | Windows 10 | PT Telkom Indonesia |
| `websecure.account-verification.myloveyouflo.com`                                  | 110.138.151.198 | Chrome           | Windows 10 |  |
| `update-amazon.com.serv01-updateamazon.com`                                        | 110.138.96.172  | Chrome           | Windows 10 | PT Telkom Indonesia |
| `sign-ins-aces2try-phaypal1.com`                                                   | 112.78.180.121  | Chrome           | Windows 10 | Biznet ISP |
| `amzaon.com.verificationcentrehomesupport.hyeoapld.com`                            | 114.122.70.144  | Chrome           | Windows 10 | PT. Telekomunikasi Selular Indonesia |
| `limited.paypalservice.customer-support.it.heasads.com`                            | 114.124.139.210 | Chrome           | Windows 10 | PT. Telekomunikasi Selular Indonesia |
| `cslivesupport.manage-appservice.com`                                              | 114.124.165.246 | Firefox          | Windows 10 | PT. Telekomunikasi Selular Indonesia |
| `security-verification.fashionablemidnight.com`                                    | 114.125.12.110  | Chrome           | Windows 10 | PT. Telekomunikasi Selular Indonesia |
| `signin-webverifyacc-vg9eapple.serveusers.com`                                     | 125.161.107.254 | Chrome           | Windows 7  | PT Telkom Indonesia |
| `cgs-informationupdate.apps.com.snezenieea.com`                                    | 125.161.137.118 | Handheld Browser | Android    | PT Telkom Indonesia |
| `secure01-amazon.serveirc.com`                                                     | 125.167.50.218  | Chrome           | Windows 10 | PT Telkom Indonesia |
| `cg-summary.verivicacionlockedappservice.com`                                      | 140.213.15.132  | Handheld Browser | iPhone     | PT XL Axiata |
| `notice-applestoremanagers.gheafem.com`                                            | 180.241.152.234 | Chrome           | Windows 10 | PT Telkom Indonesia |
| `manage-scure-login.acc-brsae.com`                                                 | 180.241.161.183 | Chrome           | Windows 10 | PT Telkom Indonesia |
| `appleid.apple.com-noreply-informations.186341735184331.org`                       | 180.241.45.178  | Chrome           | Windows 10 | PT Telkom Indonesia |
| `signin.secure.account.support.center.tld100.tstrr11.com`                          | 180.242.235.36  | Chrome           | Windows 10 | PT Telkom Indonesia |
| `manageaccount-appleid.com.stokestrategy.com`                                      | 180.247.45.136  | Chrome           | Windows 10 | PT Telkom Indonesia |
| `service.verification-accountid.appsidga.com`                                      | 180.248.123.152 | Handheld Browser | iPhone     | PT Telkom Indonesia |
| `service-account.usmislead.com`                                                    | 180.251.2.158   | Chrome           | Windows 10 | PT Telekomunikasi Indonesia |
| `amazon-secured-signed-in-uknown-access-from-unauthorise-device.avshgbupdsko.com`  | 180.251.58.144  | Chrome           | Windows 10 | PT Telkom Indonesia |
| `service.account.costumecharge.business`                                           | 182.1.13.46     | Chrome           | Windows 10 | PT. Telekomunikasi Selular Indonesia |
| `service.account.dedicatejurisdiction.com`                                         | 182.1.13.46     | Chrome           | Windows 10 | PT. Telekomunikasi Selular Indonesia |
| `service.account.ealogoeitai.com`                                                  | 182.1.15.157    | Chrome           | Windows 10 | PT. Telekomunikasi Selular Indonesia |
| `security-verification.flexiblewire.info`                                          | 182.1.16.90     | Chrome           | Windows 10 | PT. Telekomunikasi Selular Indonesia |
| `amazon.verificationalertnotificationappshomeen.yupxis.com`                        | 182.1.75.30     | Chrome           | Windows 10 | PT. Telekomunikasi Selular Indonesia |
| `en.amazon.verificationalertaccountaiueugdhaasddxs.fafanms.com`                    | 182.1.75.30     | Chrome           | Windows 10 | PT. Telekomunikasi Selular Indonesia |
| `en.secureaccountlimited-paypal.com`                                               | 182.253.219.4   | Firefox          | Windows 10 | Biznet ISP |
| `manageamazonaccountservicemmzjftsass.vkjnkwd.com`                                 | 36.68.23.62     | Chrome           | Windows 10 | PT Telkom Indonesia |
| `livesupportcsdatacenter.mertgthea.com`                                            | 36.68.4.104     | Firefox          | Windows 10 | PT Telkom Indonesia |
| `manage.unlock-services.accounts.myappleid.pellocks.com`                           | 36.69.4.51      | Firefox          | Windows 10 | PT Telekomunikasi Indonesia |
| `amazon.com-webserviceincresolvedetaild.amdsupportcustomers.com`                   | 36.75.238.40    | Firefox          | Windows 10 | PT Telekomunikasi Indonesia |
| `app.sign.in.amazon.jp.langh-jp.j4r.p.wafoainc.com`                                | 36.76.167.184   | Chrome           | Windows 10 | PT Telkom Indonesia |
| `sign-account-paypal-configure.coreymniez.com`                                     | 36.84.227.169   | Chrome           | Windows 10 | PT Telkom Indonesia |
| `amazon-reportdaily-service.theworkpc.com`                                         | 36.85.217.57    | Firefox          | Windows 10 | PT Telkom Indonesia |
| `secureserver-amazonredirectwebview.kozow.com`                                     | 36.85.218.204   | Firefox          | Windows 10 | PT Telkom Indonesia |
| `amazon.com-limitedcenter.webserviceidrecoverycentersupporte.com`                  | 36.85.219.37    | Firefox          | Windows 10 | PT Telkom Indonesia |
| `mail-helpdeskupdateaccountserv8091.upgandegan.com`                                | 36.88.126.200   | Chrome           | Windows 10 | PT Telkom Indonesia |
| `intl-costumer.limited.6y123-sys.info`                                             | 36.90.159.35    | Chrome           | Windows 10 | PT Telkom Indonesia |
| `user.auth-recover.limited-account.online.pply.534-tyr.net`                        | 36.90.159.35    | Chrome           | Windows 10 | PT Telkom Indonesia |
| `user.limited-account.reactivate.97ter.com`                                        | 36.90.159.35    | Chrome           | Windows 10 | PT Telkom Indonesia |
| `support.mailapp.secuirity-verifikey.ascavc.com`                                   | 36.90.76.191    | Handheld Browser | iPhone     | PT Telkom Indonesia |
| `safeandmanage.accinfo-formlimitation2020.tembelekgarings.com`                     | 36.90.88.240    | Chrome           | Windows 10 | PT Telkom Indonesia |

&nbsp;  

In total there were 38246 visits recorded with 29551 of those being unique. With the total victim count, this shows these 16Shop kits have had an average **47% success rate**. 😰

&nbsp;  
&nbsp;  
# Summary of findings
> 60% of all victims are US based

> The vast majority of victims were using mobile devices

> 40% of deployments appear to originate from Indonesia

> Deployments have an average 47% click to phish ratio

These results go to show that commercial kits like 16Shop are highly targeted, effective and simple to use. This effectively lowers the bar for potential fraudsters wanting to make a quick buck. 

The information and IOC's within PhishingReel's weekly reports and daily posts should help you keep up to date with the latest developments and trends within the world of SaaS phishing kits, and hopefully reduce the risk of you or someone you know falling victim to these.

---

{% capture notice-3 %}
The above information is a summary of the total available data collected.  
For further information please contact me via [Twitter](https://twitter.com/sysgoblin) or [Keybase](https://keybase.com/sysg0blin).

If this has been of use or interest to you, please consider helping me out and [keeping me caffeinated!](https://ko-fi.com/sysgoblin) ☕
{% endcapture %}

<div class="warn">
  {{ notice-3 | markdownify }}
</div>