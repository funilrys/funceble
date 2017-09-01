Want to contribute ? Let us first thank you for your action!!

:heart: :tada: :heart: :tada:

```
.___________. __    __       ___      .__   __.  __  ___      _______.    __  
|           ||  |  |  |     /   \     |  \ |  | |  |/  /     /       |   |  |
`---|  |----`|  |__|  |    /  ^  \    |   \|  | |  '  /     |   (----`   |  |
    |  |     |   __   |   /  /_\  \   |  . `  | |    <       \   \       |  |
    |  |     |  |  |  |  /  _____  \  |  |\   | |  .  \  .----)   |      |__|
    |__|     |__|  |__| /__/     \__\ |__| \__| |__|\__\ |_______/       (__)
```

:heart: :tada: :heart: :tada:

There are many ways to contribute here's few way about how to contribute!

# Fix typography

I'm not an English native speaker so you can help by fixing the typography in Wiki, README.md or even my comments under `funceble` and `tool`!

If you plan to fix typography into `funceble` and or `tool` please be sure to read the [:warning: WARNING :warning:](https://github.com/funilrys/funceble/wiki/How-to-contribute%3F/#warning-warning-warning) part first.

# Suggest new Features

I like to get suggestion about things I didn't think about! So let me know your suggestion if it's possible and once it's implemented your name/nickname will be added in the [Special Thanks and Contributors](https://github.com/funilrys/funceble/wiki/Special-Thanks-and-Contributors) section! :smile:

# Hack :smile:

The best way to contribute is to hack funceble :smile:. Simply **send a new [Pull Request](https://github.com/funilrys/funceble/compare)** with your modifications after you **[forked](https://github.com/funilrys/funceble/pulls#fork-destination-box)** and edited the repository.

Once done, let's talk about your modifications :+1::smile: !!!

--------------------------------------------------------------------------------

# :warning: WARNING :warning:

If you plan to **send a new [Pull Request](https://github.com/funilrys/funceble/compare)**:

- All **contributions/modifications** must be done under **the `dev` or a new branch**.
- You should follow the following convention
- Your [Pull Request](https://github.com/funilrys/funceble/compare) description should be as possible description
- All your commits should be signed:

  - With **"Signed-off by: FirstName LastName < email[at]service[dot]com >"** at the end of the commit message/description

- **AND/OR**

  - With **PGP** _(Please read more [here](https://github.com/blog/2144-gpg-signature-verification))_.

--------------------------------------------------------------------------------

# Conventions

You should follow the following convention in order to get your Pull Request merged.

## Comments

Avoid comments at the end of a line, comment before the begining of the line.

```bash
# This is the proof of Arch's superiority
myAwesomeVariable='Arch is the best!'


myAwesomeVariable='Arch is the best!' # This is a really really bad place to comment that line
```

## Variables

### Naming

The name of the variables should be descriptive and written in [camelCase](https://en.wikipedia.org/wiki/Camel_case). It would be even better if you add a comment before the variable declaration.

```bash
# This is the proof of Arch's superiority
myAwesomeVariable='Arch is the best!'

# This are examples of really bad ideas
MYAWESOMEVARIABLE='Arch is the best!'
my_Awesome_Variable='Arch is the best!'
```

### Calling

The way you call your variable should be like the following.

```bash
# This is the proof of Arch's superiority
myAwesomeVariable='Arch is the best!'

# Awesome
echo ${myAwesomeVariable}

# Really bad idea
echo $myAwesomeVariable
```

## Function

### Naming

Functions should also be descriptive and written in [camelCase](https://en.wikipedia.org/wiki/Camel_case). It's even better if you add a comment block before to describe its purpose.

```bash
############################# Print Arch is the best ###########################
# This an example of naming and comment convention.
# This function print "Arch is the best!" on screen
#
# @CalledBy functionA, functionC
################################################################################
printArchIsTheBest()
{
    # Let's show the world who's superior!
    echo "Arch is the best!"
}

################################# Bad example ##################################

# This should fix all my headache
print_arch_is_the_best()
{
    echo "Arch is the best!"
}
```
