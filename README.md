# `http-notify`

<br>

<p align="left">
  <a href="https://img.shields.io/badge/Branch-master-green.svg">
    <img src="https://img.shields.io/badge/Branch-master-green.svg"
        alt="Branch">
  </a>
  <a href="https://travis-ci.org/trimstray/http-notify">
    <img src="https://travis-ci.org/trimstray/http-notify.svg?branch=master"
        alt="Travis-CI">
  </a>
</p>

## How To Use

  > Before use **http-notify** please see **[Requirements](#requirements)**.

It's simple:

```bash
# Clone this repository
git clone https://github.com/trimstray/http-notify

# Go into the repository
cd http-notify

# Edit src/wtop.cfg
#   - set properly log format (LOG_FORMAT)
#   - set properly log directory (LOG_ROOT)
#   - set properly log filename (LOG_FILE)

# Run the app
#   - for monitor mode
./bin/http-notify -m monitor -l /var/log/httpd/access_log -f "login" --mailto admin@example.com

client_ip      cc  proto     code    bytes   path
---------      --  -----     ----    -----   ----
216.58.215.28  US  HTTP/1.0  200     11429   /index.php/login
78.224.23.85   FR  HTTP/2.0  200     10522   /admin/login
...

#   - for stats mode
./bin/http-notify -m stats -l /var/log/httpd/access_log
client_ip       cc      proto           code    bytes   count   path
---------       --      -----           ----    -----   -----   ----
10.240.30.3     None    HTTP/1.1        200     1567    14      https://dvwa.nsbox.int/login.php
10.240.30.3     None    HTTP/1.1        302     0       14      https://dvwa.nsbox.int/
10.240.30.3     None    HTTP/1.1        404     281     1       https://dvwa.nsbox.int/asdf
192.168.252.1   None    HTTP/1.1        200     721     1       https://dvwa.nsbox.int/login.php?cache=137115269
192.168.252.1   None    HTTP/1.1        200     9088    25      https://dvwa.nsbox.int/dvwa/images/login_logo.png
192.168.252.1   None    HTTP/1.1        200     1405    14      https://dvwa.nsbox.int/setup.php
192.168.252.1   None    HTTP/1.1        200     722     1       https://dvwa.nsbox.int/login.php?cache=1e885d96a
```

<br>

<p align="center">
    <img src="https://i.imgur.com/RsEy4TU.gif"
         alt="Master">
</p>

###### Mail notification

<p align="center">
    <img src="https://github.com/trimstray/http-notify/blob/master/doc/img/http-notify-mail-report.png"
        alt="Master">
</p>

## Requirements

This tool working with:

- **GNU/Linux** (testing on Debian and CentOS)
- **[Bash](https://www.gnu.org/software/bash/)** (testing on 4.4.19)
- **[wtop](https://github.com/ClockworkNet/wtop)** (testing on 0.7.11)

### wtop/logrep installation

`wtop` can be installed from PyPI via pip like so:

```bash
pip install wtop
```

## Parameters

Provides the following options:

```bash
    http-notify v1.0.0

  Usage:
    http-notify <option|long-option>

  Examples:
    http-notify --help
    http-notify -m stats -l /var/log/httpd/access_log
    http-notify -m monitor -l /var/log/httpd/access_log -f "login" --mailto admin@example.com

  Options:
        --help                                show this message
        -m|--mode                             set mode type: stats or monitor
        -l|--logfile                          set path to logfile
        -f|--filter                           set filter (e.g. by url)
        --mailto                              set mail recipient
```

## Contributing

See **[this](CONTRIBUTING.md)**.

## License

GPLv3 : <http://www.gnu.org/licenses/>

**Free software, Yeah!**
