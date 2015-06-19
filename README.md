# git identity

This util helps you to manage multiple identities.

# Usage

```
$ git identity --help
Usage: git-identity <command> [<arguments...>]
Commands:
  list|-l
  add <name> <email>
  count
  get|show <n>
  use|setup <n>
  check|-c
  whoami
```

```
$ git identity whoami
toto <toto@example.net>

$ git identity list
1: toto <toto@example.net>
2: titi <email@hided>
3: foo <bar@foobar.org>
4: webmaster <webmaster@myoffice.com>
5: aa bb cc <dev@myoffice.com>

$ git identity use 2
Done. Now use: titi <email@hided>

$ git identity whoami
titi <email@hided>

$ git config 
```

```
$ git identity whoami
toto <toto@example.net>

$ git config --local --get-regexp 'user\.'
user.name titi
user.email email@hided
```


# TODO

 * improve the check command to detect if they are more than one of your identity in commits
 * provide command to setup a default identity per repository
 * add a simple and fast way to check if the current identity follow the policies/setup
 * try to see to catch the commit command to check on the fly the identity (just before commiting)
 * support GPG keyid for each identity ?

# git autoconfig support

Some part of code is here to allow git-identity to be used inside the git-autoconfig util.
But I still not released git-autoconfig...

# License

 * My git-identity follows the MIT License
