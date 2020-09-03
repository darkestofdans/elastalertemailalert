# ElastAlert Email Alerts

A sample ElastAlert that will send an email when a DNS entry is found matching the list in the domain_list.txt.

### Prerequisites

Security Onion, email account (Gmail is require IMAP enabled and allowing less secure applications to authenticate)

### Installing

Edit the domain_list.txt placing one domain per line.

Place email credentials in smtp_auth_file.txt

Place all three files in /etc/elastalert/rules

Adjust the permissions on the auth file.

```
sudo chown elastalert:elastalert /etc/elastalert/rules/smtp_auth_file.txt 
sudo chmod 600 /etc/elastalert/rules/smtp_auth_file.txt 
```

## Test

Purposely trigger the alert by visiting the domain and then check your email.