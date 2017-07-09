# Funceble

> A script to check domains or IP accessibilities.

The main idea was to create a script that can check if a given domain name or a **list of domains** are/is **ACTIVE** or **INACTIVE**. And, in between, if wanted, **create a hosts file** based on the results.

## Features

- Read an existing `hosts`file and check every domain present into it.
- Set a timeout for `whois`
- Deactivate logs
- Deactivate the production of unified results
- Silent mode available
- Show on screen

  - if domain name is **ACTIVE**, **INACTIVE** or **INVALID**
  - The execution time
  - The percentage of **ACTIVE**, **INACTIVE** and **INVALID**

- Save on single file

  - Result of execution
  - Execution time
  - The percentage of **ACTIVE**, **INACTIVE** and **INVALID**

- Save on separated files (when needed)

  - Logs of encountered error(s)
  - **ACTIVE** domain name
  - **INACTIVE** domain name
  - **INVALID** domain name

- Generate `hosts` file

  - With custom IP
  - ONLY with **ACTIVE** domain names

--------------------------------------------------------------------------------

# Usage

## funceble

```shell
Usage: ./funceble [ -a|--all ] [ -ex|--execution ] [ --help ] [ -h ] [ -ip ] [ -q|--quiet ] [ -n|--noFiles ] [ -p|--percentage ] [ -nl|--noLogs ] [ -nu|--noUnified ] [ --split ] [ -t|--timeout ]

       {[ -d domain-name.me ]} || {[ -f listOfDomainInAFile ]}

  --all                      -a              Output all information on screen (Must be before -d or -f)
  --domain                   -d              Domain to analyze
  --file                     -f              File with a list of domains
  --execution                -ex             Show the execution time (Must be before -d or -f)
  --help                                     Print this screen
                             -ip             Change the ip to print in host file (Must be before -d or -f)
  --host                     -h              Activate the generation of host (Must be before -d or -f)
  --quiet                    -q              Activate quiet mode (Must be before -d or -f)
  --percentage               -p              Show the percentage of the results (Must be before -d or -f)
  --noFiles                  -n              Deactivate the production of output files (Must be before -d or -f)
  --noLogs                   -nl             Deactivate the production of logs files in case we encounter some errors (Must be before -d or -f)
  --noUnified                -nu             Deactivate the production of result.txt as unified result under the output directory (Must be before -d or -f)
  --split                                    Split output files (Must be before -d or -f)
  --timeout                  -t              Seconds before timeout (Must be before -d or -f)
```

## tool

```shell
Usage: ./tool [ -d ] [ -h ]

       {[ -i ]} || {[ -p ]} || {[ -u ]}

  --debug                    -d              Activate the debug mode with the installation (Must be before -u or -i)
  --help                                     Print this screen
  --installation             -i              Execute the installation script
  --production               -p              Prepare the repository for production
  --update                   -u              Update the script
```

--------------------------------------------------------------------------------

# Status

## ACTIVE

- `whois` let us read the date of expiration
- `nslookup` don't return `server can't find domain-name.me: NXDOMAIN`

## INACTIVE

- `whois` don't let us read the date of expiration

**AND**

- `nslookup` return `server can't find domain-name.me: NXDOMAIN`

## INVALID

- Domain extension has an invalid format or is unregistered in **[IANA](https://www.iana.org/domains/root/db) Root Zone Database**.

--------------------------------------------------------------------------------

# How to contribute?

To contribute, you have to **send a new [Pull Request](https://github.com/funilrys/funceble/compare)** after you **[forked](https://github.com/funilrys/funceble/pulls#fork-destination-box)** and edited the script(s).

## :warning: WARNING :warning:

### DO NOT FORGET

- To sign your commit(s) with **"Signed-off by: FirstName LastName < email at service dot com >"** _**and/or**_ simply **sign your commit(s)** with **PGP** _(Please read more [here](https://github.com/blog/2144-gpg-signature-verification))_.

- All **contributions/modifications** must be done under **the `dev` or a new branch** if you plan to **send a new [Pull Request](https://github.com/funilrys/funceble/compare)**.

- :warning::warning::warning: Every **contributions/modifications** which are under **master** _(exception for minor changes)_ **will not be merged**.

--------------------------------------------------------------------------------

# Special Thanks

Thank you guys for your awesome lists which helped _(and still help)_ me build this script. :smile: :+1:

- [@mitchellkrogza](https://github.com/mitchellkrogza)
- [@PromoFaux](https://github.com/PromoFaux) with [Pi-Hole](https://github.com/pi-hole/pi-hole) hosts file.

# Contributors

- [@mitchellkrogza](https://github.com/mitchellkrogza)
- [@WaLLy3K](https://github.com/WaLLy3K)

--------------------------------------------------------------------------------

# `Hosts` files

## What is a hosts file?

A hosts file, named `hosts` (with no file extension), is a plain-text file used by all operating systems to map hostnames to IP addresses.

In most operating systems, the `hosts` file is preferential to `DNS`. Therefore if a domain name is resolved by the `hosts` file, the request never leaves your computer.

Having a smart `hosts` file goes a long way towards blocking malware, adware, ransomware, porn and other nuisance websites.

A hosts file like this causes any lookups to any of the listed domains to resolve back to your localhost so it prevents any outgoing connections to the listed domains.

## Recommendations

I'd personally recommend using [Steven's hosts](https://github.com/StevenBlack/hosts) or [Pi-Hole](https://github.com/pi-hole/pi-hole) which are in my opinion the best out there.

--------------------------------------------------------------------------------

# Logic representation

![](https://funilrys.com/user/pages/projects/funceble/global.png)
