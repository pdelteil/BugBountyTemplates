
# Elmah.axd is publicly accessible leaking Error Log

## Summary

ELMAH (Error Logging Modules and Handlers) is an application-wide error logging facility that is completely pluggable. If ELMAH is not properly configured, the **elmah.axd** handler can be accessed without authorization. This page will list all the error messages generated by the web application.

## Steps To Reproduce

Go to  $URL
From here you can download the entire log going to this [URL]($URL). 
I found some errors that had sensitive information:
- [Cookie](https://$DOMAIN/elmah.axd/detail?id=8eb722b8-4628-421a-ad32-36c945e23e3b) (ss-pid=nRWaLI079kORwvV5HN/tgw==; ASP.NET_SessionId=REDACTED-.. **truncated**)
- Local paths (REDACTED) 
- IP Address (REDACTED)


## Impact
 May disclose sensitive information to an attacker, users cookies, IP addresses and more. 


### Supporting Material/References:
- https://hackerone.com/reports/962753


