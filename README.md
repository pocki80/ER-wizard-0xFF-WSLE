# ER-wizard-0xFF-WSLE
BMK-Webstatus-LetsEncrypt Wizard for Ubiquiti EdgeMAX Devices supporting Wizards 

**IMPORTANT**: the status page uses python for current EdgeOS versions, and PHP on EdgeOS v1.9.7alpha2 or older.

Installs and manages the Web-Status-Packages with LetsEncrypt-Setup from this git:
+ https://github.com/dabeani/0xFF-BMK-webstatus

what it does:
- on installation of wizard, installs BMK-Webstatus-LE package
- shows webserver port settings and status of certificates, package installations
- shows certificate validity/expiary and FQDN for domain.csr and signed.crt
- trigger FQDN certificate register and/or renewal on apply()
- change webserver ports
- restart webserices on apply()

known bugs/limitations:
- not all files from older versions are checked: bmk-webstatus-package will clean them on install anyway
- apply will raise error message "failed" on following actions: 
  install, register/renew, restart-orig (webui session will break due to lighttpd restart)

...in progress..
