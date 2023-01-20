# IPInfo MulesSoft Project
MuleSoft System Integration Demo 2


This project was made by Lesia Pokotulyk and Ivan Kostroba as Softserve Software integration internship MuleSoft demo project.

Functionell:
HTTP-webserver, performs IP lookup using GET requests;
Telegram Bot, performs IP lookup using chatbot commands;
E-Mail Bot, performs IP lookup using commands sent as a message topic.

Serivce receives IP address (or domain name that it converts to IP address using the DNS-webservice) and sends requests on multiple website security APIs, such as AbuseIPDB.
After receiving lookup result, it aggregates them into one JSON (or plain text message, if request sent via Telegram bot) and returns to user.

IP lookup result example (plain text):

IP report:   
IP: 8.8.8.8    
Site owner: GOOGLE    
Usage type: Search Engine Spider   
Found hostnames: dns.google, dns.google.com, *.dns.google.com, 8888.google, dns64.dns.google, 8.8.8.8, 8.8.4.4, 2001:4860:4860:0:0:0:0:8888, 2001:4860:4860:0:0:0:0:8844, 2001:4860:4860:0:0:0:0:6464, 2001:4860:4860:0:0:0:0:64   
Country: US    
Datacenter: /v1/datacenter/GOOGLE   
AbuseIPDB result:    
Total times reported: 8   
Confidence score: 0   
Threatjammer result:   
Risk level: LOW   
Reason phrase: Found in one or more denylist datasets.   
Cloudmersive result:   
Is bot: false   
Is threat: false   
Threat type if any:   
Virustotal result ratings:   
Harmless: 82   
Malicious: 1   
Suspicious: 0   
Undetected: 12   
Timeout: 0   

IP lookup result example (JSON):   

{   
  "IP": "91.202.128.77",   
  "owner": "Kyiv National Taras Shevchenko University",   
  "usage_type": "University/College/School",   
  "found_hostnames": [
    "knu.ua",
    "univ.kiev.ua",
    "www.knu.ua",
    "www.univ.kiev.ua"
  ],   
  "country": "UA",   
  "datacenter": "",   
  "abuseIPDB": {   
    "total_reports": 0,    
    "confidence_score": 0   
  },   
  "threatjammer": {    
    "risk_level": "LOW",   
    "reason_phrase": "No risk found."   
  },   
  "cloudmersive": {   
    "is_bot": false,   
    "is_threat": false,   
    "threat_type": ""   
  },   
  "virustotal": {   
    "ratings": {   
      "harmless": 94,   
      "malicious": 0,   
      "suspicious": 0,   
      "undetected": 0,   
      "timeout": 0   
    }   
  }   
}   
   
