Ansible Role for Apache2 VirtualHost
====================================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-apache2-vhosts.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-apache2-vhosts)
 [![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-apache2-vhosts.svg)](https://github.com/pantarei/ansible-role-apache2-vhosts)
 [![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-apache2-vhosts.svg)](https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/LICENSE)
 [![Ansible Role](https://img.shields.io/ansible/role/6294.svg)](https://galaxy.ansible.com/detail#/role/6294)

Ansible Role for Apache2 VirtualHost Management.

Requirements
------------

This role require Ansible 2.0 or higher.

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
<td align="left">apache2_vhosts_http_port</td>
<td align="left">yes</td>
<td align="left">80</td>
<td align="left"></td>
<td align="left">Apache2 VirtualHost HTTP port.</td>
</tr>
<tr class="even">
<td align="left">apache2_vhosts_https_port</td>
<td align="left">yes</td>
<td align="left">443</td>
<td align="left"></td>
<td align="left">Apache2 VirtualHost HTTPS port.</td>
</tr>
<tr class="odd">
<td align="left">apache2_vhosts_server_name</td>
<td align="left">yes</td>
<td align="left">example.com</td>
<td align="left"></td>
<td align="left">Hostname and port that the server uses to identify itself.</td>
</tr>
<tr class="even">
<td align="left">apache2_vhosts_server_admin</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Email address that the server includes in error messages sent to the client.</td>
</tr>
<tr class="odd">
<td align="left">apache2_vhosts_server_alias</td>
<td align="left">no</td>
<td align="left"><code>[]</code></td>
<td align="left"><ul>
<li><code>list</code></li>
<li><code>[]</code></li>
</ul></td>
<td align="left">Alternate names for a host used when matching requests to name-virtual hosts.</td>
</tr>
<tr class="even">
<td align="left">apache2_vhosts_error_log</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Location where the server will log errors.</td>
</tr>
<tr class="odd">
<td align="left">apache2_vhosts_custom_log</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Sets filename and format of log file.</td>
</tr>
<tr class="even">
<td align="left">apache2_vhosts_ssl_engine</td>
<td align="left">no</td>
<td align="left"></td>
<td align="left"><ul>
<li><code>On</code></li>
<li><code>Off</code></li>
</ul></td>
<td align="left">SSL Engine Operation Switch.</td>
</tr>
<tr class="odd">
<td align="left">apache2_vhosts_redirect</td>
<td align="left">no</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Sends an external redirect asking the client to fetch a different URL.</td>
</tr>
<tr class="even">
<td align="left">apache2_vhosts_ssl_certificate_chain_file</td>
<td align="left">no</td>
<td align="left"></td>
<td align="left"></td>
<td align="left">File of PEM-encoded Server CA Certificates.</td>
</tr>
<tr class="odd">
<td align="left">apache2_vhosts_ssl_certificate_file</td>
<td align="left">no</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Server PEM-encoded X.509 certificate data file.</td>
</tr>
<tr class="even">
<td align="left">apache2_vhosts_ssl_certificate_key_file</td>
<td align="left">no</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Server PEM-encoded private key file.</td>
</tr>
<tr class="odd">
<td align="left">apache2_vhosts_user</td>
<td align="left">yes</td>
<td align="left">example</td>
<td align="left"></td>
<td align="left">Username for virtual host user.</td>
</tr>
<tr class="even">
<td align="left">apache2_vhosts_pass</td>
<td align="left">yes</td>
<td align="left">Maih7eeB</td>
<td align="left"></td>
<td align="left">Password for virtual host user.</td>
</tr>
<tr class="odd">
<td align="left">apache2_vhosts_hash_salt</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Specific password hash salt for sha512.</td>
</tr>
<tr class="even">
<td align="left">apache2_vhosts_home</td>
<td align="left">yes</td>
<td align="left">/home/example</td>
<td align="left"></td>
<td align="left">Location for the virtual host user home directory.</td>
</tr>
<tr class="odd">
<td align="left">apache2_vhosts_document_root</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-apache2-vhosts/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"></td>
<td align="left">Directory that forms the main document tree visible from the web.</td>
</tr>
<tr class="even">
<td align="left">apache2_vhosts_proxy_pass</td>
<td align="left">no</td>
<td align="left"></td>
<td align="left"></td>
<td align="left">Maps remote servers into the local server URL-space.</td>
</tr>
<tr class="odd">
<td align="left">apache2_vhosts_proxy_pass_reverse</td>
<td align="left">no</td>
<td align="left"></td>
<td align="left"></td>
<td align="left">Adjusts the URL in HTTP response headers sent from a reverse proxied server.</td>
</tr>
<tr class="even">
<td align="left">apache2_vhosts_proxy_preserve_host</td>
<td align="left">yes</td>
<td align="left"></td>
<td align="left"><ul>
<li><code>On</code></li>
<li><code>Off</code></li>
</ul></td>
<td align="left">Use incoming Host HTTP request header for proxy request.</td>
</tr>
<tr class="odd">
<td align="left">apache2_vhosts_proxy_request</td>
<td align="left">no</td>
<td align="left"></td>
<td align="left"><ul>
<li><code>On</code></li>
<li><code>Off</code></li>
</ul></td>
<td align="left">Enables forward (standard) proxy requests.</td>
</tr>
<tr class="even">
<td align="left">apache2_vhosts_proxy_via</td>
<td align="left">yes</td>
<td align="left"></td>
<td align="left"><ul>
<li><code>On</code></li>
<li><code>Off</code></li>
</ul></td>
<td align="left">Information provided in the Via HTTP response header for proxied requests.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hswong3i.apache2_vhosts, apache2_vhosts_server_name: 'example.com' }

License
-------

-   Code released under [MIT](https://github.com/hswong3i/ansible-role-apache2-vhosts/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

