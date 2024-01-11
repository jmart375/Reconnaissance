![download](https://github.com/jmart375/Reconnaissance/assets/91294710/cd971882-73e3-47ce-a270-b928da4a1873)
# Penetration Test - Reconnaissance

## Table of Contents
1. [Deliverables 1.3](#deliverables-13)
2. [Reconnaissance Deliverables 2.2](#reconnaissance-deliverables-22)
   2.1 [Deliverable 2.1.2 DNS](#deliverable-212-dns)
   2.2 [Deliverable 2.1.3 The Whois Database](#deliverable-213-the-whois-database)
   2.3 [Deliverable 2.1.4 The ARIN Database](#deliverable-214-the-arin-database)
   2.4 [Deliverable 2.1.5 SSL Certificates](#deliverable-215-ssl-certificates)
   2.5 [Other Info Discovered](#other-info-discovered)
   2.6 [Deliverable 2.1.6 Shodan](#deliverable-216-shodan)
   2.7 [Deliverable 2.1.7 Fierce Domain Name Scanner](#deliverable-217-fierce-domain-name-scanner)
3. [What would you suggest doing next?](#what-would-you-suggest-doing-next)
4. [What hosts at what IP addresses/ports should be scanned for vulnerabilities?](#what-hosts-at-what-ip-addressesports-should-be-scanned-for-vulnerabilities)
5. [What other ideas about how you could proceed if this were a real pen test?](#what-other-ideas-about-how-you-could-proceed-if-this-were-a-real-pen-test)

## Deliverables 1.3

- Kali VM running, logged in, and at the desktop ready for use.
![image](https://github.com/jmart375/Reconnaissance/assets/91294710/b7981c4b-5bfc-43e3-9b80-eae2f8da64d0)

- Metasploitable2 VM running and at the command prompt ready for use.
![image](https://github.com/jmart375/Reconnaissance/assets/91294710/ab88ee6f-3f8a-4145-98e3-95bb0efac1aa)

- Windows task manager shows system resource utilization with both VMs and your host OS running concurrently. Make sure that memory (RAM) usage is shown.
![image](https://github.com/jmart375/Reconnaissance/assets/91294710/b0e8d8cf-8b70-4de6-86ea-5702070f9dd5)
![image](https://github.com/jmart375/Reconnaissance/assets/91294710/fb417dc0-60dc-4e35-8973-09dc329ed482)

- A text editor opened in Kali with the names of all team members and the date displayed.
![image](https://github.com/jmart375/Reconnaissance/assets/91294710/43d0d7a6-7ced-41fd-994e-3eaf77311271)

## Reconnaissance Deliverables 2.2
The information below demonstrates how much information can be collected during an external data reconnaissance exercise. As you can see from the plethora of pictures, we ordered a ton of information on multiple services and servers, cloud providers, IP addresses, and subnets to move forward and try various attacks against the University of San Diego. All the information you see below has been collected off-site and off any VPN connecting back to the school. What items we came across that may or may not be a suitable attack vector? We identified a website by the name of adamboocher.com the University of San Diego is hosting it, and it's an Assistant Professor possibly currently employed. We could try making social engineering attacks against this teacher to collect more information further. 
### Deliverable 2.1.2 DNS

We found the following IP/DNS information using the commands in the picture below.
![image](https://github.com/jmart375/Reconnaissance/assets/91294710/144764e6-4312-4a09-a2ef-602c86bda542)

### Deliverable 2.1.3 The Whois Database

Using the whois command, we identified the following email address of the technical contact along with the authoritative name servers.
![image](https://github.com/jmart375/Reconnaissance/assets/91294710/38a3f7c1-dfcd-48d5-b51f-f909cceb208d)

### Deliverable 2.1.4 The ARIN Database

The Autonomous System Number (ASN) for USD is AS14255, and the IP address range (in CIDR format) is 192.195.152.0/22.
![image](https://github.com/jmart375/Reconnaissance/assets/91294710/9645bc2c-0fc1-48cc-a226-82dbc24f1ba4)

### Deliverable 2.1.5 SSL Certificates

What are the “alternative manes” or “DNS names” listed in the SSL certificate? Please reference the picture below.
![image](https://github.com/jmart375/Reconnaissance/assets/91294710/9d9505db-5451-4205-a2d0-ba81981c4e5a)

Ports open on SanDiego.edu.
![image](https://github.com/jmart375/Reconnaissance/assets/91294710/2dce9c52-9e5d-4428-9906-6e073d14e3f3)

### Other Info Discovered:

- Office Phone: +1-619-260-7900
- Mailbox: abuse@sandiego.edu
- Office Phone: +1-619-260-7900
- Mailbox: network@sandiego.edu

•	192.195.153.0/24	University of San Diego	256
•	192.195.154.0/24	University of San Diego	256
•	192.195.155.0/24	University of San Diego	256
•	192.55.87.0/24	University of San Diego	256
•	208.71.25.0/24	University of San Diego	256
•	208.71.27.0/24	University of San Diego	256
•	192.195.155.48	adamboocher.com … interesting… 

Twenty-four domains are being hosted on IP 192.195.155.200.
•	sandiego.edu
•	campusrj.com
•	burnhammoorescenterforrealestate.com
•	innovate-up.com
•	usdbmc.net
•	alisonyehcheung.com
•	usdprocopioiti.com
•	rjncc.org
•	robertschapiro.com
•	burnhammoorescenter.com
•	sdqol.org
•	effectivechangemaker.com
•	effectivechangemaker.org
•	resilientcoastlines.org
•	usdrealestate.com
•	campusprism.org
•	campusrj.org
•	usdburnhammoorescenter.com
•	sdqualityoflife.org
•	usdburnhammoorescenterforrealestate.com
•	sdclimatecollaborative.org
•	usdprocopioiti.info
•	impactpeace.org
•	Usdbmc.com

### Deliverable 2.1.6 Shodan

I. We found 252 hosts
![image](https://github.com/jmart375/Reconnaissance/assets/91294710/4e81edc1-7210-4847-8ee3-e6d9c001bf08)

II. We found 104 hosts on the 192.195.155.0/24 subnet

![image](https://github.com/jmart375/Reconnaissance/assets/91294710/988d6b4f-84b9-4e1e-a590-1eb31d97552c)
III. The ports pictured below are open on the subnet, and the listening services are in order from top to bottom. HTTPS,  HTTP, HTTPS (custom port) HTTP (custom port) SMTP, HTTP (custom port) and lastly HTTP (custom port)

![image](https://github.com/jmart375/Reconnaissance/assets/91294710/4e52fc1a-df50-4680-b305-7fd98ebab766)
IV. Above, We have 14 Linux computers running Apache, and we have six computers running IIS. 
V. we have a total of hosts running either version 7.5, 8.5, or 10.0 of IIS. 

![image](https://github.com/jmart375/Reconnaissance/assets/91294710/52ce21e5-5b53-47da-95c5-4a9d1803ca3f)
VI. the joint named for HTTPS on IIS is the following
•	usdadvanceweb.sandiego.edu
•	Starportal.sandiego.edu
•	Mediasitevideo2.sandiego.edu
•	Projecto.sandiego.edu
•	Itorero.sandiego.edu
•	mywellness.sandiego.edu
VII. the shodan search query is “net:192.195.155.0/24 port:443 product: "Microsoft IIS httpd"
VIII. Below is the Shodan report picture

![image](https://github.com/jmart375/Reconnaissance/assets/91294710/88add331-5882-4d39-b5e0-212d3edda023)

### Deliverable 2.1.7 Fierce Domain Name Scanner
![image](https://github.com/jmart375/Reconnaissance/assets/91294710/7d28afca-741f-4ce5-b1e2-e6960fecfe66)
What were the hostnames and IP addresses that fierce “found”? 
A lot! some of them were the following
•	Found: access.sandiego.edu. (192.195.155.83)
•	Found: ai.sandiego.edu. (104.154.181.98)
•	Found: arizona.sandiego.edu. (54.193.22.52)
•	Found: bb.sandiego.edu. (3.214.97.198)
•	blue.sandiego.edu. (52.37.118.199)
•	build.sandiego.edu. (192.195.155.226)
How many “nearby” hostnames and IP addresses were revealed by the DNS scan? 
A lot! some of them were the following
•	Nearby: {'104.154.181.100': '100.181.154.104.bc.googleusercontent.com.',
•	Nearby: {'54.193.22.47': 'ec2-54-193-22-47.us-west-1.compute.amazonaws.com.',
•	Nearby: {'3.214.97.193': 'ec2-3-214-97-193.compute-1.amazonaws.com.',
•	Nearby: {'52.37.118.195': 'ec2-52-37-118-195.us-west-2.compute.amazonaws.com.',
•	Nearby: {'192.195.155.221': 'genet.sandiego.edu.',
Can you identify some cloud service providers that USD uses?
•	Google 
•	Amazon
•	Cloudfront

## What would you suggest doing next?
The critical individual I would use for social engineering efforts is Cesar Fernandez since he is listed as the technical contact for the school. Next would be the president. This type of attack is also commonly known as “whale hunting” the president would also be a good target as he oversees the entire university and should have substantial privileges. Lastly, I would target new faculty, such as the new program coordinator, since they may not be fully acquainted with the university's policies.

## What hosts at what IP addresses/ports should be scanned for vulnerabilities?
I strongly suggest that SanDiego.edu affiliates like burnhammoorescenterforrealestate.com, usdburnhammoorescenter.com, and usdprocopioiti.info be scanned for vulnerabilities. School programs and partners make it very enticing for attackers to target via malware or social engineering.  A port scan can provide valuable information like the services running and the users who own the benefits. I would consider ports 80, 8080, 443, and 8443. Port 80, one of the more widely used protocols on the internet, makes the protocol equally prone to vulnerabilities. There are several ways to do so, like SQL injections and DDOS attacks.


## What other ideas about how you could proceed if this were a real pen test?

A deeper network scan of the USDs subnet, such as a map test, to see all the available ports to test. I would also try to talk to the local students and staff and try and collect information about local wireless policies and IT services public. Another thing we can try is using tools like Metasploit to identify known vulnerabilities and possibly set up a backdoor once we can exploit a known weakness. I strongly recommend using Nessus because it’ll comprehensively search many vulnerabilities and raise an alert if any discoveries are made. Nessus tests each port on a computer to determine what service is running and tries the service to ensure there are no vulnerabilities. Nessus is an open source that provides a scripting language to write tests specific to the system, offers a plug-in interface, and stays updated with information.

