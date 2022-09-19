# iscctl

Tool for InterSystems products and supports both IRIS and Caché

## Installation

Download the latest version from the [releases](https://github.com/caretdev/iscctl/releases/latest) page. And extract to the desired place

## Commands

- [help](#help)
- [zversion](#zversion)
- [version](#version)

### help

```shell
$ iscctl help
iscctl 0.1.0
Dmitry Maslennikov <dmitry@caretdev.com>
Simple checker version of InterSystems IRIS

USAGE:
    iscctl [OPTIONS] <SUBCOMMAND>

OPTIONS:
    -H, --host <HOST>              Host [default: localhost]
    -P, --port <PORT>              Port [default: 1972]
    -n, --namespace <NAMESPACE>    Namespace [default: USER]
    -u, --username <USERNAME>      Username
    -p, --password <PASSWORD>      Password
    -h, --help                     Print help information
    -V, --version                  Print version information

SUBCOMMANDS:
    zversion    Prints $ZVersion
    version     Prints Version Number in full form, e.g. 2022.2.0.334
    help        Print this message or the help of the given subcommand(s)
```

### zversion

```shell
$ iscctl -H localhost -P 1972 -n %SYS -u _SYSTEM -p SYS zversion
IRIS for UNIX (Ubuntu Server LTS for x86-64 Containers) 2022.2 (Build 334U) Fri Sep 9 2022 01:11:15 EDT

$ iscctl -H localhost -P 1973 -n %SYS -u _SYSTEM -p SYS zversion
Cache for UNIX (Red Hat Enterprise Linux for x86-64) 2018.1.5 (Build 659U) Mon Mar 22 2021 07:12:43 EDT
```

### version

```shell
$ iscctl -H localhost -P 1972 -n %SYS -u _SYSTEM -p SYS version
2022.2.0.334
```
