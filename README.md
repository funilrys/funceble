# Funceble

A script to check domains or IP accessibilities.

The main idea was to create a script that can **check if domain** or a **list of domains** are/is **ACTIVE** or **INACTIVE**. And, in between, **create a hosts file** base on the results.

For all issues/bugs and others, please report [here](https://github.com/funilrys/funceble/issues/new).

Current Version: **1.0.0**

## NB Status

* **ACTIVE**
    * Date of expiration accessible per WHOIS-Server (`whois` command)
    * `nslookup` Don't return "**server can't find domain-name.me: NXDOMAIN**"
* **INACTIVE**
    * WHOIS-Server don't return anything
    * nslookup return "**server can't find domain-name.me: NXDOMAIN**"
* **INVALID**
    * Domain extension has an invalid format or is unregistered in **[IANA](https://www.iana.org/domains/root/db) Root Zone Database**.

## Usage

```sh
Usage: ./funceble [ --help ] [ -h ] [ -ip ] [ -q ] [ -n ] [ --split ]

       {[ -d domain-name.me ]} || {[ -f listOfDomainInAFile ]}

  --domain                   -d              Domain to analyze
  --file                     -f              File with a list of domains
  --help                                     Print this screen
                             -ip             Change the IP to print in the host file
  --host                     -h              Activate the generation of host (Must be before -d or -f)
  --quiet                    -q              Activate quiet mode (Must be before -d or -f)
  --noFiles                  -n              Deactivate the production of output files (Must be before -d or -f)
  --split                                    Split output files (Must be before -d or -f)
```

## How to contribute?

To contribute, you have to send a new [Pull Request](https://github.com/funilrys/funceble/compare) after you [forked](https://github.com/funilrys/funceble/pulls#fork-destination-box) and edited the script(s).

### DO NOT FORGET

* To sign your commit(s) with **'Signed-off by: FirstName LastName <e at mail dot com>'** AND/OR simply sign your commit(s) with **PGP**. **Please read more [here](https://github.com/blog/2144-gpg-signature-verification)**.
* All contributions/modifications must be done under **the `dev` branch**.

____
# Special Thanks
Thank you guys for your awesome lists which helped _(and still help)_ me build this script. :smile: :+1:

* [@mitchellkrogza](https://github.com/mitchellkrogza)
* [@PromoFaux](https://github.com/PromoFaux) with [Pi-Hole](https://github.com/pi-hole/pi-hole) hosts file.

# Contributors

* [@WaLLy3K](https://github.com/WaLLy3K)

____
# `Hosts` files

If you're not familiar with `hosts` files, take a look at [this short definition](http://www.computerhope.com/jargon/h/hostsfil.htm).

I'd personally recommend using [Steven's hosts](https://github.com/StevenBlack/hosts) or [Pi-Hole](https://github.com/pi-hole/pi-hole) which are in my opinion the best out there.
