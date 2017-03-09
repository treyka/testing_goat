Provisioning a new site
=======================

Required packages:
------------------
* Apache2
* Python 3
* Git
* pip
* virtualenv

* e.g., on Debian: `sudo aptitude install apache2 git python3 python3-venv`
    
Apache2 Virtual Host config
---------------------------
* see apache2.template.conf
* replace SITE_NAME with, e.g., staging.my-domain.com
* `a2enmod proxy proxy_http`
    
Systemd service
---------------
* see gunicorn-systemd.template.service
* replace SITE_NAME with, e.g., staging.my-domain.com
    
Folder structure:
-----------------
Assume we have a user account at /home/username
    
/home/username
└── sites
    └── SITENAME
        ├── database
        ├── source
        ├── static
        └── virtualenv
