---
title: "Medium severity security update announced for NetScaler Gateway and NetScaler"
url: "https://www.netscaler.com/blog/news/medium-severity-security-update-announced-for-netscaler-gateway-and-netscaler/"
date: "Tue, 11 Nov 2025 14:00:34 +0000"
author: "Anil Shetty"
feed_url: "https://www.netscaler.com/blog/feed/"
---
<p>Cloud Software Group released builds on November 11, 2025, to address one security vulnerability. NetScaler Gateway &amp; NetScaler is affected by CVE 2025-12101, which has a CVSS score of 5.9.&nbsp;&nbsp;</p>



<p><strong>CVE 2025-12101</strong> is a cross-site scripting vulnerability impacting NetScaler Gateway (VPN virtual server, ICA Proxy, CVPN, RDP Proxy, or AAA virtual server). Insufficient validation controls enable a malicious party to inject CRLF control characters into HTTP responses.&nbsp;</p>



<p>NetScaler recommends its customers to follow <a href="https://docs.netscaler.com/en-us/netscaler-adc-secure-deployment/netscaler%C2%AE-secure-deployment-guide.pdf">secure deployment guidelines</a> and feature documentation for <a href="https://docs.netscaler.com/en-us/citrix-adc/current-release/aaa-tm/entities-of-authentication-authorization-auditing/authentication-virtual-server.html">configuring AAA</a>, which advise configuring Auth Vserver only when the AAA feature is enabled. Not configuring AAA feature if an Auth vServer is configured may lead to unintended consequences. &nbsp;&nbsp;</p>



<p>Cloud Software Group thanks Sina Kheirkhah of watchTowr and Dylan Pindur of Assetnote for working with us to protect NetScaler customers.&nbsp;</p>



<p>As of <strong>November 11, 2025,</strong> Cloud Software Group has no reason to believe that this vulnerability has an unmitigated exploit available in NetScaler deployments.&nbsp;</p>



<p>The following supported versions of <strong>NetScaler ADC</strong> and <strong>NetScaler Gateway</strong> are affected by CVE 2025-12101:</p>



<ul class="wp-block-list">
<li>NetScaler ADC and NetScaler Gateway 14.1 BEFORE 14.1-56.73</li>



<li>NetScaler ADC and NetScaler Gateway 13.1 BEFORE 13.1-60.32</li>



<li>NetScaler ADC 13.1-FIPS and NDcPP BEFORE 13.1-37.250-FIPS and 13.1 NDcPP</li>



<li>NetScaler ADC 12.1-FIPS and NDcPP BEFORE 12.1-55.333-FIPS and 13.1 NDcPP</li>
</ul>



<p>Cloud Software Group strongly urges affected customers of NetScaler ADC and NetScaler Gateway to install the following relevant updated versions as soon as possible: &nbsp;</p>



<ul class="wp-block-list">
<li>NetScaler ADC and NetScaler Gateway 14.1-56.73 and later releases</li>



<li>NetScaler ADC and NetScaler Gateway 13.1-60.32 and later releases of 13.1</li>



<li>NetScaler ADC 13.1-FIPS and 13.1-NDcPP 13.1-37.250 and later releases of 13.1-FIPS and 13.1-NDcPP</li>



<li>NetScaler ADC 12.1-FIPS and 12.1-NDcPP 12.1-55.333 and later releases of 12.1-FIPS and 12.1-NDcPP</li>
</ul>



<h2 class="wp-block-heading">Update installation</h2>



<p><a href="https://www.citrix.com/downloads/citrix-adc/">Download permanent fixes for NetScaler</a></p>



<p>NetScaler and Citrix are both part of Cloud Software Group, and share the same ticketing system. If you encounter issues when you are updating your affected builds, please contact <a href="https://support.citrix.com/support-home/home" rel="noreferrer noopener" target="_blank">Citrix Customer Support</a>, irrespective of whether your product includes NetScaler branding or Citrix branding.&nbsp;&nbsp;</p>



<p><strong>Note</strong>: Please note that starting 14.1 51.x, 13.1-60.x, 13.1-37.x (FIPS) for NetScaler ADC builds which includes VPX, MPX and SDX form factors and 14.1 51.x, 13.1-60.x for NetScaler SVM, NetScaler has started to enforce SA (Subscription Advantage) date and BID (Burn-In-Date) which means, if the Burn-In Date of the NetScaler build to which you are trying to upgrade to is later than the SA date in the perpetual license file used on your NetScaler instance, your NetScaler instance <strong>will become unlicensed</strong> after the upgrade. Please refer to the <a href="https://docs.netscaler.com/en-us/citrix-adc/current-release/licensing.html#changes-related-to-perpetual-licensing" rel="noreferrer noopener" target="_blank">documentation</a> for more details. Additionally, this change has also been covered in NetScaler release notes for <a href="https://docs.netscaler.com/en-us/updates?product=NetScaler%2520ADC%2520%28includes%2520NetScaler%2520Gateway%29&amp;version=14.1&amp;build=51.80" rel="noreferrer noopener" target="_blank">14.1</a> and <a href="https://docs.netscaler.com/en-us/updates?product=NetScaler%2520ADC%2520%28includes%2520NetScaler%2520Gateway%29&amp;version=13.1&amp;build=60.29" rel="noreferrer noopener" target="_blank">13.1</a> under CTXENG-68283. </p>



<h2 class="wp-block-heading">Learn more and stay up to date</h2>



<p><a href="https://support.citrix.com/support-home/kbsearch/article?articleNumber=CTX695486">Read the security bulletin for NetScaler and NetScaler Gateway </a></p>



<p><a href="https://support.citrix.com/support-home/home">Sign up for security bulletin notifications </a></p>



<p><a href="https://docs.netscaler.com/en-us/netscaler-adc-secure-deployment.html">See the NetScaler Secure Deployment Guide</a></p>
<p>The post <a href="https://www.netscaler.com/blog/news/medium-severity-security-update-announced-for-netscaler-gateway-and-netscaler/">Medium severity security update announced for NetScaler Gateway and NetScaler</a> appeared first on <a href="https://www.netscaler.com/blog">NetScaler Blog</a>.</p>
