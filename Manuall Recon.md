<h1 align="center">Hi , I'm Sanjay Kumar Das <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="35"></h1>
<p align="center">

<a href="https://github.com/DenverCoder1/readme-typing-svg"><img src="https://readme-typing-svg.herokuapp.com?lines=Cyber+Security+Student;Ethical+Hacker;Defcon+2021+Finalist;DS%20|%20Algorithms%20|%20OOP%20;Specialist%20on%20Codeforces;Division%202%20on%20Codechef%20(3%20Stars);6%20Kyu%20on%20Atcoder;Always%20learning%20new%20things&center=true&width=600&height=70"></a>
</p>


https://github.com/vavkamil/awesome-bugbounty-tools#Subdomain-Enumeration
https://www.cobalt.io/blog/scope-based-recon-smart-recon-tactics


## 🔥Subdomain Enumeration

assetfinder --subs-only  <domain>

httprobe (subdomain alive or dead)
Take a list of domains and probe for working http and https servers.

cat recon/example/domains.txt | httprobe
cat domains.txt | httprobe --prefer-https

### 👉 GitDorker
A Python program to scrape secrets from GitHub through usage of a large repository of dorks.

python3 GitDorker.py -tf TOKENSFILE -q tesla.com -d Dorks/DORKFILE -o tesla

EyeWitness

./EyeWitness -f urls.txt --web

./EyeWitness -x urls.xml --timeout 8 

./EyeWitness.py -f urls.txt --web --proxy-ip 127.0.0.1 --proxy-port 8080 --proxy-type socks5 --timeout 120

### 👉Content Discovery 


gobuster dir -u https   -w /wordlists/shortlist.txt

## 🔥 gau
About
Fetch known URLs from AlienVault's Open Threat Exchange, the Wayback Machine, and Common Crawl.

 printf example.com | gau
$ cat domains.txt | gau --threads 5
$ gau example.com google.com
$ gau --o example-urls.txt example.com
$ gau --blacklist png,jpg,gif example.com

### 👉 GetJS

About
A tool to fastly get all javascript sources/files

To save the results to a file, and don't display anything, use:

-  getJS --url https://poc-server.com --output results.txt
If you would like the output to be in JSON format, you can combine it with @Tomnomnom's toJSON:

$ getJS --url https://poc-server.com | tojson

### 👉 Arjun (parameter finder)
HTTP parameter discovery suite.

arjun -i targets.txt
 arjun  -u https://api.example.com/endpoint -oJ result.json

## 🔥Fuzzing

fuf - Fuzz Faster U Fool
- wordlist:
fuzzdb
seclists

wfuzz -w wordlist/general/common.txt --hc 404 http://testphp.vulnweb.com/FUZZ

wfuzz -w wordlist/general/common.txt http://testphp.vulnweb.com/FUZZ.php

wfuzz -z file,wordlist/others/common_pass.txt -d "uname=FUZZ&pass=FUZZ"  --hc 302 http://testphp.vulnweb.com/userinfo.php

wfuzz -z file,wordlist/general/common.txt -b cookie=value1 -b cookie2=value2 http://testphp.vulnweb.com/FUZZ

wfuzz -z list,nonvalid-httpwatch --basic FUZZ:FUZZ https://www.httpwatch.com/httpgallery/authentication/authenticatedimage/default.aspx
 
fuzz -z file,wordlist/general/common.txt -H "User-Agent: FUZZ" http://testphp.vulnweb.com/

## 🔥 ffuf - Fuzz
 - Faster U Fool
 
Fast web fuzzer written in Go

ffuf -w /path/to/wordlist -u https://target/FUZZ

ffuf -w /path/to/values.txt -u https://target/script.php?valid_name=FUZZ -fc 401 (filter response code 401)
 
ffuf -w /path/to/postdata.txt -X POST -d "username=admin\&password=FUZZ" -u https://target/login.php

<summary><b>⚡ Gf-Patterns V 1.9  XSS, SSRF, SQLi,  <</b></summary>


GF Paterns For (ssrf,RCE,Lfi,sqli,ssti,idor,url redirection,debug_logic, interesting Subs) parameters grep
 cat subdomains.txt | waybackurls | sort -u >> waybackdata | gf ssrf | tee -a ssfrparams.txt

▶ cat waybackdata | gf redirect | tee -a redirect.txt
 cat ~/.gf/ssrf.json
 cat ~/.gf/lfi.json
  cat ~/.gf/sqli.jsoncat 
  ~/.gf/idor.json 
  cat ~/.gf/rce.json
  
  
 ### 👉 ReconNote
  
  
=========================================================================================================================

### 👉 Template Based Scanning

Nuclei 
About
Fast and customizable vulnerability scanner based on simple YAML based DSL.

nuclei -list urls.txt

nuclei -u https://example.com -tags cve

nuclei -u https://example.com -tags cve -severity critical,high -author geeknik

nuclei -list http_urls.txt -w workflows/wordpress-workflow.yaml


# 👉 shodan:

country:US or org:"Harvard University" or hostname:"nasa.gov" 

"authentication disabled" "RFB 003.008"

Already Logged-In as root via Telnet 🔎 →
"root@" port:23 -login -password -name -Session
