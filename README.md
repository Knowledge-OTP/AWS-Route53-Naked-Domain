# AWS-Route53-Naked-Domain
This repo describe the steps to have a naked domain with https support managed in AWS route53

- Make sure to have a domain register (in amazon or any other domain provider)
- Use for example "zinckers.com"
- Go to hosted zones -> Create hosted zone -> Domain name: zinckers.com -> Create
- Create Record Set -> Name: '' (empty), Type: A, Alias: yes
- In alias target field, select the relevant cloudfront distrbution for this domain (make sure this domain is listed in the cname fields in the cloudfront distrbution)
- Create Record Set -> Name: www (empty), Type: A, Alias: yes
- In alias target field, select the relevant cloudfront distrbution for this domain (make sure this domain is listed in the cname fields in the cloudfront distrbution)
- Look in the NS record, copy the name of the name servers
- Make sure to domain name servers listed the name servers from the previous section
