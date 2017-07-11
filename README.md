# Funceble

> A script to check domains or IP accessibility.

The main idea was to create a script that can check if a given domain, a `hosts` file or a **list of domains** are/is **ACTIVE** or **INACTIVE**. And, in between, if wanted, **generate a `hosts` file** based on the results.

Have any question? Fill a new issue and I'll do my best to answer as soon as possible.

## :book: Wiki as place to be :star2::star2::star2:

Want to know more about **Funceble** ? All information to know are under the [wiki](https://github.com/funilrys/funceble/wiki)! You can also contribute there if you want! :smile:

You can get a copy of the wiki with the following:

```shell
git clone https://github.com/funilrys/funceble.wiki.git
```

## Features

- Read an existing `hosts`file and check every domain present into it.
- Change/set timeout for `whois`
- Deactivate logs
- Deactivate the production of unified results
- Silent mode available
- Show on screen

  - The status of a given domain is **ACTIVE**, **INACTIVE** or **INVALID** (live update)
  - The execution time of the script (at the end)
  - The percentage of **ACTIVE**, **INACTIVE** and **INVALID** (at the end)

- Save on single file

  - Result of execution (live update)
  - Execution time (at the end)
  - The percentage of **ACTIVE**, **INACTIVE** and **INVALID** (at the end)

- Save on separated files (when needed)

  - Logs of encountered error(s)
  - **ACTIVE** domain
  - **INACTIVE** domain
  - **INVALID** domain

- Generate `hosts` file

  - With custom IP
  - ONLY with **ACTIVE** domains

--------------------------------------------------------------------------------

# `Hosts` files

## What is a hosts file?

A hosts file, named `hosts` (with no file extension), is a plain-text file used by all operating systems to map hostnames to IP addresses.

In most operating systems, the `hosts` file is preferential to `DNS`. Therefore if a domain is resolved by the `hosts` file, the request never leaves your computer.

Having a smart `hosts` file goes a long way towards blocking malware, adware, ransomware, porn and other nuisance websites.

A hosts file like this causes any lookups to any of the listed domains to resolve back to your localhost so it prevents any outgoing connections to the listed domains.

## Recommendations

I'd personally recommend using [Steven's hosts](https://github.com/StevenBlack/hosts) or [Pi-Hole](https://github.com/pi-hole/pi-hole) which are in my opinion the best out there.
