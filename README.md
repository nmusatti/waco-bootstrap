waco-bootstrap
==============

A set of bash scripts and Ansible playbooks to install and run the
[waco_master](https://github.com/waco-org/waco-master.git) role. 

- Download or clone this repository to the `/tmp` directory of your newly installed EL, Fedora or
  Ubuntu LTS system;
- As `root` run the `waco-bootstrap` script, which will install Git and Ansible, create the
  `waco` user and copy the installation to `waco`'s home directory;
- Edit the `~waco/waco/settings/master.yml` file to suit your needs;
- As `waco` run the `~waco/waco/waco-provision` script, which will ensure Ansible 2.10 is
  installed, download the required roles and apply `waco-master`.

If you plan to apply `waco-master` to several systems you might consider forking this repository
and modify `master.yml` in your copy.

Known problems
--------------

Currently installing as the waco user fails due to a problem in a dependency. Run `waco-provision`
as root instead.
