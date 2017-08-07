[root@ip-172-31-38-126 ~]# cat /etc/krb5.conf
[libdefaults]
default_realm = AINOWY.ES
dns_lookup_kdc = false
dns_lookup_realm = false
ticket_lifetime = 86400
renew_lifetime = 604800
forwardable = true
default_tgs_enctypes = rc4-hmac aes256-cts-hmac-sha1-96
default_tkt_enctypes = rc4-hmac aes256-cts-hmac-sha1-96
permitted_enctypes = rc4-hmac aes256-cts-hmac-sha1-96
udp_preference_limit = 1
kdc_timeout = 3000
[realms]
AINOWY.ES = {
kdc = ip-172-31-38-126
admin_server = ip-172-31-38-126
}
[domain_realm]
