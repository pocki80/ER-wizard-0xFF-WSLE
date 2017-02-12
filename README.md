# ER-wizard-0xFF-WSLE
BMK-Webstatus-LetsEncrypt Wizard for Ubiquiti EdgeMAX Devices supporting Wizards 

Installs and manages the Web-Status-Packages with LetsEncrypt-Setup from this git:
+ https://github.com/dabeani/0xFF-BMK-webstatus

what it does:
- on installation of wizard, downloads/extracts BMK-Webstatus-LE package to user-data
- shows webserver port settings and status of certificates, package installations
- shows certificate validity/expiary and FQDN for domain.csr and signed.crt
- trigger BMK-Webstatus Package-Install on apply() -> won't register FQDN certificate
- trigger FQDN certificate register and/or renewal on apply()
- restart webserices on apply()

known bugs/limitations:
- not all files from older versions are checked: bmk-webstatus-package will clean them on install anyway
- change webserver ports disabled, not yet fully implemented the change procedure
- apply will raise error message "failed" on following actions: 
  install, register/renew, restart-orig (webui session will break due to lighttpd restart)

open tasks
- fill up file-checks and package status for older versions
- include DEB to wizard base64-encoded, replace download procedure
- manage settings for BMK-Webstatus cgi-bin-status.php to configure:
  traceroute-destination, show_link_to_adminlogin, get_nslookup_from_nodedb, interface_1100_list

...in progress..
