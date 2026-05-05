---
title: "Critical security update announced for NetScaler Gateway and NetScaler"
url: "https://www.netscaler.com/blog/news/critical-security-update-announced-for-netscaler-gateway-and-netscaler/"
date: "Tue, 26 Aug 2025 14:34:41 +0000"
author: "Anil Shetty"
feed_url: "https://www.netscaler.com/blog/feed/"
---
<p>Cloud Software Group released builds on August 26, 2025, to address three security vulnerabilities. NetScaler Gateway &amp; NetScaler is affected by CVE-2025-7775, which has a CVSS score of 9.2. CVE-2025-7776 impacts NetScaler Gateway (CVSS 8.8), CVE-2025-8424 impacts NetScaler (CVSS 8.7).&nbsp;</p>



<div class="wp-block-spacer" style="height: 32px;"></div>



<p><strong>CVE-2025-7775</strong> is a memory overflow vulnerability the exploit of which can lead to Denial of Service on NetScaler appliances and possibly a Remote Code Execution (RCE) attack. There are several independent pre-conditions for this vulnerability, these are:</p>



<p>​​a) NetScaler must be configured as Gateway (VPN virtual server, ICA Proxy, CVPN, RDP Proxy) OR as a AAA virtual server.</p>



<p>OR</p>



<p>b) NetScaler ADC and NetScaler Gateway 13.1, 14.1, 13.1-FIPS and NDcPP: LB virtual servers of type (HTTP, SSL or HTTP_QUIC) bound with IPv6 services or service groups bound with IPv6 servers</p>



<p>OR</p>



<p>c) NetScaler ADC and NetScaler Gateway 13.1, 14.1, 13.1-FIPS and NDcPP: LB virtual servers of type (HTTP, SSL or HTTP_QUIC) bound with DBS IPv6 services or service groups bound with IPv6 DBS servers</p>



<p>OR</p>



<p>d) NetScaler is configured with a CR (Cache redirection) virtual server with type HDX.</p>



<p>As of August 26, 2025 Cloud Software Group has reason to believe that exploits of CVE-2025-7775 on unmitigated appliances have been observed, and strongly recommends customers to upgrade their NetScaler firmware to the versions containing the fix as there are no mitigations available to protect against a potential exploit.</p>



<p>Additionally, customers can determine if they have an appliance configured as any of the following by inspecting their <strong>ns.conf</strong> file for the specified strings</p>



<p><strong>An Auth Server (AAA Vserver).</strong></p>



<pre class="wp-block-code"><code>add authentication vserver .*</code></pre>



<div class="wp-block-spacer" style="height: 36px;"></div>



<p><strong>A Gateway (VPN Vserver, ICA Proxy, CVPN, RDP Proxy)&nbsp;</strong></p>



<pre class="wp-block-code"><code>add vpn vserver .*</code></pre>



<div class="wp-block-spacer" style="height: 36px;"></div>



<p><strong>LB vserver of Type HTTP_QUIC | SSL | HTTP with IPv6 server bindings :</strong></p>



<pre class="wp-block-code"><code>enable ns feature lb.*
add serviceGroup .* (HTTP_QUIC|SSL|HTTP) .*
add server .* &lt;IPv6&gt;
bind servicegroup &lt;servicegroup name&gt; &lt;IPv6 server&gt; .*
add lb vserver .* (HTTP_QUIC|SSL|HTTP) .*
bind lb vserver .* &lt;ipv6 servicegroup name&gt;</code></pre>



<div class="wp-block-spacer" style="height: 36px;"></div>



<p><strong>LB vserver of Type HTTP_QUIC | SSL | HTTP with DBS IPv6 server&nbsp; :&nbsp;</strong></p>



<pre class="wp-block-code"><code>enable ns feature lb.*
add serviceGroup .* (HTTP_QUIC | SSL | HTTP) .*
add server .* &lt;domain&gt; -queryType AAAA
add service .* &lt;IPv6 DBS server &gt;&nbsp;&nbsp;
bind servicegroup &lt;servicegroup name&gt; &lt;IPv6 DBS server&gt; .*
add lb vserver .* (HTTP_QUIC | SSL | HTTP) .*
bind lb vserver .* &lt;ipv6 servicegroup name&gt;</code></pre>



<div class="wp-block-spacer" style="height: 36px;"></div>



<p><strong>CR vserver with type HDX:&nbsp;</strong></p>



<pre class="wp-block-code"><code>add cr vserver .* HDX .*</code></pre>



