1. Clone the repo
2. Initialize git submodules

```bash
git submodule init
git submodule update
```

3. Try to build the app

```bash
moon run :build
```

It fails with the latest version of moon `v1.33.3`, but work fine with `v1.28.3`.

```
Error: process::failed

  × Process git failed: exit code 128
  │
  │ fatal: /backend: '/backend' is outside repository at '/home/bludnic/Dev/moon-bug/
  │ moon/moon-submodule'
```

Test with different versions:

```bash
pnpm dlx @moonrepo/cli@1.28.3 run :build
pnpm dlx @moonrepo/cli@latest run :build
```
