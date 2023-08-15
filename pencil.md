docker run  --hosname mailserver -p 25:25 -p 465:465 -p 587:587 -p 993:993  -env MAIL_USER=pencil -env MAIL_PASSWORD=pencil  ghcr.io/docker-mailserver/docker-mailserver:latest



```
docker run --rm -it                                      \
  --env MAIL_USER=pencil@pencil.com                      \
  --env MAIL_PASS=pencil                             \
  ghcr.io/docker-mailserver/docker-mailserver:latest     \
  /bin/bash -c \
    'echo "${MAIL_USER}|$(doveadm pw -s SHA512-CRYPT -u ${MAIL_USER} -p ${MAIL_PASS})" >>docker-data/dms/config/postfix-accounts.cf'
```



docker exec -ti mailserver setup email add pencil




```bash
sudo docker run -p 587:587 \
		-e maildomain=mail.example.com -e smtp_user=user:pwd \
		-v /home/kaspar/stuff/sources/pencil/src/test/resources/certssudo docker run -p 587:587 \
		-e maildomain=mail.example.com -e smtp_user=user:pwd \
		-v /path/to/certs:/etc/postfix/certs \
		--name postfix -d catatnight/pos:/etc/postfix/certs \
		--name postfix -d catatnight/postfix
```