<div class="wp-block-spacer" style="height: 53px;"></div>



<p><strong>CVE-2025-7776 </strong>is also a memory overflow vulnerability which can lead to unpredictable/erroneous behavior or a denial of service on NetScaler appliances. This vulnerability only impacts NetScaler if NetScaler is configured as Gateway (VPN virtual server/ICA Proxy/CVPN/RDP Proxy) with a PCoIP Profile bound to them. </p>



<p>Customers can determine if they have an appliance configured by inspecting their ns.conf file for the specified strings.</p>



<p><strong>A Gateway (VPN vserver) with with PCoIP Profile bound to it</strong></p>



<pre class="wp-block-code"><code>add vpn vserver .* -pcoipVserverProfileName .*</code></pre>



<div class="wp-block-spacer" style="height: 53px;"></div>



<p><strong>CVE-2025-8424 </strong>arises due to improper access control on NetScaler Management Interface and can lead to an attacker getting unauthorized access to files they’re not authorized for. However, access to NSIP or Cluster Management IP or local GSLB Site IP or SNIP with management access is required to exploit this vulnerability. In most NetScaler deployments, these IP’s are protected by access control lists (ACL’s) or via an IDAM solution. If access to NetScaler console isn’t gated by IDAM solutions or if local authentication is still being used, CSG strongly recommends customers to consider using IDAM solutions and disabling local authentication. Additionally, NetScaler<a href="https://docs.netscaler.com/en-us/netscaler-adc-secure-deployment/netscaler-secure-deployment-guide.pdf"> secure deployment</a> practices recommend that NSIP not be exposed to the internet.</p>



<div class="wp-block-spacer" style="height: 53px;"></div>



<p>​​The following supported versions of <strong>NetScaler ADC</strong> and <strong>NetScaler Gateway</strong> are affected by the vulnerabilities described above:&nbsp;</p>



<ul class="wp-block-list">
<li>NetScaler ADC and NetScaler Gateway 14.1 BEFORE 14.1-47.48</li>



<li>NetScaler ADC and NetScaler Gateway 13.1 BEFORE 13.1-59.22</li>



<li>NetScaler ADC 13.1-FIPS and NDcPP BEFORE 13.1-37.241-FIPS and NDcPP</li>



<li>NetScaler ADC 12.1-FIPS and NDcPP BEFORE 12.1-55.330-FIPS and NDcPP</li>
</ul>



<p>Cloud Software Group strongly urges affected customers of NetScaler ADC and NetScaler Gateway to install the relevant updated versions as soon as possible.&nbsp;</p>



<ul class="wp-block-list">
<li>NetScaler ADC and NetScaler Gateway 14.1-47.48 and later releases</li>



<li>NetScaler ADC and NetScaler Gateway 13.1-59.22 and later releases of 13.1</li>



<li>NetScaler ADC 13.1-FIPS and 13.1-NDcPP 13.1-37.241 and later releases of 13.1-FIPS and 13.1-NDcPP</li>



<li>NetScaler ADC 12.1-FIPS and 12.1-NDcPP 12.1-55.330 and later releases of 12.1-FIPS and 12.1-NDcPP</li>
</ul>



<h2 class="wp-block-heading">Update installation</h2>



<p><a href="https://www.citrix.com/downloads/citrix-adc/">Download permanent fixes for NetScaler&nbsp;</a></p>



<p>NetScaler and Citrix are both part of Cloud Software Group, and share the same ticketing system. If you encounter issues when you are updating your affected builds, please contact <a href="https://support.citrix.com/support-home/home">Citrix Customer Support</a>, irrespective of whether your product includes NetScaler branding or Citrix branding.&nbsp;</p>



<h2 class="wp-block-heading">Learn more and stay up to date</h2>



<p><a href="https://support.citrix.com/support-home/kbsearch/article?articleNumber=CTX694938">Read the security bulletin for NetScaler and NetScaler Gateway&nbsp;</a></p>



<p><a href="https://support.citrix.com/support-home/home">Sign up for security bulletin notifications</a></p>



<p><a href="https://docs.netscaler.com/en-us/netscaler-adc-secure-deployment.html">See the NetScaler Secure Deployment Guide</a></p>



<p></p>
<p>The post <a href="https://www.netscaler.com/blog/news/critical-security-update-announced-for-netscaler-gateway-and-netscaler/">Critical security update announced for NetScaler Gateway and NetScaler</a> appeared first on <a href="https://www.netscaler.com/blog">NetScaler Blog</a>.</p>
