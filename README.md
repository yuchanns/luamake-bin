# luamake-bin

Prebuilt standalone `luamake` binaries built from
[actboy168/luamake](https://github.com/actboy168/luamake).

## Layout

```text
bin/
  linux/
    luamake
  linux_arm64/
    luamake
  osx/
    luamake
  osx_arm64/
    luamake
  win32/
    luamake.exe
luamake-commit.txt
```

`luamake-commit.txt` records the upstream `actboy168/luamake` commit used for
the checked-in binaries.

## Updates

The update workflow runs daily and can also be triggered manually. It checks the
latest upstream `master` commit first. If that commit matches
`luamake-commit.txt`, the build is skipped. If upstream changed, the workflow
builds standalone binaries for all supported runner targets and pushes the
updated binaries back to this repository.
