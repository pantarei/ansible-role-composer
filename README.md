Ansible Role for Composer Installation.
=======================================

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
<td>composer_global_require</td>
<td>no</td>
<td><code>[]</code></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Skip install gloabl packages if <code>[]</code>, or pass list to <code>composer global require</code>.</td>
</tr>
<tr class="even">
<td>composer_home</td>
<td>no</td>
<td>/usr/share/composer</td>
<td></td>
<td>Location for the <code>$COMPOSER_HOME</code> directory..</td>
</tr>
<tr class="odd">
<td>composer_install_dir</td>
<td>no</td>
<td>/usr/bin</td>
<td></td>
<td>Location for the composer install directory.</td>
</tr>
<tr class="even">
<td>composer_installer_checksum</td>
<td>no</td>
<td><a href="https://github.com/pantarei/ansible-role-composer/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>Download archive sha256 checksum for cache during (re)install.</td>
</tr>
<tr class="odd">
<td>composer_installer_dest</td>
<td>no</td>
<td>/tmp/composer-setup-php</td>
<td></td>
<td>Download archive filename for cache during (re)install.</td>
</tr>
<tr class="even">
<td>composer_installer_rul</td>
<td>no</td>
<td>https://getcomposer.org/installer</td>
<td></td>
<td>URL for download composer installer.</td>
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
          composer_global_require:
            - "drush/drush:@stable"
            - "fabpot/php-cs-fixer:@stable"
            - "phpunit/phpunit:@stable"
            - "sami/sami:@stable"

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-composer/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>

