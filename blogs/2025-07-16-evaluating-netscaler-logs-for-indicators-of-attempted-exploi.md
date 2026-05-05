---
title: "Evaluating NetScaler logs for indicators of attempted exploitation of CVE-2025-5777"
url: "https://www.netscaler.com/blog/news/evaluating-netscaler-logs-for-indicators-of-attempted-exploitation-of-cve-2025-5777/"
date: "Wed, 16 Jul 2025 00:34:23 +0000"
author: "Anil Shetty"
feed_url: "https://www.netscaler.com/blog/feed/"
---
<p>In our recent update to our <a href="https://www.netscaler.com/blog/news/netscaler-critical-security-updates-for-cve-2025-6543-and-cve-2025-5777/">announcement of CVE 2025-5777</a>, we noted that on July 10, 2025, CISA added CVE-2025-5777 to its Known Exploited Vulnerabilities Catalog. To help customers assess their security posture, we&#8217;ve provided additional guidance below.</p>



<p>In unpatched appliances, if attempts to exploit or scan for CVE-2025-5777 have taken place, then there may be some observable artifacts in NetScaler logs. Note that this analysis assumes that syslog is being externally collected and available for the period that is being analyzed. If logs are being analyzed locally, note that the system logs may only be available for a few days prior, as older logs may have been automatically deleted to conserve disk space on the appliance.</p>



<p><strong>Syslog analysis</strong></p>



<p>Search for log lines containing<code> /\"Authentication is rejected for / AND /AAA Message/</code> AND bytes containing non-ASCII characters (range 128-255). Note these bytes may be escaped when viewed through a log viewer. The strings between the opening and closing ‘/’s can be treated as a regular expression.</p>



<p>If searching locally on MPX or VPX, the following awk command can be used within /var/log:</p>



<p><code>zcat ns.log.*.gz | awk -v FS='Authentication is rejected for ' '{if($1~/AAA Message/&amp;&amp;$2~/[\x80-\xff]/) print}'</code></p>



<p>The presence of non-ASCII characters in these lines can indicate exploit attempts.</p>



<p><strong>Session analysis</strong></p>



<p>Administrators and incident responders can also attempt to manually review client IP addresses from certain types of session events. A change in client IP during one session may indicate session theft, although it can also indicate that a user has connected from multiple locations, like switching from office WiFi to a home network. Session theft is plausible but not guaranteed if CVE-2025-5777 is exploited and the likelihood of this depends on the device configuration and the volume and types of traffic that are being processed by NetScaler.</p>



<p>For example, if analyzing VPN sessions (SSLVPN TCPCONNSTAT event):</p>



<p><code>ns.log.10.gz:Jul 11 10:41:50 &lt;local0.info> 10.0.0.1  07/11/2025:10:41:50 GMT ns 0-PPE-0 : default <strong>SSLVPN TCPCONNSTAT</strong> 1496 0 :  User user1 - <strong>Client_ip 10.2.0.20</strong> - Nat_ip 127.0.0.2 - Vserver 10.1.2.32:443 - <strong>Source 10.2.0.20</strong>:50961 - Destination 127.0.0.1:81 - Start_time "07/11/2025:10:41:50 GMT" - End_time "07/11/2025:10:41:50 GMT" - Duration 00:00:00  - Total_bytes_send 750 - Total_bytes_recv 1200 - Total_compressedbytes_send 0 - Total_compressedbytes_recv 0 - Compression_ratio_send 0.00% - Compression_ratio_recv 0.00% - Access Allowed - Group(s) "N/A"</code></p>



<p>It would be expected that the client_ip and the source IP address are the same, as long as the client has not changed how they are connecting to the internet.</p>



<p>Please note that the steps suggested above can be useful in detecting certain potential exploits but the process will not necessarily successfully detect all possible exploits.</p>
<p>The post <a href="https://www.netscaler.com/blog/news/evaluating-netscaler-logs-for-indicators-of-attempted-exploitation-of-cve-2025-5777/">Evaluating NetScaler logs for indicators of attempted exploitation of CVE-2025-5777</a> appeared first on <a href="https://www.netscaler.com/blog">NetScaler Blog</a>.</p>
