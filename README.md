# wpversion
Showing latest version of WordPress. Updated every 15 mins.

## How it works

#### List all tags in remote repo
```
git ls-remote --tags https://github.com/WordPress/WordPress.git | tail -n1
```
*..but only use the last one*

#### Split string on / 
```
awk -F'/' '{print $3}'
```
*turns "537057d65e2713934002276c10da44fb1ccca83e	refs/tags/4.9.4" => "4.9.4"*

#### Full example

```bash
# Latest WordPress version from Github mirror
git ls-remote --tags https://github.com/WordPress/WordPress.git | tail -n1 | awk -F'/' '{print $3}'
```
source/inspiration: https://stackoverflow.com/a/20742976


## TODO

- [ ] Move cron to Github Actions (WIP)

- [ ] Move hosting to Github
