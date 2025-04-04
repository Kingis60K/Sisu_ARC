# Setting up webmail + smtp for SisuCTF.com

Echoctf framework uses smtp to send email to users. This all has to be setup manually, google smtp relay is recommended(google workspaces subscription)Google is easy and usually trustworthy relay(not getting flagged as spam/junk). but we opted to go for a cheaper route with some more work(DKIM). 

Plan: mxroute & DKIM Records to avoid getting flagged as spam


## DNS Records for email

Adding Custom MX records on our dns provider (namecheap)

For our mxroute account we have been assigned following:
```
wednesday.mxrouting.net (Priority 10)
wednesday-relay.mxrouting.net (Priority 20)
```
![](assets/1741532075404.png)

TXT SPF record:

![](assets/1741532195539.png)


DKIM+DMARC records:

![](assets/1741533141604.png)

## Webmail send + recieve

Setting up new domain on mxroute

![](assets/1741520356146.png)

Creating a test address riki@sisuctf.com

testing email sending from mxroute webmail with sisuctf domain to outlook

![](assets/1741532940514.png)

Email sending works, but identified as spam/junk, trying this later since records might still be propagating. 

![](assets/1741532965154.png)

using toolbox.googleapps.com to test records, not yet active.

![](assets/1741533427118.png)


Testing reply from outlook to riki@sisuctf.com

![](assets/1741533034537.png)

works!

## Setting up mail.sisuctf.com webmail

Setting DNS record for subdomain mail.sisuctf.com

![](assets/1741533790802.png)

SSL certificate setup on mxroute, using letsencrypt automatic cert.

![](assets/1741533699496.png)

![](assets/1741533769850.png)

webmail works with custom subdomain:

![](assets/1741533934151.png)

## modified to use STARTTLS



![](assets/1743400415311.png)