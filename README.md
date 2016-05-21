Ansible Role for Composer Installation.
====================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-composer.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-composer)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-composer.svg)](https://github.com/pantarei/ansible-role-composer)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-composer.svg)](https://github.com/pantarei/ansible-role-composer/blob/master/LICENSE)

Ansible Role for Composer Installation.

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
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>composer_cache_valid_time</td>
<td>no</td>
<td>0</td>
<td></td>
<td>Pass value as <code>cache_valid_time</code> to <a href="http://docs.ansible.com/ansible/composer_module.html">composer module</a>.</td>
</tr>
<tr class="even">
<td>composer_name</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-composer/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Skip install packages if <code>[]</code>, or pass <code>list</code> to <a href="http://docs.ansible.com/ansible/composer_module.html">composer module</a>.</td>
</tr>
<tr class="odd">
<td>composer_repository_repo</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-composer/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Skip adding APT repository if <code>[]</code>, or pass <code>list</code> to <a href="http://docs.ansible.com/ansible/composer_repository_module.html">composer_repository module</a>.</td>
</tr>
<tr class="even">
<td>composer_upgrade</td>
<td>no</td>
<td>no</td>
<td><ul>
<li>no</li>
<li>yes</li>
<li>safe</li>
<li>full</li>
<li>dist</li>
</ul></td>
<td>Pass value as <code>upgrade</code> to <a href="http://docs.ansible.com/ansible/composer_module.html">composer module</a>.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: hswong3i.composer
          composer_cache_valid_time: "0"
          composer_upgrade: "full"

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-composer/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>

