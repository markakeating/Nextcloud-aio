### Installation of Nextcloud/postfix/amavisd/clamd/dovecot

## Prerequisites

# cadddy with acme-dns support

Install go > 1.21 per https://go.dev/doc/install```

Download xcaddy from https://github.com/caddyserver/xcaddy/releases
```
mkdir xcaddy
mv xcaddy_0.3.5_linux_amd64.tar.gz xcaddy/
cd xcaddy
tar xf xcaddy_0.3.5_linux_amd64.tar.gz
wget -o https://github.com/caddyserver/caddy/blob/master/cmd/caddy/main.go
./xcaddy build --with github.com/caddy-dns/route53

  ls /etc/letsencrypt/live/
  133  ls /etc/letsencrypt/live/hmsa-cloud.com/
  134  tail -f /var/log/maillog
  135  tail -f /var/log/maillog
  136  exit
  137  cat /etc/letsencrypt/live/hmsa-cloud.com/cert.pem
  138  cat /etc/letsencrypt/live/hmsa-cloud.com/privkey.pem
  139  cat /etc/letsencrypt/live/hmsa-cloud.com/README 
  140  sudo vi /etc/postfix/main.cf
  141  ls /etc/letsencrypt/live/hmsa-cloud.com/fullchain.pem 
  142  grep lets /etc/postfix/main.cf
  143  systemctl restart postfix
  144  tail -f /var/log/maillog
  145  systemctl restart postfix
  146  sudo vi /etc/dovecot/conf.d/10-ssl.conf 
  147  systemctl restart dovecot postfix
  148  tail -f /var/log/maillog
  149  ip a
  150  tail -f /var/log/maillog
  151  sudo vi /etc/postfix/main.cf
  152  sudo vi /etc/postfix/master.cf
  153  systemctl restart postfix
  154  tail -f /var/log/maillog
  155  vi /etc/postfix/main.cf
  156  vi /etc/postfix/main.cf
  157  systemctl restart postfix
  158  tail -f /var/log/maillog
  159  openssl s_client -connect localhost:25 -starttls smtp
  160  sudo vi /etc/httpd/conf.d/nextcloud-le-ssl.conf 
  161  sudo vi /etc/httpd/conf.d/nextcloud.conf 
  162  sudo vi /etc/httpd/conf.d/ssl.conf 
  163  tail -f /var/log/maillog
  164  reboot
  165  adduser 
  166  adduser -G wheel admin
  167  passwd admin
  168  cat ~/.ssh/authorized_keys 
  169  su admin
  170  ls -al ~/
  171  su admin
  172  tail -f /var/log/maillog
  173  ss -ltn
  174  systecmtl restart psotfix
  175  systemctl enable --now postfix
  176  ss -ltn
  177  tail -f /var/log/maillog
  178  clear
  179  tail -f /var/log/maillog
  180  passwd admin
  181  tail -f /var/log/maillog
  182  tail /var/log/messages
  183  firewall-cmd --list-all
  184  vi /etc/fail2ban/jail.local
  185  systecmtl restart fail2ban
  186  systemctl restart fail2ban
  187  vi /etc/fail2ban/jail.local
  188  firewall-cmd --list-all
  189  firewall-cmd --list-all
  190  tail -f /var/log/maillog
  191  vi /etc/dovecot/conf.d/10-auth.conf 
  192  grep -r location /etc/dovecot
  193  ce /etc/dovecot/conf.d/
  194  cd /etc/dovecot/conf.d/
  195  sed '/^[[:blank:]]*#/d;s/#.*//'
  196  sed '/^[[:blank:]]*#/d;s/#.*//' 10-auth.conf 
  197  grep "^[^#*/;]" 10-auth.conf 
  198  grep -e "^[^#*/;]" 10-auth.conf 
  199  grep -i "^[^#*/;]" 10-auth.conf 
  200  vi 10-auth.conf 
  201  grep -i "^[^#*/;]" 10-mail.conf 
  202  vi 10-mail.conf 
  203  systemctl restart dovecot
  204  tail -f /var/log/maillog
  205  cd /var/www/html/nextcloud/
  206  ls
  207  su -u apache php cron.php
  208  sudo -u apache php cron.php
  209  dnf search memcache
  210  dnf install -y php82-php-pecl-memcached
  211  dnf install -y php-pecl-memcached
  212  dnf search apc
  213  dnf -y install php-pecl-apcu php82-php-pecl-apcu
  214  systemctl restart hppd
  215  systemctl restart httpd
  216  sudo -u apache php cron.php
  217  grep -R apc.enable /etc
  218  vi /etc/opt/remi/php82/php.d/40-apcu.ini
  219  sudo -u apache php cron.php
  220  vi /etc/php.d/40-apcu.ini
  221  sudo -u apache php cron.php
  222  grep -R opcache.interned_strings_buffer /etc
  223  vi /etc/php.d/10-opcache.ini:;opcache.interned_strings_buffer=8
  224  vi /etc/php.d/10-opcache.ini
  225  systemctl restart httpd
  226  vi /etc/php-zts.d/10-opcache.ini 
  227  systemctl restart httpd
  228  reboot
  229  vi ~/.forward
  230  exit
  231  adduser hmsa
  232  passwd hmsa
  233  vi /etc/postfix/main.cf
  234  systemctl restart postfix
  235  tail -f /var/log/maillog
  236  systemctl status postfix
  237  vi /etc/postfix/main.cf
  238  tail -f /var/log/maillog
  239  cd /var/www/html/nextcloud/
  240  ls
  241  sudo -u apache php cron.php
  242  tail -f /var/log/maillog
  243  vi /etc/dovecot/conf.d/10-mail.conf 
  244  pwd
  245  cd /etc/dovecot/conf.d/
  246  grep lmtp ./
  247  grep lmtp
  248  grep lmtp *
  249  vi 10-master.conf 
  250  grpe protocols *
  251  grep protocols *
  252  grep protocols ../*
  253  vi /etc/postfix/main.cf
  254  vi /etc/postfix/main.cf
  255  vi 20-lmtp.conf 
  256  vi /etc/dovecot/dovecot.conf 
  257  systemctl resart dovecot
  258  systemctl restart dovecot.service
  259  vi /etc/dovecot/conf.d/10-master.conf 
  260  systemctl stat
  261  systemctl status dovecot.service
  262  vi /etc/dovecot/conf.d/10-master.conf 
  263  systemctl restart postfix.service
  264  systemctl restart dovecot.service
  265  journalctl -xe
  266  vi /etc/postfix/main.cf
  267  ps ax
  268  ps ax | grep ort
  269  ls -al /var/spool/
  270  ls -al /var/spool/postfix/
  271  ls -al /var/spool/postfix/private/
  272  vi /etc/dovecot/dovecot.conf 
  273  systemctl restart dovecot.service
  274  systemctl statys dovecot.service
  275  systemctl status dovecot.service
  276  tail -f /var/log/maillog
  277  sudo vi 10-master.conf 
  278  systemctl restart dovecot.service postfix.service
  279  tail -f /var/log/maillog
  280  clear
  281  c
  282  cd
  283  clear
  284  dnf install -y opendkim
  285  vi /etc/opendkim
  286  vi /etc/opendkim.conf 
  287  vi /etc/opendkim/SigningTable
  288  vi /etc/opendkim/KeyTable 
  289  vi /etc/opendkim/KeyTable 
  290  vi /etc/opendkim/TrustedHosts 
  291  mkdir -p /etc/opendkim/keys/hmsa-cloud.com
  292  mkdir -p /etc/opendkim/keys/houstonmasters.org
  293  dnf install opendkim-tools
  294  opendkim-genkey -b 2048 -d hmsa-cloud.com -D /etc/opendkim/keys/hmsa-cloud.com -s 20230626 -v
  295  opendkim-genkey -b 2048 -d houstonmasters.org -D /etc/opendkim/keys/houstonmasters.org -s 20230626 -v
  296  opendkim-genkey -b 2048 -d hmsa-cloud.com -D /etc/opendkim/keys/hmsa-cloud.com -s hmsa-cloud-20230626 -v
  297  opendkim-genkey -b 2048 -d hmsa-cloud.com -D /etc/opendkim/keys/hmsa-cloud.com -s 20230626 -v
  298  chown opendkim:opendkim /etc/opendkim/keys/ -R
  299  clear
  300  cat /etc/opendkim/keys/hmsa-cloud.com/20230626.txt
  301  ip a
  302  cat /etc/opendkim/keys/houstonmasters.org/
  303  cat /etc/opendkim/keys/houstonmasters.org/20230626.
  304  cat /etc/opendkim/keys/houstonmasters.org/20230626.txt
  305  clear
  306  opendkim-testkey -d hmsa-cloud.com -s 20230626 -vvv
  307  systemctl enable --now opendkim
  308  systemctl status opendkim.service
  309  opendkim-testkey -d houstonmasters.org -s 20230626 -vvv
  310  vi /etc/opendkim.conf 
  311  opendkim-testkey -d houstonmasters.org -s 20230626 -vvv
  312  opendkim-testkey -d hmsa-cloud.com -s 20230626 -vvv
  313  opendkim-testkey -d hmsa-cloud.com -s 20230626 -vvv
  314  opendkim-testkey -d hmsa-cloud.com -s 20230626 -vvv
  315  opendkim-testkey -d hmsa-cloud.com -s 20230626 -vvv
  316  opendkim-testkey -d hmsa-cloud.com -s 20230626 -vvv
  317  cat /etc/opendkim/keys/hmsa-cloud.com/20230626.txt
  318  cd /etc/opendkim/keys/
  319  ls
  320  cd hmsa-cloud.com/
  321  ls
  322  rm hmsa-cloud-20230626*
  323  ls
  324  opendkim-testkey -d hmsa-cloud.com -s 20230626 -vvv
  325  opendkim-testkey -d hmsa-cloud.com -s 20230626 -vvv
  326  opendkim-testkey -d houstonmasters.org -s 20230626 -vvv
  327  clear
  328  opendkim-testkey -d houstonmasters.org -s 20230626 -vvv
  329  clear
  330  opendkim-testkey -d hmsa-cloud.com -s 20230626 -vvv
  331  opendkim-testkey -d hmsa-cloud.com -s 20230626 -vvv
  332  opendkim-testkey -d hmsa-cloud.com -s 20230626 -vvv
  333  clear
  334  vi /etc/postfix/main.cf
  335  gpasswd -a postfix opendkim
  336  systemctl restart postfix.service
  337  systemctl status postfix.service
  338  tail -50 /var/log/maillog
  339  firewall-cmd --add-port=8891 --permanent
  340  firewall-cmd --add-port=8891/tcp --permanent
  341  firewall-cmd --list-all
  342  firewall-cmd --reload
  343  firewall-cmd --list-all
  344  tail -f /var/log/maillog
  345  vi /etc/postfix/main.cf
  346  systemctl restart postfix.service
  347  systemctl status postfix.service
  348  tail -f /var/log/maillog
  349  systemctl status opendkim.service
  350  vi /etc/opendkim.conf
  351  ss -ltn
  352  vi /etc/opendkim.conf
  353  vi /etc/postfix/main.cf
  354  systemctl restart postfix.service
  355  tail -f /var/log/maillog
  356  sudo -u apache crontab -l
  357  sudo crontab -l
  358  clear
  359  cat /etc/passwd
  360  sudo -u apache crontab -e
  361  tail /var/log/messages
  362  sudo -u apache php /var/www/html/nextcloud/cron.php 
  363  sudo -u apache crontab -e
  364  grep -R upload_max_filesize /etc
  365  vi /etc/opt/remi/php82/php.ini
  366  vi /etc/php.ini 
  367  systemctl restart httpd.service
  368  dnf -y update
  369  exxit
  370  exit
  371  dnf install amavisd-new
  372  clear
  373  vi /etc/amavisd/amavisd.conf 
  374  systemctl enable --now amavisd-new
  375  systemctl enable --now amavisd
  376  dnf install clamd
  377  vi /etc/clamd.d/scan.conf
  378  touch /var/log/clamd.scan
  379  chown clamscan. /var/log/clamd.scan 
  380  restorecon -Rv /var/log
  381  systemctl enable --now clamd@scan.service
  382  systemctl status clamd@scan.service
  383  journalctl xeu clamd@scan.service
  384  journalctl -xeu clamd@scan.service
  385  vi /etc/clamd.d/scan.conf 
  386  tail -50 /var/log/messages
  387  tail -50 /var/log/maillo
  388  journalctl -xeu clamd@scan.service
  389  ls /var/log
  390  view /var/log/clamd.scan 
  391  systemctl restart clamd@scan
  392  journalctl -xeu clamd@scan.service
  393  restorecon /etc/clamd.d/
  394  restorecon -Rv /etc/clamd.d/
  395  vi /etc/clamd.d/scan.conf 
  396  systemctl restart clamd@scan
  397  restorecon -v /var/log/clamd.scan 
  398  setsebool -P antivirus_can_scan_system on 
  399  vi /etc/amavisd/amavisd.conf 
  400  vi /etc/postfix/main.cf
  401  vi /etc/postfix/master.cf
  402  systemctl restart amavisd
  403  systemctl restart postfix
  404  tail -f /var/log/messages
  405  tail -f /var/log/maillog
  406  vi /etc/postfix/main.cf
  407  vi /etc/postfix/main.cf
  408  vi /etc/postfix/dnsrbl-reply-map
  409  postmap /etc/postfix/dnsbl-reply-map
  410  mv /etc/postfix/dnsrbl-reply-map /etc/postfix/dnsbl-reply-map
  411  postmap /etc/postfix/dnsbl-reply-map
  412  systemctl restart postfix.service
  413  tail -f /var/log/maillog
  414  cd /srv/nc-data
  415  ls
  416  ls -alF /var/www/html
  417  ls -alF /var/www/html/nextcloud
  418  ls -alF /var/www/html/nextcloud/lib
  419  ls -alF /var/www/html/nextcloud/config
  420  ls -alF /var/www/html/nextcloud/core
  421  vi /etc/dovecot/conf.d/10-master.conf 
  422  cat /etc/passwd
  423  cat /etc/group
  424  hsitory
  425  history
  426  cat /etc/postfix/main.cf
  427  :q
  428  cd /etc/postfix
  429  ls
  430  scp -i /home/rocky/.ssh/mark_ed25519 /etc/postfix/dnsbl-reply-map root@nextcloud.hmsa-cloud.com:/etc/postfix/
  431  ls /etc/
  432  cd /etc/amavisd/
  433  ls
  434  scp -i /home/rocky/.ssh/mark_ed25519 /etc/amavisd/amavisd.conf root@nextcloud.hmsa-cloud.com:/etc/amavisd/
  435  scp -i /home/rocky/.ssh/mark_ed25519 /etc/clamd.d/scan.conf root@nextcloud.hmsa-cloud.com:/etc/clamd.d/
  436  scp -i /home/rocky/.ssh/mark_ed25519 /etc/clamd.d/amavisd.conf root@nextcloud.hmsa-cloud.com:/etc/clamd.d/
  437  systemctl | grep clam
  438  history
  439  vi /etc/dovecot/conf.d/10-master.conf
```
