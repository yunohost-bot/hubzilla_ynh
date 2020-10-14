# Hubzilla for YunoHost

[![Integration level](https://dash.yunohost.org/integration/hubzilla.svg)](https://dash.yunohost.org/appci/app/hubzilla)
[![Install Nextcloud with YunoHost](https://install-app.yunohost.org/install-with-yunohost.png)](https://install-app.yunohost.org/?app=hubzilla)

> *This package allow you to install Hubzilla quickly and simply on a YunoHost server.
If you don't have YunoHost, please see [here](https://yunohost.org/#/install) to know how to install and enjoy it.*

Version: **4.7.2**

### Interesting links

- [YunoHost project](https://yunohost.org)
- [Hubzilla website](https://zotlabs.org/page/hubzilla/hubzilla-project)
- [Hubzilla code on Framagit](https://framagit.org/hubzilla/core)
- [Hubzilla addons on Framagit](https://framagit.org/hubzilla/addons)


## Hubzilla
[Hubzilla](https://hub.libranet.de/directory?f=&global=1&pubforums=1) is a social networking platform built with control of your privacy at center stage. Your online communications can be as public as you wish or as private as you require. Private conversations, private photos, private videos. Your media isn't hidden behind an obscure URL which can be guessed, it is protected by state-of-the-art cross-domain authentication. What this all means for you: **less drama**.

![](https://fediverse.party/img/screenshots/hubzilla-1.png)



## This app claims following features:
- [X] Ldap integration
- [X] Multi-instance
- [X] Adeed php.log in the root folder for debugging php, with logrotate applied on it (can be accesssed by **admin->logs** and entering the **php.log**).
- [X] Fail2ban
- [X] Choose between **Mysql** and
**PostgreSQL** database to be used for the Hubzilla while installation.



## Installation
Before installing, read the [Hubzilla installation instructions](https://framagit.org/hubzilla/core/blob/master/install/INSTALL.txt) for important information about:


### Register a new domain and add it to YunoHost
- Hubzilla requires a dedicated domain, so obtain one and add it using the YunoHost admin panel. **Domains -> Add domain**. As Hubzilla uses the full domain and is installed on the root, you can create a subdomain such as hubzilla.domain.tld. Don't forget to update your DNS if you manage them manually.


## Ldap Admin user rights, logs and failed database updates

- **For admin rights**: When installation is complete, you will need to visit your new hub's page and login with the **admin account username** which was entered at the time of installation process. You should then be able to create your first channel and have the **admin rights** for the hub.

- **For normal YunoHost users :** Normal LDAP users can login through Ldap authentication and create there channels.

- **Failing to get admin rights :** If the admin cannot access the admin settings at `https://hubzilla.example.com/admin` or you want to grant admin rights to any other user(s) on the hub, then you have to **manually add 4096** to the **account_roles** under **accounts** for that user in the **database through phpMYAdmin**.

- **For logs :**  Go to **admin->logs** and enter the file name **php.log**.

- **Failed Database after Upgrade :** Some times databse upgrade fails after version upgrade. You can go to hub  eg. `https://hubzilla.example.com/admin/dbsync/` and check the numbers of failled update. These updates will have to be ran manually by **phpMYAdmin**.

#### Supported architectures

* x86-64b - [![Build Status](https://ci-apps.yunohost.org/ci/logs/hubzilla%20%28Official%29.svg)](https://ci-apps.yunohost.org/ci/apps/hubzilla/)
* ARMv8-A - [![Build Status](https://ci-apps-arm.yunohost.org/ci/logs/hubzilla%20%28Official%29.svg)](https://ci-apps-arm.yunohost.org/ci/apps/hubzilla/)
* Jessie x86-64b - [![Build Status](https://ci-stretch.nohost.me/ci/logs/hubzilla%20%28Official%29.svg)](https://ci-stretch.nohost.me/ci/apps/hubzilla/)
