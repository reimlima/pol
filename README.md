# pol

Simple Proof of Life script in Python

## Badges

[![python][python-badge]][python-version] ![pylint-score]

## Requirements

* **python >= 3.7**
* **PushOver Account**

## Setup

### Resolving Dependencies

```sh
pip3 install -r requirements.txt
```
### Config File

Rename the file `pol.sample.yml` to `pol.yml` and add informations as requested below.

You have to fill these fields in the [YAML] config file before your first run:

| Field              | Description                                                            |
|--------------------|------------------------------------------------------------------------|
| **pushover_api**   | Unless they changed the address, normally it is "api.pushover.net:443" |
| **pushover_token** | Find this information in [pushover doc]                                |
| **pushover_user**  | Find this information in [pushover doc]                                |

| Option              | Mandatory? | Description                                       |
|---------------------|------------|---------------------------------------------------|
| **-p, --port**      | Yes        | Ports to be checked, list space separated         |
| **-c, --config**    | Yes        | Path to Config File                               |
| **-e, --equipment** | Yes        | Address of the Equipment to be checked, IP or DNS |
| **-h, --help**      | No         | Show help like below                              |

### Systemd

Rename the file `pol.sample.service` to `pol.service`, change informations from command-line options and follow the steps to configure the script to run like a [systemd] service.

### Docker

Soon. 

## Command-line Options

```sh
# pol
usage: pol [-h] [-c CONFIG] [-e EQUIPMENT] [-p PORTS [PORTS ...]]

optional arguments:
  -h, --help            show this help message and exit
  -c CONFIG, --config CONFIG
                        Config file path
  -e EQUIPMENT, --equipment EQUIPMENT
                        Equipment to be monitored
  -p PORTS [PORTS ...], --ports PORTS [PORTS ...]
                        Port list, space separated
```

## Maintainer

 [Reinaldo Lima]

## License

See LICENSE file

[//]: #

[pushover doc]: https://docs.n8n.io/integrations/credentials/pushover/
[python-badge]: https://img.shields.io/badge/python-3.7.3-blue
[python-version]: https://www.python.org/downloads/release/python-375/
[pylint-score]: https://mperlet.github.io/pybadge/badges/10.00.svg
[Reinaldo Lima]: https://github.com/reimlima
[systemd]: https://wiki.debian.org/systemd/Services
[YAML]: https://en.wikipedia.org/wiki/YAML