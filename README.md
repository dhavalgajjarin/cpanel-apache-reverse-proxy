![Banner](https://cpanel.net/wp-content/themes/cPbase/assets/img/logos/cPanel_orange.svg)

# cPanel Apache Reverse Proxy

This repository contains a simple script which can be used to configure reverse proxy in cPanel with Apache

## Prerequisites

1. cPanel Server
2. Apache Modules
   1. [`mod_proxy`] **_-- Required_**
   1. [`mod_proxy_http`] **_-- Required_**
   1. [`mod_proxy_connect`] _-- Optional._
   1. [`mod_proxy_wstunnel`] _-- Optional. enable if you want to use WebSockets_

[`mod_proxy`]: http://httpd.apache.org/docs/current/mod/mod_proxy.html
[`mod_proxy_http`]: https://httpd.apache.org/docs/2.4/mod/mod_proxy_http.html
[`mod_proxy_connect`]: https://httpd.apache.org/docs/2.4/mod/mod_proxy_connect.html
[`mod_proxy_wstunnel`]: https://httpd.apache.org/docs/2.4/mod/mod_proxy_wstunnel.html

## 🚀 Usage

### 1. Download The Proxy Script

```shell
wget https://raw.githubusercontent.com/dhavalgajjarin/cpanel-apache-reverse-proxy/main/setup-reverse-proxy.sh
```

### 2. Run To Create A New Proxy

```shell
# setup-reverse-proxy.sh {account_username} {subdomain/domain} {local_application_url}

setup-reverse-proxy.sh "cpanelAccountName" "api.mydomain.com" "http://localhost:8080"
```

### 3. Rebuild & Restart HTTP

```
/scripts/rebuildhttpdconf && service httpd restart
```

---

## 🤝 Contributing

If you would like to help, please take a look at the list of [issues](https://github.com/dhavalgajjarin/cpanel-apache-reverse-proxy/issues/).

## 📜 License

- [**GNU General Public License v3.0**](https://github.com/dhavalgajjarin/cpanel-apache-reverse-proxy/blob/main/LICENSE)

## 📣 Feedback

- ⭐ This repository if this project helped you! :wink:
- Create An [🔧 Issue](https://github.com/dhavalgajjarin/cpanel-apache-reverse-proxy/issues/) if you need help / found a bug

## Connect & Say 👋

- **Follow** me on [👨‍💻 Github][github]
- **Follow** me on [🐦 Twitter][twitter]

<!-- Personl Links -->

[github]: https://github.com/dhavalgajjarin
[twitter]: https://twitter.com/dhavalgajjarin

## Thanks to:

- Varun Sridharan
