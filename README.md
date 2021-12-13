module to ensure that  sudo requires password
=============================================

Ensures `/etc/sudoers` and `/etc/sudoers.d/*` files
don't allow passwordless sudo:

* Removes `NOPASSWD:` entries
  (changes them to `PASSWD:`)

* Removes `exempt_group` setting
  (comments it out)

Security notice
---------------

> While this module tries its best,
> it can't guarantee a protection against
> a malitious sysadmin.
> They can always `chomd u+s` a copy of bash,
> or replace `sudo` binary with their own copy,
> or configure it to use a different security policy plugin,
> or to look for config files in a different place.

