# Chrony

Ansible role to setup ntp service  based on chrony

## Requirements

- ansible: version 2 and higher

## Role Variables

Some variables defaults are based on the support OS. These variables are in `vars/os-<OS>.yml` files.

### General Variables

`chrony_packages`: list of packages to install or remove based on the OS

`chrony_service`: service name based on the OS

`chrony_service`: configuration file location based on the OS

`chrony_file_keys`: ntp keys file locations

`chrony_log_dir`: log file directory

`chrony_backup`: if the  backup old chrony configuration files should be backuped

`chrony_backup`: if the service should be enabled

`chrony_service_state`: if the service should be started

### Configuration file Variables


The `ntp_config_directives` variable defined in `vars/main.yml` hold all supported `chrony.conf` variables with defautls. For each variable there is **name**, **type** and **default value**. 

To override the the default value set varibale `chrony_conf_<name>`, see some defaults in `defautls/main.yml`

If the type is

- **s** / **scalar**: use value enclosed in double quote, since values like **yes** and **no** have special meaning.
- **l** / **list**: use YAML list syntax, like `['val1', 'val2']`
- **b** / **list**: has boolean value indicating whether to display item


## Dependencies

None

## License

BSD

## Author Information

Peter Hudec