# ER-wizard-0xFF-WSLE
BMK-Webstatus-LetsEncrypt Wizard for Ubiquiti EdgeMAX Devices supporting Wizards 

Installs and manages the Web-Status-Packages with LetsEncrypt-Setup from this git:
+ https://github.com/dabeani/0xFF-BMK-webstatus as of version v4.1

what it does:
- on installation of wizard, downloads/extracts BMK-Webstatus-LE package to user-data
- shows webserver port settings and status of certificates, package installations
- shows certificate validity/expiary and FQDN for domain.csr and signed.crt
- trigger BMK-Webstatus Package-Install on apply() -> won't register FQDN certificate
- trigger FQDN certificate register and/or renewal on apply()
- change webserver ports, use with care as webgui-session will most likely break
- restart webserices on apply()

known bugs/limitations:
- not all files from older versions are checked: bmk-webstatus-package will clean them on install anyway
- apply will raise error message "failed" on following actions: 
  install, register/renew, restart-orig (webui session will break due to lighttpd restart)

open tasks
- fill up file-checks and package status for older versions
- manage settings for BMK-Webstatus cgi-bin-status.php to configure:
  traceroute-destination, show_link_to_adminlogin, get_nslookup_from_nodedb, interface_1100_list

...in progress..
