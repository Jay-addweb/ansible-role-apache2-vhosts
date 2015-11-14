Ansible Role for Apache2 Proxy
==============================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-apache2-proxy.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-apache2-proxy)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-apache2-proxy.svg)](https://github.com/pantarei/ansible-role-apache2-proxy)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-apache2-proxy.svg)](https://github.com/pantarei/ansible-role-apache2-proxy/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/5974.svg)](https://galaxy.ansible.com/detail#/role/5974)

Ansible Role for Apache2 Proxy Configuration.

Requirements
------------

This role require Ansible 1.9 or higher.

This role was designed for Ubuntu Server 14.04 LTS.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">parameter</th>
<th align="left">required</th>
<th align="left">default</th>
<th align="left">choices</th>
<th align="left">comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">apache2_proxy_crt</td>
<td align="left">no</td>
<td align="left"><code>null</code></td>
<td align="left"></td>
<td align="left">Skip if <code>null</code>, or pass value as <code>SSLCertificateChainFile</code> to <a href="https://github.com/pantarei/ansible-role-apache2-proxy/blob/release/1.0.0/templates/etc/apache2/sites-available/default.conf.j2">template</a>.</td>
</tr>
<tr class="even">
<td align="left">apache2_proxy_key</td>
<td align="left">no</td>
<td align="left">/etc/ssl/private/ssl-cert-snakeoil.key</td>
<td align="left"></td>
<td align="left">Skip if <code>null</code>, or pass value as <code>SSLCertificateKeyFile</code> to <a href="https://github.com/pantarei/ansible-role-apache2-proxy/blob/release/1.0.0/templates/etc/apache2/sites-available/default.conf.j2">template</a>.</td>
</tr>
<tr class="odd">
<td align="left">apache2_proxy_scheme</td>
<td align="left">yes</td>
<td align="left"><ul>
<li>http</li>
<li>https</li>
</ul></td>
<td align="left">http</td>
<td align="left">Enable proxy in HTTP mode if <code>http</code>, or enable as Enforced-HTTPS modue if <code>https</code>.</td>
</tr>
<tr class="even">
<td align="left">apache2_proxy_pass</td>
<td align="left">yes</td>
<td align="left">/ http://localhost:8080/</td>
<td align="left"></td>
<td align="left">Pass value as <code>ProxyPass</code> to <a href="https://github.com/pantarei/ansible-role-apache2-proxy/blob/release/1.0.0/templates/etc/apache2/sites-available/default.conf.j2">template</a>.</td>
</tr>
<tr class="odd">
<td align="left">apache2_proxy_pass_reverse</td>
<td align="left">yes</td>
<td align="left">/ http://localhost:8080/</td>
<td align="left"></td>
<td align="left">Pass value as <code>ProxyPassReverse</code> to <a href="https://github.com/pantarei/ansible-role-apache2-proxy/blob/release/1.0.0/templates/etc/apache2/sites-available/default.conf.j2">template</a>.</td>
</tr>
<tr class="even">
<td align="left">apache2_proxy_pem</td>
<td align="left">no</td>
<td align="left">/etc/ssl/certs/ssl-cert-snakeoil.pem</td>
<td align="left"></td>
<td align="left">Skip if <code>null</code>, or pass value as <code>SSLCertificateFile</code> to <a href="https://github.com/pantarei/ansible-role-apache2-proxy/blob/release/1.0.0/templates/etc/apache2/sites-available/default.conf.j2">template</a>.</td>
</tr>
<tr class="odd">
<td align="left">apache2_proxy_server_name</td>
<td align="left">yes</td>
<td align="left">example.com</td>
<td align="left"></td>
<td align="left">Pass value as <code>ServerName</code> to <a href="https://github.com/pantarei/ansible-role-apache2-proxy/blob/release/1.0.0/templates/etc/apache2/sites-available/default.conf.j2">template</a>.</td>
</tr>
</tbody>
</table>

Dependencies
------------

-   [hswong3i.apache2](https://galaxy.ansible.com/detail#/role/5972)

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hswong3i.apache2 }
        - { role: hswong3i.apache2_proxy }

License
-------

-   Code released under [MIT](https://github.com/hswong3i/ansible-role-apache2-proxy/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

