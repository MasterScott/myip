# myip

Get your external IP address from command line.

[![Build Status](https://dev.azure.com/nekomimiswitch/General/_apis/build/status/myip?branchName=master)](https://dev.azure.com/nekomimiswitch/General/_build/latest?definitionId=72&branchName=master)

## Usage

### Basic Usage

```shell
$ myip
2001:db8::2

$ myip -4
192.0.2.2

$ myip -6
2001:db8::2
```

### STUN

* This is the default method
* `stun.l.google.com:19302` is the default server
* Connection over UDP only

```shell
myip --method STUN --server stun.l.google.com:19302
```

### ip.sb HTTPS API

```shell
myip --method ip.sb
```

### OpenDNS DNS Query

```shell
myip --method OpenDNS
```

### OpenDNS HTTPS API

* `-4`/`-6` doesn't work

```shell
myip --method OpenDNS-API
```

## Building

Use go 1.11 or higher. Run `build.sh` to build and collect your artifact in `build` directory.

## Donation

If this project is helpful to you, please consider buying me a coffee.

[![Buy Me A Coffee](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/Jamesits) or [PayPal](https://paypal.me/Jamesits)
